# Project Template

A repository template for human-led software development with specialized AI
agents, explicit approval gates, behavioral contracts, and independent review.

Start with `CLAUDE.md`, then read `AGENTS.md` and
`docs/AI_DEVELOPMENT_SYSTEM.md`.

Active work is tracked through plan files in `tasks/`. The directory containing a
task is its authoritative workflow state.

## Presentation

A slide deck introducing this system — [`presentation/index.html`](presentation/index.html) —
is available live at
[mrdatawolf.github.io/PROJECT-TEMPLATE-DBC/presentation/](https://mrdatawolf.github.io/PROJECT-TEMPLATE-DBC/presentation/)
once GitHub Pages is enabled for this repo (Settings → Pages → deploy from the
`main` branch). It also runs standalone by opening the file directly in any
browser, no server required.

## Origin of Design by Contract

The "DbC" in this template's name refers to Design by Contract, a methodology
originated by Bertrand Meyer in the 1980s and first realized in the Eiffel
programming language. It formalizes software correctness through preconditions,
postconditions, and invariants — obligations and guarantees shared between a
component and its callers. This template borrows the spirit of that discipline
(explicit obligations, verifiable behavior, clear responsibility boundaries) and
applies it to the human/agent development process itself.

Further reading: Bertrand Meyer, *Object-Oriented Software Construction*
(Prentice Hall, 1988; 2nd ed. 1997).
