---
name: map-vs-territory
description: Empiricism and Reality Checking. Prioritizing runtime truth over documentation.
license: MIT
---

# Map vs. Territory (The Reality Check)

> "The map is not the territory." - Alfred Korzybski

## When to Use
*   **Debugging:** When "it should work" but doesn't.
*   **Integration:** When using 3rd party APIs or libraries.
*   **Legacy Code:** When comments don't match the code.

## The Protocol: The Reality Check
Do not trust the Map (Docs, Comments, Variable Names).
Trust the Territory (Logs, Memory, Disk, Network).

### 1. The Doubt
Identify the "Map" you are relying on.
*   *"The comment says this function returns a User."*
*   *"The variable is named `isValid`."*
*   *"The API docs say it returns 200 OK."*

### 2. The Probe
Active verify the Territory. DO NOT READ CODE. **RUN CODE.**
*   *Action:* `print(type(user))` -> Is it actually a User object? or a Dict? or None?
*   *Action:* `console.log(isValid)` -> Is it `true`? `1`? `"true"`?
*   *Action:* Inspect the raw HTTP body.

### 3. The Update
If Map $\neq$ Territory, **The Map is Wrong.**
*   Update the docs/comments.
*   Rename the variable (`isValid` -> `shouldBeValid`).
*   Fix the mental model.
