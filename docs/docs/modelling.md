# Modelling

Modelling is at the heart of early Model-Based Testing (eMBT).  
In TestCompass, a model represents the intended behaviour of a system in a clear, structured, and explicit way.  
It serves as a shared thinking tool for business and technical stakeholders, enabling early discovery of ambiguities, risks, and misunderstandings.

This page explains the principles behind modelling in TestCompass and how models support systematic test generation and impact analysis.

---

## Purpose of Modelling

A model makes behaviour explicit.  
Instead of relying on assumptions, implicit knowledge, or scattered requirements, the model provides a single, visual representation of:

- decisions  
- business rules  
- flows and outcomes  
- boundary conditions  
- exceptional behaviour  

By externalising behaviour, teams can reason more clearly, validate understanding earlier, and avoid costly rework later in the development process.

---

## Modelling Principles

TestCompass uses a lightweight, expressive modelling style based on flowchart principles.  
The goal is not to create a perfect diagram, but to create a **shared understanding** of behaviour.

Key principles:

- **High-level abstraction**  
  Models should be understandable by both business and IT.

- **Explicit decisions**  
  Every decision is represented visually, making happy and unhappy paths visible.

- **Clear outcomes**  
  Each path leads to a result that reflects the expected system behaviour.

- **No hidden assumptions**  
  If something is unclear, it becomes visible in the model.

- **Iterative refinement**  
  Models evolve as requirements become clearer.

---

## Node Types

TestCompass models use a small set of node types to keep diagrams simple and readable:

- **Start / End** — entry and exit points of the behaviour  
- **Action / State** — steps or states in the flow  
- **Decision** — yes/no or conditional branching  
- **Result** — expected outcomes  
- **Comment** — questions, ambiguities, or notes for review  

These elements are sufficient to express complex behaviour without overwhelming the reader.

---

## Modelling Workflow

Modelling typically follows an iterative workflow aligned with the eMBT phases:

1. **Exploratory**  
   Initial model creation based on available requirements.  
   Questions, ambiguities, and assumptions are captured using comment nodes.

2. **Review**  
   The team discusses the model, resolves uncertainties, and updates the behaviour accordingly.

3. **Coverage**  
   Once validated, the model becomes the basis for systematic test generation.

4. **Checking**  
   The model and generated tests are used to verify the system under test.

This workflow ensures that modelling is not a one‑time activity but a continuous source of clarity.

---

## Boundary Conditions and Decisions

Every decision in the model should reflect:

- the positive path  
- the negative path  
- relevant boundary values  

This ensures that the model captures the full behavioural space and supports strong test coverage strategies.

---

## Modelling with Mermaid

TestCompass supports open, text-based modelling through Mermaid:

- Import Mermaid diagrams and convert them into testable models  
- Export models back to Mermaid for documentation or version control  

This enables teams to collaborate using plain text, pull requests, and version-controlled workflows.

➡️ See examples in the repository’s Mermaid section.

---

## Relationship to Test Generation

A well‑structured model directly enables:

- path-based test generation  
- decision coverage  
- boundary-oriented coverage  
- minimal path sets  
- custom constraints  

The quality of the model determines the quality of the generated tests.

➡️ Learn more: [Test Generation](test-generation.md)

---

## Relationship to Impact Analysis

When requirements change, the model is updated — not the tests.  
TestCompass automatically identifies:

- added behaviour  
- removed behaviour  
- changed behaviour  
- unaffected behaviour  

This keeps test suites maintainable and aligned with evolving requirements.

➡️ Learn more: [Impact Analysis](impact-analysis.md)

---

Modelling is not about drawing diagrams — it is about creating clarity.  
TestCompass provides the structure, the notation, and the workflow to make that clarity possible.

