---
name: exploring
description: Use for free-form thinking and exploration - a read-only thinking partner that never writes code, uses ASCII diagrams, and follows interesting threads without fixed steps
---

# Exploring

## Overview

A thinking-partner stance for free-form exploration. No fixed steps, no required outputs, no implementation.

**Core principle:** Read, think, diagram, discuss. Never write code.

**Announce at start:** "I'm using the exploring skill — thinking partner mode. I'll read and reason but won't write any code."

## The Stance

### What Exploring IS

- **A conversation**, not a workflow — follow interesting threads
- **Read-only** — may read files, search code, grep, glob, web search. NEVER write, edit, or create files
- **Visual** — use ASCII diagrams liberally to clarify structure, flow, relationships
- **Curious** — ask probing questions, challenge assumptions, surface hidden constraints
- **Divergent** — explore multiple angles before converging on anything

### What Exploring IS NOT

- Not a design session (that's `brainstorming` / `/propose`)
- Not a spec generator (that's `writing-plans`)
- Not debugging (that's `systematic-debugging`)
- Not implementation (that's everything else)

## How It Works

1. **Orient** — Read relevant code, docs, specs, plans. Check `docs/spsa/changes/` for existing context.

2. **Follow threads** — Whatever seems interesting or relevant:
   - "What happens if we...?"
   - "Where does this assumption break down?"
   - "What are we not seeing?"
   - Trace execution paths, map dependencies, surface edge cases

3. **Diagram freely** — ASCII art for:
   ```
   ┌─────────┐     ┌─────────┐
   │ Service A├────►│ Service B│
   └────┬────┘     └─────────┘
        │
        ▼
   ┌─────────┐
   │ Database │
   └─────────┘
   ```
   Data flows, state machines, dependency graphs, sequence diagrams — whatever clarifies thinking.

4. **Surface tensions** — Name tradeoffs explicitly:
   - "This gives us X but costs us Y"
   - "This assumes Z — is that still true?"
   - "These two goals conflict: ..."

5. **Offer transitions** — When ideas crystallize, offer (don't push):
   - "Want me to turn this into a proposal? (`/propose`)"
   - "This looks like a bug worth investigating. (`/debug`)"
   - "Ready to plan implementation? (`/write-plan`)"

## Guardrails

**NEVER during explore mode:**
- Write, edit, or create any files
- Generate implementation code (even "just a sketch")
- Create specs, plans, or tasks
- Commit to a specific solution

**ALWAYS during explore mode:**
- Stay in conversation
- Use diagrams to communicate structure
- Ask more questions than you answer
- Name assumptions and constraints explicitly

## Red Flags

| Thought | Reality |
|---------|---------|
| "Let me just sketch some code" | No. Diagram the idea instead. |
| "I should create a spec for this" | Offer `/propose` transition. Don't create. |
| "This is clear enough to implement" | Ask: "What are we missing?" first. |
| "Let me fix this while I'm here" | Offer `/debug` transition. Don't fix. |

## Integration

**Flows into:**
- **brainstorming** (`/propose`) — When exploration reveals a design worth proposing
- **systematic-debugging** (`/debug`) — When exploration uncovers a bug
- **writing-plans** (`/write-plan`) — When the path forward is clear

**Called standalone** — This skill has no prerequisite. Use it anytime.
