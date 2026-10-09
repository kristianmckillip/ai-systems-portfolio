# Kristian McKillip | AI Systems & Software Portfolio

I build local AI workflows, governed assistants, and practical software with AI-assisted development. This portfolio documents the problems, implementation decisions, testing, and limits behind that work.

## Featured project: ClearSpace Personal v1

**Completed personal release · Windows · VITURE glasses · Signed off October 7, 2026**

ClearSpace is a spatial multi-panel workspace for Windows and VITURE glasses. The signed-off configuration uses six panels: one primary panel and five virtual panels.

I defined requirements, prioritized the release scope, and performed live testing, with AI-assisted coding supporting implementation.

The final six-panel sign-off covered workspace save, relaunch, and clean exit. Earlier development testing covered presentation persistence, group-distance apply/undo, FitSource, keyboard panel navigation, stop and return-to-primary controls, and settings capture pause/restore. The case study separates these test stages. The desktop release includes a custom icon.

[Read the ClearSpace case study](docs/project_06_clearspace_personal.md)

## Local AI systems and operational projects

These five projects document the local infrastructure, operating procedures, prototypes, and agent designs developed before ClearSpace.

### 01 · Local AI Workstation Architecture
Configured and stabilized an RTX 4060 laptop environment for local generative AI. The write-up covers InvokeAI, ComfyUI, Ollama, isolated Python environments, CUDA mismatch troubleshooting, dependency recovery, and model selection within hardware limits.

[Read the workstation project](docs/project_01_local_ai_workstation.md)

### 02 · OpenCLAW / Praxis AI Operations System
Deployed a Discord-connected operations assistant using a local OpenCLAW gateway and Gemini API inference. Its human-in-the-loop workflow uses commands run by the user and returned terminal output to guide troubleshooting.

[Read the Praxis project](docs/project_02_openclaw_praxis_system.md)

### 03 · Diffusion Model Operations Framework
Developed an InvokeAI operating framework for an 8 GB VRAM workstation. It covers model intake, LoRA classification, prompt structure, repeatable generation workflows, failure diagnosis, canvas geometry, and asset cleanup.

[Read the diffusion operations project](docs/project_03_diffusion_operations_framework.md)

### 04 · Prompt Orchestration Engine
Built a prototype on Emergent for staged prompt construction and model adaptation. The documented workflow extracts visual attributes from reference images, turns them into structured reusable prompt components, and adapts assembled prompts for diffusion model families.

[Read the prompt orchestration project](docs/project_04_prompt_orchestration_engine.md)

### 05 · AI Agent Systems & Behavioral Governance
Developed specialized assistant roles for operations, prompt optimization, installation support, planning, and reflective dialogue. The documentation explains the behavioral rules and interaction patterns for Praxis, Lyra, Nova, Veridian, and Hale.

[Read the agent governance project](docs/project_05_ai_agent_systems_governance.md)

## Development context

The local AI projects were documented on a Windows 11 workstation with a Ryzen 5 7535HS, RTX 4060 Laptop GPU with 8 GB VRAM, and 32 GB DDR5 RAM. InvokeAI was the primary diffusion interface; ComfyUI supported experimentation.

Each project page provides its own technical context. The portfolio currently presents project documentation; source code, test artifacts, and demonstrations are included only where explicitly linked.

