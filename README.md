# Management Reflection Agent: Deterministic Logic Prototype

### Project Overview
This repository contains a functional prototype of an AI-driven Reflection Agent designed for daily management audits. As part of the Internshala/DeepThought assignment, I have architected a system that moves beyond simple chat and into **Knowledge Engineering**.

### 1. Technical Architecture
I implemented this agent as a **Deterministic State Machine** using a JSON-based Directed Acyclic Graph (DAG). 
* **Engine:** Python-based state navigator.
* **Knowledge Base:** `reflection-tree.json` (containing 28 unique nodes).

### 2. Guardrails & Hallucination Control
To meet the core requirement of countering AI hallucination, I decoupled the **Logic** from the **Content**:
* The agent does not "generate" responses on the fly. 
* It retrieves pre-validated psychological prompts from the JSON tree based on user input (Signals).
* This ensures 100% predictability and prevents the AI from providing vague or irrelevant advice.

### 3. The Three Axes of Reflection
The logic tree is engineered to test three specific psychological dimensions:
1. **Locus of Control:** Identifying if the user takes internal ownership (Victor) or blames external factors (Victim).
2. **Orientation:** Differentiating between a contribution-mindset (Giver) and an entitlement-mindset (Taker).
3. **Radius:** Measuring the impact of the user’s work from a self-centric perspective to an altrocentric (end-user focused) perspective.

### 4. Files in this Repo
* `main.ipynb`: The core execution notebook.
* `reflection-tree.json`: The data substrate containing the 28-node logic tree.
* `logic_diagram.png`: The original hand-drawn architectural plan documenting the engineering phase.
