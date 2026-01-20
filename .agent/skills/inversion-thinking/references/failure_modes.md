# failure_modes.md - The Saboteur's Cheat Sheet

Use these categories to find weak points in the system.

## 1. Entropy (Natural Decay)
*   **Race Conditions:** What happens if two requests happen at the exact same microsecond?
*   **Timeouts:** What if the database takes 30 seconds to respond?
*   **Data Corruption:** What if the JSON is malformed or cut off?
*   **Resource Exhaustion:** What if the disk is full? What if memory is 100%?

## 2. Malice (The Attacker)
*   **Injection:** SQL, XSS, Command Injection. Can I execute code?
*   **Privilege Escalation:** Can I access data I shouldn't own? IDOR?
*   **Replay Attacks:** Can I send the same "pay" request 10 times?
*   **Denial of Service:** Can I lock the resource for everyone else?

## 3. Ignorance (The User)
*   **Bad Input:** Nulls, emojis, massive strings, negative numbers.
*   **Misunderstanding:** What if the user clicks "Back" during a transaction?
*   **Legacy Data:** What if old data doesn't match the new schema?

## 4. Scale (The Crowd)
*   **Thundering Herd:** What if 10,000 users retry at once?
*   **Latency Spikes:** What if the network adds 500ms jitter?
*   **Connection Limits:** What if we run out of DB connections?
