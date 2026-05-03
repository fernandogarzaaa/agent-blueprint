# 🧠 Chimera Builder — PRD & System Blueprint

> AMD hackathon entry 1.

## 1. Overview

**Product Name:** Chimera Builder
**Category:** Autonomous Multi-Agent Software Engineering System


**Vision:**  
Build an autonomous AI system that can:
- Analyze a GitHub repository
- Generate a development roadmap
- Implement improvements
- Simulate user interaction
- Iteratively improve itself

---

## 2. Objectives

### Primary Goals
- Move beyond single-agent systems into **true multi-agent orchestration**
- Demonstrate **autonomous execution loop**
- Provide **real, inspectable outputs** (not just chat)

### Success Criteria
- System can process a repo end-to-end
- Agents visibly collaborate
- Output includes:
  - Audit report
  - Roadmap
  - Code improvements
  - Test simulation results

---

## 3. Core Features

### 3.1 Repository Intelligence Engine
**Description:**  
Analyzes repository structure, code, and dependencies.

**Capabilities:**
- Parse directory structure
- Identify tech stack
- Detect missing components
- Highlight code issues

---

### 3.2 Multi-Agent System

#### Agents

**1. Analyst Agent**
- Codebase understanding
- Architecture mapping
- Issue detection

**2. Planner Agent**
- Generates roadmap
- Prioritizes tasks
- Breaks down work

**3. Builder Agent**
- Writes/modifies code
- Implements features
- Refactors components

**4. Tester Agent**
- Simulates user behavior
- Identifies usability issues
- Validates workflows

**5. Critic Agent**
- Reviews outputs of all agents
- Detects inconsistencies
- Suggests improvements

---

### 3.3 Autonomous Execution Loop

**Core Loop:**
Plan → Execute → Evaluate → Improve → Repeat

**Requirements:**
- Loop must run at least 2–3 iterations
- Each iteration must produce visible improvements

---

### 3.4 Memory System

**Types:**
- Episodic (past runs)
- Semantic (repo knowledge)
- Procedural (decisions made)

**Storage:**
- `.context/`
  - `/tasks`
  - `/sessions`
  - `/decisions`

---

### 3.5 Execution Engine

**Responsibilities:**
- Run generated code
- Apply file changes
- Execute test simulations

---

## 4. System Architecture

```

User Input
↓
Task Decomposer (Coordinator)
↓
Agent Swarm

* Analyst
* Planner
* Builder
* Tester
* Critic
  ↓
  Execution Engine
  ↓
  Evaluation Loop
  ↓
  Memory Storage
  ↓
  Final Output

````

---

## 5. Repository Integration Plan

### Aegis-Swarm → Memory Layer
Extract:
- `.context` structure
- Task/session tracking
- Decision logs

Use for:
- Persistent memory
- Execution history

---

### Project AETHER → Orchestration Core
Extract:
- Task decomposition logic
- Model routing
- Coordination patterns

Use for:
- Central coordinator agent

---

### Project WRAITH → Execution Engine
Extract:
- Automation scripts
- Background execution logic

Use for:
- Task execution layer

---

### Project EVO → Improvement Loop
Extract:
- Feedback mechanisms
- Iteration logic

Use for:
- Self-improving loop

---

## 6. Agent Design Specification

Each agent must follow this schema:

```json
{
  "name": "AgentName",
  "role": "Primary responsibility",
  "goal": "Objective",
  "tools": [],
  "memory_access": [],
  "input_format": {},
  "output_format": {}
}
````

---

## 7. Execution Flow

### Step 1: Input

User provides:

* GitHub repository URL

---

### Step 2: Analysis

Analyst Agent:

* Parses repo
* Builds architecture map
* Identifies issues

---

### Step 3: Planning

Planner Agent:

* Generates roadmap
* Prioritizes tasks

---

### Step 4: Execution

Builder Agent:

* Implements improvements

---

### Step 5: Testing

Tester Agent:

* Simulates user interaction

---

### Step 6: Evaluation

Critic Agent:

* Reviews outputs
* Suggests refinements

---

### Step 7: Iteration

System loops:

* Applies improvements
* Re-runs evaluation

---

## 8. Tech Stack

### Core Framework

* CrewAI (preferred) or LangChain

### Models

* Qwen / DeepSeek (reasoning)
* Lightweight model for fast agents

### Serving

* vLLM

### Memory

* FAISS / Chroma

### Execution

* Python runtime
* File system access

---

## 9. Folder Structure

```

chimera-builder/
│
├── core/
│   ├── coordinator/
│   ├── agents/
│   ├── loop/
│
├── memory/
│   ├── .context/
│   │   ├── tasks/
│   │   ├── sessions/
│   │   ├── decisions/
│
├── execution/
│   ├── runner/
│   ├── file_manager/
│
├── analysis/
│   ├── repo_parser/
│   ├── dependency_mapper/
│
├── config/
│   ├── agents.json
│   ├── models.yaml
│
├── interface/
│   ├── cli.py
│   ├── api.py
│
└── main.py

```

---

## 10. Demo Requirements

### Must Show:

* Agent collaboration (visible logs)
* Task delegation
* Iteration loop

### Input:

```

Analyze this repository: <repo_url>

```

### Output:

* Audit report
* Roadmap
* Code improvements
* Test simulation results

---

## 11. Differentiators

* Multi-agent collaboration (not single LLM)
* Persistent memory across runs
* Autonomous improvement loop
* Real execution (not just suggestions)

---

## 12. Constraints

* Must run within hackathon time limits
* Avoid over-engineering UI
* Focus on backend intelligence + demo clarity

---

## 13. Future Enhancements (Optional)

* GUI dashboard for agent visualization
* Real-time agent communication graph
* Multi-repo support
* CI/CD integration

---

## 14. Deliverables

* Working prototype
* Demo script
* Open-source repository
* Technical walkthrough
