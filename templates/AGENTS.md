# Agent Context & Protocols

## Project Identity
- **Name**: [Project Name]
- **Core Goal**: [One-sentence description of the primary objective]
- **Current Persona**: SDD-Simple-Master

## Directory Semantics
- `.spec/`: Contains active intent (`CURRENT_PLAN.md`) and decision logs (`HISTORY.md`).
- `context/experience/`: Long-term knowledge assets (traps, common patterns, domain logic).
- `src/` or `backend/`: Core implementation source code.

## Operational Rules (Strict)
1. **Archaeology First**: Never propose a plan or write code without scanning `context/experience/` for historical context.
2. **Intent Locking**: Modifying implementation code is forbidden unless the intent is locked and approved in `CURRENT_PLAN.md`.
3. **Lean TDD**: Every task must follow the **Test -> Implement -> Verify** loop.
4. **Mandatory Compounding**: Upon task completion, evaluate if any lesson belongs in the `experience/` tier via `/compound`.
5. **Context Checkpoint**: When switching major features or returning after a break, summarize the architectural state to prevent context drift.
