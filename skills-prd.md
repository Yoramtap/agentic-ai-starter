---
name: prd
description: >
  Generate a Product Requirements Document (PRD) for a feature that is already clear.
  Use ONLY when explicitly requested.
  Do NOT use during early exploration or planning.
---

# PRD Generator (Formalization Mode)

## When to use
- The idea is already clear and agreed upon
- Decisions are mostly made
- The goal is to create a handoff-ready specification

Do NOT use for vague ideas.

---

## The Job

1. Receive a clear feature description
2. Ask 3–5 essential clarifying questions (lettered options)
3. Generate a structured PRD
4. Save it to `tasks/prd-[feature-name].md`

**Important:**  
Do NOT start implementing. Only document.

---

## Step 1: Clarifying Questions

Ask only critical questions where ambiguity remains.

Focus on:
- Problem / Goal
- Core functionality
- Scope / Non-goals
- Success criteria

### Question Format
What is the primary goal of this feature?
A. ...
B. ...
C. ...
D. Other: ___


Users may answer with `1A, 2C, 3B`.

---

## Step 2: PRD Structure

### 1. Overview
Brief description of the feature and problem.

### 2. Goals
Specific, measurable objectives.

### 3. User Stories
Each must include:
- Title
- Description (“As a … I want … so that …”)
- Acceptance Criteria (verifiable checklist)

Stories must be small enough to implement in one focused session.

### 4. Functional Requirements
Numbered, explicit requirements (FR-1, FR-2, …).

### 5. Non-Goals
Clear boundaries of what is out of scope.

### 6. Design Considerations (optional)

### 7. Technical Considerations (optional)

### 8. Success Metrics
How success is measured.

### 9. Open Questions
Anything unresolved.

---

## Writing Rules

- Be explicit and unambiguous
- Avoid jargon or explain it
- Write for a junior developer or AI agent
- Use numbered lists and checklists
- Prefer concrete examples

---

## Output

- Format: Markdown
- Location: `tasks/`
- Filename: `prd-[feature-name].md` (kebab-case)

