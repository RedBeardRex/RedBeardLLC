# AI Workflow Protocol v1.1

This file governs AI/Codex workflow mechanics for this repository. README.md remains authoritative for current product/task state.

## Global Engineering Policy

### GEP-001 — Codex Cost & Escalation Policy
**Scope:** GLOBAL  
**Strength:** MUST

- Every ChatGPT-to-Codex handoff MUST state the recommended Codex model and reasoning/effort level.
- Default implementation tier is **GPT-5.6 Terra / Medium** (or the current successor balanced-cost tier) unless the task clearly warrants another tier.
- Clearly routine, low-risk, mechanical work SHOULD use **Luna** or the lowest-cost capable tier when practical.
- Escalation to **Sol / High** or an equivalent higher-cost tier MUST be justified explicitly by architecture risk, difficult debugging, security-sensitive work, destructive migrations, or comparable complexity.
- **Astra, Max, Ultra, Extra-High, Pro, or any equivalent frontier/high-cost mode MUST NOT be used without Jeff's explicit approval.**
- Do not silently self-escalate compute. If the current tier appears insufficient, stop at a safe checkpoint, preserve state, explain why escalation is warranted, and request approval.
- Cost control MUST NOT weaken required security, testing, release acceptance, secret handling, or destructive-action safeguards.
- Project- or task-level instructions MAY be stricter but MUST NOT weaken this policy unless Jeff explicitly overrides GEP-001.

### GEP-002 — Handshake Compliance & Recovery Policy
**Scope:** GLOBAL for ChatGPT-Codex coordinated projects  
**Strength:** MUST

- Every meaningful ownership transfer between ChatGPT and Codex MUST use the checkpoint-based handshake protocol.
- The repository's live handshake/state is authoritative over conversation memory.
- Both sides MUST verify handshake compliance before acting on a transfer of ownership.
- The standard cross-interface verification phrase is **`CHECK HANDSHAKE`**.
- On `CHECK HANDSHAKE`, read the authoritative repository state, verify Protocol Version, Handshake ID, Current Owner, State, Task ID, Last Completed Action, Next Required Action, and Blockers, reconcile stale conversation state, and report the authoritative state before new implementation begins.
- If the handshake is missing, malformed, contradictory, or stale, repair it when the correction is unambiguous and authorized; otherwise stop and report the mismatch instead of guessing.
- If Current Owner is not the receiving side, that side MUST NOT begin implementation until the live repository state is reconciled.
- Routine implementation inside an already-authorized task does not require repeated micro-handshakes. Handshakes are for meaningful ownership changes, completion checkpoints, and exception boundaries.
- Project-level rules MAY be stricter but MUST NOT weaken GEP-002 unless Jeff explicitly overrides it.

Use RFC-style terms consistently: **MUST** = mandatory, **SHOULD** = default unless there is a documented reason to deviate, **MAY** = optional.

## Resume behavior
Read the current project state first, then only the files needed for the next action. Do not reread historical completion reports or unrelated architecture unless required.

## Lean handshake
Use: Protocol 1.1, Handshake, Owner, State, Task, concise Last, concise Next, Blockers, task-spec path, and latest report/evidence path when useful. Do not duplicate full task specs, acceptance criteria, history, or long test reports in the live handshake.

Use ownership handoffs for meaningful ownership changes, not every tiny provider/browser/approval pause where the same task can safely resume afterward. Never bypass genuine authorization or safety boundaries.

## Cost-aware execution
- Batch related work into one bounded task when practical.
- Prefer targeted reads/searches over repository-wide rereads.
- Keep chat reports concise; durable detail belongs in repo files.
- Avoid repeating unchanged architecture or constraints.
- Use the least expensive capable model/reasoning tier for routine work; escalate only when justified and subject to GEP-001.

## Testing tiers
1. Micro/config/docs: targeted validation.
2. Feature iteration: affected subsystem tests plus build/typecheck as appropriate.
3. Feature/milestone handoff: full relevant regression suite.
4. Release/security milestone: full regression plus required security/browser/production acceptance.

## Completion format
Default chat handoff: DONE; RESULT; TESTS; EXCEPTIONS/BLOCKERS; COMMIT; NEXT.

## Safety and quality
Do not trade away security, release acceptance, secret handling, destructive-action confirmation, or final regression quality to save tokens.
