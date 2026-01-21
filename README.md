# Calm planning assistant

This repository defines a **two-phase AI planning system** designed for beginners.

Its goal is to help turn **vague ideas into clear, small plans**, and only later — when explicitly requested — into **formal Product Requirements Documents (PRDs)**.

The system prioritizes:
- clarity over speed
- small steps over big leaps
- explicit phase changes over implicit behavior

---

## Core Idea

Most planning fails because people are pushed into **specification too early**.

This system separates work into two explicit phases:

1. **Exploration & Clarity**  
   (thinking, understanding, shaping the idea)
2. **Formalization (PRD mode)**  
   (documenting a clear idea for implementation)

The assistant never switches phases unless you explicitly ask it to.

---

## Repository Structure

/
├─ identity.md # Who the assistant is (permanent)
├─ principles.md # Learning rules (permanent)
├─ skills.md # Allowed behaviors in planning mode
├─ skills-prd.md # Explicit PRD mode (opt-in only)
├─ active.md # Current session scratchpad (temporary)
└─ tasks/ # Generated PRDs live here


---

## File Roles (Plain English)

### `identity.md`
Defines the assistant’s **role, tone, and definition of “done”**.

This file should almost never change.

---

### `principles.md`
Defines **how learning and planning should happen**:
- small steps
- no jumping ahead
- stop when unsure
- stop when done

These rules override speed or completeness.

---

### `skills.md` (Planning Mode)
Defines the **only behaviors allowed during exploration**:

- clarify_idea
- restate_idea
- create_plan
- ask_for_feedback

This keeps the assistant calm, beginner-friendly, and predictable.

---

### `active.md` (Session Scratchpad)
This file represents **what we are working on right now**.

It is:
- temporary
- expected to change
- safe to delete or replace

It defines:
- the current idea
- non-goals
- assumptions
- the next tiny action
- what “done for today” means

---

### `skills-prd.md` (PRD Mode)
This is a **separate mode**, not a normal skill.

It is used only when you explicitly say something like:
- “Switch to PRD mode”
- “Generate a PRD for this feature”

PRD mode:
- assumes the idea is already clear
- asks structured clarifying questions
- produces a handoff-ready document
- saves it to `tasks/prd-[feature-name].md`

It must **never** be used during early exploration.

---

## How to Use This System

### Typical Flow

1. Start with `active.md`
2. Explore the idea calmly using planning skills
3. Stop when the goal and steps feel clear
4. **Explicitly decide** to formalize
5. Switch to PRD mode
6. Generate a PRD in `tasks/`

At no point should the assistant jump ahead without permission.

---

## Design Philosophy

This system separates:

- **Epistemic clarity**  
  (“Do I understand what I want?”)

from

- **Communicative clarity**  
  (“Can someone else build this?”)

Most tools mix these. This system does not.

---

## When to Stop

Each session defines its own stopping condition in `active.md`.

When that condition is met:
- the assistant stops
- no new tasks are introduced
- momentum is intentionally paused

This is a feature, not a limitation.

---

## Intended Audience

- Beginners
- People learning to plan clearly
- Developers who want calmer thinking
- Anyone tired of premature optimization

---

## Non-Goals

This system is NOT:
- a task manager
- an automation framework
- a coding assistant by default
- a replacement for thinking

It is a **thinking aid**
