---
name: Occam's Razor
description: Complexity Pruning and Simplification using the Subtraction Method.
---

# Occam's Razor (The Subtraction Method)

> "Entities should not be multiplied without necessity." - William of Ockham

## When to Use
*   **Before** adding a new library or dependency.
*   **When** refactoring legacy code.
*   **When** a solution feels "heavy", "boilerplate-y", or hard to explain.
*   **During** Code Review to challenge over-engineering.

## The Protocol: The Subtraction Method
Do not ask "What can I add?". Ask "What can I remove?".
Follow these 4 steps explicitly.

### 1. The Hypothesis
Assume the current solution is over-engineered.
State: **"This solution is too complex. It can be simpler."**

### 2. The "Why" Test
Iterate through every component (file, class, function, library, config).
Ask: **"What precisely breaks if I delete this?"**
*   *Weak Answer:* "Ideally we might need it later..." -> **DELETE**.
*   *Weak Answer:* "It makes it more 'enterprisey'..." -> **DELETE**.
*   *Strong Answer:* "The application crashes on startup." -> **KEEP**.

### 3. The Prune
Actively remove the unnecessary components.
*   Replace heavy libraries with native language features (e.g., `lodash` -> `Array.map`).
*   Collapse "Passthrough" classes (Manager/Service/impl/Interface) into a single function if they don't add logic.
*   Delete unused config/boilerplate.

### 4. Verification
Does the *bare metal* system still solve the user's Core Problem?
*   If YES: You are done.
*   If NO: Restore only the *minimum* necessary piece.
