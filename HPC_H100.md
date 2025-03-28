# H100 GPU Access Guide on TAMU-CC HPC

## Purpose  
This guide provides a step-by-step workflow to verify the availability and usage of H100 GPUs on the TAMU-CC High Performance Computing (HPC) system using a lightweight deep learning test.

## 1. Request an HPC Account  
Email `hpc-support@tamucc.edu` with full name, department, and research purpose.  
An account will be created in the format `netid@crest.tamucc.edu`.

## 2. Connect to the HPC via SSH  
```bash
ssh netid@crest.tamucc.edu
```

## 3. Upload an Entire Folder to HPC  
Use `scp` to upload a local folder to the HPC home directory:  
```bash
scp -r local_folder/ netid@crest.tamucc.edu:/home/netid/
```

## 4. Check H100 Availability  
```bash
sinfo -p gpu -o "%N %G"
```

Expected output:
```
NODELIST    GRES
crest-g001  gpu:h100:4
```

This indicates that the system has 4 NVIDIA H100 GPUs located on node `crest-g001`.

## 5. Prepare the Test Script

**Python file**: `check_all_gpus.py`
```python
import torch

device = torch.device("cuda" if torch.cuda.is_available() else "cpu")
print(f"Using device: {device}")
x = torch.rand(1000, 1000).to(device)
y = torch.mm(x, x)
print("Matrix multiplication complete.")
print(f"GPU Name: {torch.cuda.get_device_name(device)}")
```

**SLURM script**: `check_all_gpus.slurm`
```bash
#!/bin/bash
#SBATCH --job-name=gpu-check
#SBATCH --partition=gpu
#SBATCH --qos=gpu
#SBATCH --gres=gpu:h100:1
#SBATCH --time=00:05:00
#SBATCH --output=check_all_gpus.log

module purge
module load pytorch-py39-cuda11.8-gcc11/1.13.0

python3 /home/netid/check_all_gpus.py
```

## 6. Submit the Job  
```bash
sbatch /home/netid/check_all_gpus.slurm
```

## 7. View Output  
```bash
cat check_all_gpus.log
```

Expected output:
```
Using device: cuda
Matrix multiplication complete.
GPU Name: NVIDIA H100 80GB HBM3
```

## Notes

- A single H100 GPU was successfully detected and used in this verification task.
- Submitting jobs with 2–4 GPUs results in a pending state with the scheduler message: `QOSMaxGRESPerUser`.
- The system currently limits each job to one GPU based on the Quality of Service (QOS) configuration.
- In previous tests, usage of two GPUs occurred when two independent processes were run (e.g., a Slurm job and a separate manual script), each occupying one GPU. This does not reflect multi-GPU support within a single job.
- Submitting a job requesting 2–4 GPUs fails due to “QOSMaxGRESPerUser”. The system restricts each job to one GPU.

## Some questions
- How many H100 does HPC have?

  There are **4 NVIDIA H100 GPUs**, all located on node `crest-g001`. 
  
  NODELIST GRES
  crest-g001 gpu:h100:4
  
  Which means the system has 4 NVIDIA H100 GPUs, all located on node crest-g001.

- How to use multiple H100 GPUs?

  Multi-GPU usage is restricted by QOSMaxGRESPerUser; only one H100 GPU can be allocated per job.
  
