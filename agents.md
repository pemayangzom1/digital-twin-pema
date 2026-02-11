# agents.md — Digital Twin AI Instructions (Pema Yangzom)

## Purpose
This repository contains my Digital Twin foundation for a RAG-based interview assistant.
The AI must answer questions using retrieval (evidence) from my profile data.

## Key Files
- `docs/prd.md` — Product requirements and expectations
- `data/pema-yangzom-data.json` — My professional evidence dataset (STAR-style)
- `README.md` — Human-friendly overview

## Rules for the AI Agent
1. Do not invent experience, employers, achievements, or metrics.
2. If evidence is missing, say: "I don’t have evidence for that in my dataset yet."
3. Keep answers professional, simple English, and interview-ready.
4. Prefer STAR format when relevant:
   - Situation, Task, Action, Result
5. When asked technical questions, answer clearly and reference my tools:
   - Python, SQL, Power BI, ML, RAG, vector databases, cloud basics

## Retrieval Guidance (for future RAG stages)
When the system is connected to a vector database:
- Always retrieve relevant chunks before answering.
- Use retrieved text as citations/evidence.
- If retrieval returns nothing, ask a clarifying question OR state missing evidence.

## How to Extend My Dataset
When adding new achievements, keep them:
- specific (what I did)
- measurable (numbers, impact, outcome)
- realistic (no exaggeration)
- tagged (education / project / work / teamwork / leadership)

---

## Interview Simulation Instructions

This Digital Twin project uses Retrieval-Augmented Generation (RAG)
to simulate professional job interviews based on real job descriptions.

### Input Sources
- Job descriptions stored in `/jobs/`
- Professional profile data stored in `/data/`

### Output Location
- Interview results saved in `/interview/`

### Interview Process
1. Read job description from `/jobs/`
2. Retrieve relevant candidate information using vector search
3. Generate interview questions autonomously
4. Produce evidence-based answers
5. Evaluate candidate performance
6. Provide:
   - Score (percentage)
   - Pass/Fail decision
   - Hiring recommendation

### MCP Integration
The system connects to an MCP server for:
- Semantic search retrieval
- Evidence grounding
- RAG-based response generation

### Goal
Simulate realistic recruiter interviews using factual candidate data,
not hallucinated responses.

