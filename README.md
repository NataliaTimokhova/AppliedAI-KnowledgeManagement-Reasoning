# AppliedAI-KnowledgeManagement-Reasoning
Applied AI – Knowledge Management and Reasoning (D0034E) is a master-level course at Luleå University of Technology that provides a practical introduction to Symbolic Artificial Intelligence. The course explores how knowledge can be represented, structured, and used for automated reasoning.

---

## 📁 Repository Structure

```
.
│
├── Lab1_Logical_Agents.ipynb        # Lab 1: logic engine, models, KB, querying
├── Lab2_Wumpus_World.ipynb          # Lab 2: knowledge-based agent + Wumpus World
│
└── README.md                        # Project description
```

---

# Lab 1 – Propositional Logic & Queries

### 🎯 Objective
Build a **minimal propositional logic engine** and use it to evaluate statements, construct a knowledge base, and check entailment by model enumeration.

### 📌 What is implemented

#### 1. **Logical Sentence Classes**
Custom Python classes to represent logic formulas:

- And(A, B)
- Or(A, B)
- Not(A)
- Implies(A, B)
- Equals(A, B)

#### 2. **Chaining Function**
Builds nested logical expressions automatically.

#### 3. **Evaluation Function**
Evaluates logical expressions in a given model, returning:
- True
- False
- None (unknown)

#### 4. **Query Function**
Model checking to determine whether statements follow from a knowledge base.

---

# Lab 2 – Logical Agent in the Wumpus World

### 🎯 Objective
Create a knowledge‑based agent that uses propositional logic to safely navigate the Wumpus World.

The environment includes:
- one Wumpus  
- several pits  
- one piece of gold  
- the agent itself  

### Percepts:
- stench  
- breeze  
- glitter  
- bump  
- scream  

### Actions:
- forward  
- turn_left  
- turn_right  
- grab  
- shoot  
- climb  

### Performance scoring:
- each action: -1  
- leaving with gold: +1000  
- dying: -1000  

---

# 🧠 Knowledge Base

Symbols such as:
- P_x_y (pit)
- W_x_y (wumpus)
- B_x_y (breeze)
- S_x_y (stench)
- Safe_x_y (safe tile)

Rules define relationships between pits/breeze and wumpus/stench.

---

# 🤖 SimpleAgent Strategy

The agent:
1. Updates its knowledge base with percepts  
2. Marks current tile as safe  
3. Grabs gold when detected  
4. Returns to start after grabbing gold  
5. Uses A* search to navigate between known safe tiles  

---

# ▶️ Running

Clone the repository, install Jupyter Notebook, and run both notebooks.

---

# ✔️ Notes

This implementation follows the exact requirements of the LTU Applied AI course.

