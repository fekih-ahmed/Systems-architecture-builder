# Systems-architecture-builder

> A structured Six-File Context Methodology for AI-assisted systems architecture building.

---

## What is this?

A set of templates and a workflow that gives AI coding agents the structured context they need to build consistently — without drift, without guessing, and without breaking things between sessions.

---

## The Six Context Files

```
templates/context/
├── project-overview.md     ← What you're building and why
├── architecture.md         ← Stack, boundaries, and invariants
├── code-standards.md       ← Conventions and patterns
├── ai-workflow-rules.md    ← How the agent should behave
├── ui-context.md           ← Colors, typography, and design tokens
└── progress-tracker.md     ← Current state and session notes
```

---

## How to Use

1. Copy `templates/` into your project root and rename it `context/`
2. Fill in each file using the prompts in the guide
3. Add `CLAUDE.md` (or `AGENTS.md`) to your project root
4. Start every session with: *"Read the entry file and resume."*

---

## Entry Point Template (`CLAUDE.md`)

```markdown
## Application Building Context

Read the following files in order before implementing anything:

1. `context/project-overview.md`
2. `context/architecture.md`
3. `context/ui-context.md`
4. `context/code-standards.md`
5. `context/ai-workflow-rules.md`
6. `context/progress-tracker.md`

Update `context/progress-tracker.md` after each meaningful change.
```

---

## The Three-Prompt Build Workflow

**Implement:**
```
Read context/specs/NN-feature-name.md. Implement it exactly as specified. Do not go beyond scope.
```

**Correct:**
```
The [element] does not match the spec. Expected: [X]. Current: [Y]. Fix only this.
```

**Close:**
```
Mark unit NN complete in context/progress-tracker.md. Push branch feat/NN-feature-name.
```

---

_Built with the Six-File Context System · 2026_
