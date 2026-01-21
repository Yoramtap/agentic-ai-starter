# PRD: RTS-Style Character Selection Screen (Current State)

## 1. Overview

This project is a single-page, RTS-inspired character selection screen built as a static webpage (HTML/CSS/JS), deployed via GitHub Pages.

The screen presents a pixel-art mage character in a centered UI panel over a pixel-art forest backdrop. The character feels “alive” through idle animation and responsive feedback, similar to classic RTS or RPG character-select menus.

This document describes **what currently exists**, not future plans.

---

## 2. Current Features

### Visual Presentation
- Full-screen pixel-art forest background (`background.png`)
- Centered, chunky UI-style selection panel
- Inner “portrait window” with white background to blend with sprite assets
- Panel remains readable against the background

### Character Display
- A blue mage character rendered from a **sprite sheet** (`mage-sheet.png`)
- Sprite sheet layout is a 2×2 grid:
  - Top-left: Front view
  - Top-right: Left-facing view
  - Bottom-left: Back view
  - Bottom-right: Unused / no right-facing sprite

### Idle Presence
- Gentle “breathing” idle animation (subtle scale up/down)
- Runs continuously when the character is idle
- Does not interfere with interaction animations

---

## 3. Controls & Interactions

### Keyboard Controls
- ↓ (Down Arrow): Show front view
- ↑ (Up Arrow): Show back view
- ← (Left Arrow): Show left-facing view
- → (Right Arrow): Show **mirrored left-facing view** (temporary placeholder)
- Arrow keys do **not** scroll the page

### Mouse / Keyboard Feedback
- Clicking the character triggers:
  - sprite change (if applicable)
  - wiggle animation
  - glow/brightness flash
  - sparkle sound effect
- Spacebar mirrors click behavior (toggle + feedback)

---

## 4. Animations & Feedback

### On Interaction
- Playful wiggle animation (subtle but noticeable)
- Brief glow/brightness flash
- Sparkle sound effect (`sparkle.mp3`)
  - Sound restarts on each interaction
  - No overlapping audio

### Idle
- Breathing pulse continues naturally after interactions

---

## 5. Known Limitations / Technical Debt

- There is **no true right-facing sprite** in the mage sprite sheet
  - Right direction is currently faked by mirroring the left-facing sprite
- Sprite sheet has a baked-in white background
  - Transparency is not available in current assets
- Only one character is implemented
- No mouse-drag rotation yet (keyboard only)

These are known and intentional limitations, not bugs.

---

## 6. Non-Goals (Out of Scope for Current State)

- Multiple characters or character roster
- Backend or persistence
- True 3D rendering
- Advanced animation blending
- Mobile/touch optimization
- Game logic beyond selection screen

---

## 7. Extension Points (Future-Friendly)

These are **not commitments**, just obvious next directions:
- Regenerate sprite sheet with a true right-facing view
- Expand to 4 or 8-direction sprite turnaround
- Add character name / faction label
- Add “confirmed selection” state
- Add mouse-drag rotation
- Support multiple selectable characters

---

## 8. Source of Truth

- Code and assets live in the GitHub repository
- `index.html` is the primary implementation file
- This PRD is the reference for current behavior and known gaps
