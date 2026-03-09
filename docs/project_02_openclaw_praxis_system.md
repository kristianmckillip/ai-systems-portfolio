# Project 02 — OpenCLAW / Praxis AI Operations System

## Overview

Designed and deployed a governance-driven AI operations assistant combining a local AI gateway (OpenCLAW) with a Discord-integrated analytical bot (Praxis).

The goal was to create a verification-first AI system capable of assisting with infrastructure troubleshooting while minimizing hallucinated commands and unsafe automation.

---

## System Architecture


User
↓
Discord
↓
Clawbot
↓
OpenCLAW Gateway
↓
Google Gemini API


OpenCLAW functions as a **local orchestration layer** that manages identity, skills, routing, and operational rules.

Inference is handled via the Google Gemini API to avoid competing with local GPU workloads used for generative AI.

---

## Workspace Environment

Example workspace path:


C:\Users\Kristian.openclaw\workspace_sidekick


The workspace stores identity configuration, operational rules, and agent memory.

---

## Governance Architecture

Agent behavior is separated into modular policy files:

IDENTITY.md  
SOUL.md  
AGENTS.md  
TOOLS.md  
USER.md  
MEMORY.md  

Each file governs a different aspect of system behavior, preventing prompt drift and maintaining deterministic behavior.

---

## Verification-First Copilot Model

The system follows a structured troubleshooting workflow:

1. clarify the user objective  
2. provide copy-safe commands  
3. user executes commands locally  
4. user returns terminal output  
5. diagnosis occurs only from verified evidence  

This prevents hallucinated commands and transforms the AI into a **human-in-the-loop operations assistant**.

---

## Behavioral Governance

Praxis was designed with constrained conversational behavior to avoid disrupting group interactions.

Design characteristics:

• restrained analytical tone  
• occasional dry humor to remain socially natural  
• avoids dominating conversations  
• interjects only when analysis is useful  

---

## Passive Acknowledgment Signals

To maintain presence without adding noise to conversations, Praxis uses lightweight acknowledgment reactions.

Example:

👀 reaction to indicate a message has been seen.

This allows participants to know the agent is monitoring context without generating unnecessary responses.

This creates a **three-tier engagement model**:

1. passive monitoring  
2. lightweight acknowledgment  
3. analytical intervention  

---

## Failure Domain Modeling

The system explicitly separates possible failure sources:

• authentication issues  
• Discord permissions  
• channel enable / disable state  
• gateway runtime status  
• message routing errors  

This structured approach improves debugging accuracy.

---

## Observability

Runtime state is validated through:

• session inspection  
• model identity confirmation  
• activity timestamps  

This replaces assumption-based debugging with observable system state.

---

## Skills Demonstrated

• AI systems architecture  
• agent governance design  
• human-in-the-loop workflows  
• Discord bot integration  
• failure domain isolation  
• AI safety design  
• observability-driven debugging  

---

## Outcome

The result is a structured AI operations assistant capable of supporting infrastructure troubleshooting while enforcing verification before action.

The system demonstrates practical concepts used in AI reliability engineering, including governed agent behavior, human-in-the-loop troubleshooting workflows, and verification-first command execution.

This project highlights the importance of operational guardrails when deploying AI assistants in real technical environments.