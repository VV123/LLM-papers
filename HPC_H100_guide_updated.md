# H100 GPU Access Guide for TAMU-CC HPC

## Overview
This guide provides detailed instructions for accessing and utilizing NVIDIA H100 GPUs on the Texas A&M University-Corpus Christi (TAMU-CC) High Performance Computing (HPC) system. It covers everything from account setup to troubleshooting.

## Table of Contents
1. [Account Setup](#1-account-setup)
2. [Connecting to the HPC](#2-connecting-to-the-hpc)
3. [File Transfer](#3-file-transfer)
4. [H100 GPU Verification](#4-h100-gpu-verification)
5. [Environment Setup](#5-environment-setup)
6. [Job Submission](#6-job-submission)
7. [Monitoring Jobs](#7-monitoring-jobs)
8. [Output and Results](#8-output-and-results)
9. [GPU Usage Notes](#9-gpu-usage-notes)
10. [FAQ](#10-faq)
11. [Acknowledgments](#11-acknowledgments)

## 1. Account Setup
**Request an HPC Account**
   - Email `hpc-support@tamucc.edu` with:
      - Your full name
      - Department/affiliation
      - Research purpose (brief description)
      - Desired software/resources
   - Account credentials will be created in the format `[islander_id]@crest.tamucc.edu`


## 2. Connecting to the HPC
1. **SSH Connection**
   ```bash
   ssh [islander_id]@crest-login.tamucc.edu
   ```

2. **Connection Troubleshooting**
   - Ensure you're connected to the university network or using VPN if off-campus
   - If persistent issues occur, contact `hpc-support@tamucc.edu`

## 3. File Transfer
1. **Upload Files to HPC**
   ```bash
   # Upload a single file
   scp local_file.py [islander_id]@crest-login.tamucc.edu:/home/[islander_id]/
   
   # Upload an entire folder
   scp -r local_folder/ [islander_id]@crest-login.tamucc.edu:/home/[islander_id]/
   ```

2. **Download Files from HPC**
   ```bash
   # Download a single file
   scp [islander_id]@crest-login.tamucc.edu:/home/[islander_id]/remote_file.py ./
   
   # Download an entire folder
   scp -r [islander_id]@crest-login.tamucc.edu:/home/[islander_id]/remote_folder/ ./
   ```

3. **Alternative Transfer Methods**
   - Using SFTP client like WinSCP

## 4. H100 GPU Verification
1. **Check GPU Availability**
   ```bash
   sinfo -p gpu -o "%N %G"
   ```

   Expected output:
   ```
   NODELIST    GRES
   crest-g001  gpu:h100:4
   ```
   This indicates 4 NVIDIA H100 GPUs located on node `crest-g001`.

2. **Check Current GPU Usage**
   ```bash
   squeue -p gpu
   ```
   This shows jobs currently running or queued on the GPU partition.

## 5. Environment Setup
1. **Load Anaconda Module**
   ```bash
   module load miniconda3/24.1.2
   ```

2. **Create a Conda Environment**
   ```bash
   conda create -n my_env python=3.10
   conda activate my_env
   ```

3. **Install Required Packages**
   ```bash
   pip install -r requirements.txt
   ```


## 6. Job Submission
1. **Create a SLURM Script**
   Create `gpu_job.slurm`:
   ```bash
   #!/bin/bash
   #SBATCH -J h100_job           # Job name
   #SBATCH -o job_%j.out         # Output file (%j will be replaced by job ID)
   #SBATCH -e job_%j.err         # Error file
   #SBATCH -t 12:00:00           # Max runtime (HH:MM:SS) (Currently the max allowed amount is 24 Hrs for all users)

   #SBATCH -p gpu                # Partition/queue name
   #SBATCH --gres=gpu:1          # Request 1 H100 GPU specifically
   #SBATCH --qos gpu             # Quality of Service

   # Load modules and activate environment
   module load miniconda3/24.1.2
   conda init
   conda activate my_env

   # Print job info
   echo "Job started at $(date)"
   echo "Running on node: $(hostname)"

   # Run your code
   python my_script.py

   # clean up
   module unload miniconda3/24.1.2
   echo "Job completed at $(date)"
   ```

2. **Submit the Job**
   ```bash
   sbatch gpu_job.slurm
   ```

3. **Job Script Parameters Explained**
   - `-J`: Job name for identification
   - `-o/-e`: Output/error file paths
   - `-t`: Maximum runtime (current limit is 24 hours)
   - `-p`: Partition to use (gpu for GPU jobs)
   - `--gres`: GPU resource specification
   - `--qos`: Quality of Service

## 7. Monitoring Jobs
1. **Check Job Status**
   ```bash
   squeue -u [islander_id]
   ```

2. **View All GPU Jobs**
   ```bash
   squeue -p gpu
   ```

3. **Cancel a Job**
   ```bash
   scancel --name=JOB_NAME
   ```
   Or cancel all your jobs:
   ```bash
   scancel -u [islander_id]
   ```
4. **Job Information**
   ```bash
   scontrol show job [job_id]
   ```
   
## 8. Output and Results
1. **View Job Output**
   ```bash
   cat job_[job_id].out
   ```

2. **View Job Error**
   ```bash
   cat job_[job_id].err
   ```

3. **Monitor Output in Real-time**
   ```bash
   tail -f job_[job_id].out
   ```

## 9. GPU Usage Notes
- A single H100 GPU was successfully detected and used in this verification task.
- Submitting jobs with 2–4 GPUs results in a pending state with the scheduler message: `QOSMaxGRESPerUser`.
- The system currently limits each job to one GPU based on the Quality of Service (QOS) configuration.
- In previous tests, usage of two GPUs occurred when two independent processes were run (e.g., a Slurm job and a separate manual script), each occupying one GPU. This does not reflect multi-GPU support within a single job.
- Submitting a job requesting 2–4 GPUs fails due to “QOSMaxGRESPerUser”. The system restricts each job to one GPU.


## 10. FAQ
1. How many H100 does HPC have?

   - There are **4 NVIDIA H100 GPUs**, all located on node `crest-g001`. 
   
   - NODELIST GRES crest-g001 gpu:h100:4
   
   - Which means the system has 4 NVIDIA H100 GPUs, all located on node crest-g001.

2. How to use multiple H100 GPUs?

   - Multi-GPU usage is restricted by QOSMaxGRESPerUser; only one H100 GPU can be allocated per job.

## 11. Acknowledgments
- I would like to thank [VV123](https://github.com/VV123) for their insights in their [HPC H100 guide](https://github.com/VV123/LLM-papers/blob/main/HPC_H100.md), which helped create this guide.

---

*Last Updated: April 6, 2025*
