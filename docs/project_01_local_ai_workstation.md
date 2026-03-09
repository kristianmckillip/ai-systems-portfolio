# Project 01 — Local AI Workstation Architecture

## Overview

Designed and stabilized a GPU-accelerated local AI workstation capable of running generative image models and AI tooling without reliance on cloud GPU infrastructure.

The environment supports Stable Diffusion image generation, experimentation with multiple AI toolchains, and hands-on development of local AI infrastructure.

---

## Hardware

**Machine**  
MSI Thin A15 B7VF laptop

**CPU**  
AMD Ryzen 5 7535HS  
6 cores / 12 threads

**GPU**  
NVIDIA RTX 4060 Laptop GPU

**RAM**  
32 GB DDR5

**Operating System**  
Windows 11 Home

---

## GPU Performance Tuning

The RTX 4060 GPU was tuned using MSI Afterburner to optimize inference workloads.

Configuration highlights:

* Memory clock offset: **+300 MHz**
* Core clock: default (for stability)
* Stable configuration when plugged in
* Separate safe profile used when running on battery to prevent instability

This configuration allowed improved generation throughput while maintaining system stability.

---

## Environment Management

Python environments were isolated using **venv**.

Example structure:

env_core  
env_image

Environment isolation reduced dependency conflicts and made system recovery easier during upgrades or debugging.

---

## AI Toolchain

Installed and configured:

InvokeAI  
ComfyUI  
Ollama

InvokeAI became the primary workflow interface due to its board-based generation system and stability.

ComfyUI was installed and configured successfully but is currently used primarily for experimentation due to the complexity of node-based workflows.

---

## Model Workloads

Primary models used:

* **SDXL models** for high-quality generation
* **Stable Diffusion 1.5 models** for faster iteration

More demanding architectures such as Flux were evaluated but proved inconsistent under current hardware constraints.

This reinforced the importance of selecting models appropriate for available compute resources.

---

## Image Generation Workflow

Capabilities currently used:

* seed-controlled image generation
* LoRA integration
* prompt iteration
* basic inpainting workflows in InvokeAI

---

## Engineering Challenges Solved

During system setup multiple technical issues were resolved:

* PyTorch CPU vs CUDA mismatch errors
* Python dependency conflicts
* local service blocking by antivirus
* model loading errors
* environment rebuilds after failed upgrades

These debugging cycles were critical to stabilizing the workstation.

---

## Skills Demonstrated

• AI infrastructure deployment  
• GPU compute configuration  
• Python environment management  
• dependency debugging  
• local AI model management  
• toolchain troubleshooting  
• workflow optimization  

---

## Outcome

The final system provides a stable local AI environment capable of running modern generative image models while maintaining full control over infrastructure.

This workstation became the foundation for the remaining projects in the portfolio, enabling experimentation with diffusion workflows, prompt orchestration systems, and AI assistant architectures.

The project demonstrates practical experience in:

• building AI infrastructure from scratch  
• diagnosing environment failures  
• stabilizing GPU-accelerated workloads  
• maintaining reproducible AI toolchains