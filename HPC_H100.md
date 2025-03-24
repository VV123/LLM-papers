# how to use HPC H100 nodes



## Step 1

## Step 2

## Step 3


## Some questions
- How many H100 does HPC have?

- How to use multiple H100 GPUs?

# H100 GPU Availability Test on HPC

## Purpose  
This document summarizes the verification process for accessing and using H100 GPUs on the HPC system.

## Summary  
- The HPC system has 4 NVIDIA H100 GPUs, all located on a single node (crest-g001).
- Successfully ran a lightweight inference task using one H100 GPU.  
- Submitting a job requesting 2–4 GPUs fails due to “QOSMaxGRESPerUser”.  
- The system restricts each job to one GPU.

## Notes  
- Previous two-GPU usage was likely from running one Slurm job and one manual Python script, each using one GPU.  
- This does not indicate true multi-GPU support in a single job.  
- Single-GPU jobs work.  
- Multi-GPU jobs are currently blocked by system policy.
