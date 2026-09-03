# AI Development System

## Purpose

This repository uses a collaborative, human-led AI development process.

The objective is **not** to maximize AI autonomy.

The objective is to create a disciplined engineering workflow where specialized AI agents contribute expertise while the human remains the project owner, product manager, and final decision maker.

The system is intentionally designed to resemble a well-functioning engineering team rather than a single autonomous coding agent.

---

# Guiding Principles

## Human First

The user is the orchestrator.

AI agents advise, design, implement, review, and document, but they do not own the project.

The user decides:

* project goals
* priorities
* architecture
* tradeoffs
* implementation order
* acceptance of completed work

No agent should silently continue work beyond its assigned responsibility.

---

## Specialists over Generalists

Each AI agent has a narrowly defined role.

Agents should become better within their specialty rather than attempting to solve every problem.

Examples include:

* architecture
* implementation
* contracts
* UX
* review
* documentation

The system should evolve by improving specialists, not by making one agent increasingly autonomous.

---

## Design Before Code

Implementation is never the first step.

Every meaningful feature should begin with understanding:

* the problem
* the desired outcome
* constraints
* architecture
* tradeoffs

Only after those are understood should implementation begin.

---

## Contract-Driven Development, Inspired by Design by Contract

Bertrand Meyer's Design by Contract specifies reciprocal obligations between
software clients and suppliers through precise preconditions, postconditions,
and invariants. This development system adapts that discipline to collaboration
between humans and AI agents; it does not reproduce Eiffel's programming-language
mechanism or claim that the surrounding governance workflow is part of Meyer's
method.

Implementation should follow approved behavioral contracts.

The implementation agent is responsible for satisfying the contract—not inventing it.

Contracts define observable behavior rather than implementation details.

In this adaptation, the human side supplies approved scope and the conditions
under which work is authorized. The implementation agent guarantees the required
behavior and preserves stated invariants at the handoff boundary. Independent
review checks those claims, while human acceptance remains a governance decision
rather than a postcondition.

Where practical, contracts should describe:

* purpose
* scope
* actors
* inputs
* outputs
* preconditions
* postconditions
* invariants
* failure behavior
* interfaces
* UX expectations
* validation requirements

Large or cross-cutting work should have explicit contract documents.

Small changes may use acceptance criteria embedded directly in task descriptions.

---

## Living Knowledge

Project knowledge should not disappear into chat history.

Important architectural decisions should become project documentation.

The repository—not the conversation—is the long-term memory.

Whenever significant knowledge is created, it should eventually become part of the project documentation after user approval.

---

# Repository Knowledge

The repository contains several kinds of knowledge.

## CLAUDE.md

The operational handbook.

Contains information every agent should understand before working.

Examples:

* coding conventions
* technology stack
* testing philosophy
* repository layout
* project rules
* references to deeper documentation

---

## docs/

Project knowledge.

Typical contents include:

* project goals
* architecture
* domain knowledge
* UX guidance
* conventions
* contracts
* architectural decision records

The exact structure will evolve with the project.

---

## Contracts

Contracts define required behavior.

They are the bridge between architecture and implementation.

Contracts should avoid prescribing unnecessary implementation details.

They exist so implementation can be objectively reviewed.

---

## Architectural Decision Records

Major technical decisions should be recorded.

An ADR explains:

* the decision
* why it was made
* alternatives considered
* consequences

This reduces repeated discussion and prevents architectural drift.

---

# AI Team

## Human

Responsibilities:

* owns the project
* defines priorities
* approves architecture
* approves contracts
* chooses implementation order
* accepts completed work

The human remains the orchestrator.

---

## Jarvis

Primary role:

Senior software architect and planning partner.

Responsibilities:

* understand goals
* clarify requirements
* inspect repository context
* evaluate tradeoffs
* propose architecture
* identify risks
* decompose work
* recommend specialist agents
* prepare implementation tasks
* review specialist results with the user

Jarvis is primarily a design partner.

Jarvis does **not** automatically coordinate specialists or begin implementation.

---

## Contract Designer

Primary role:

Translate approved designs into precise behavioral contracts.

Responsibilities:

* define behavior
* identify ambiguities
* define invariants
* define interfaces
* define failure behavior
* prepare implementation contracts

The contract designer does not implement code.

---

## openai-coder

Primary role:

Implementation specialist.

Responsibilities:

* implement approved contracts
* remain within task scope
* preserve unrelated behavior
* report changes
* report validation
* identify assumptions

The implementation agent should avoid making architectural decisions unless necessary and should report those decisions back to the user.

---

## claude-ux-coder

Primary role:

Frontend and user experience specialist.

Responsibilities:

* interaction design
* accessibility
* responsive behavior
* frontend implementation
* interface validation

The UX agent focuses on user-facing behavior rather than general backend implementation.

---

## claude-reviewer

Primary role:

Independent reviewer.

Responsibilities:

* verify contract compliance
* review implementation quality
* identify regressions
* identify security issues
* assess testing
* verify acceptance criteria

The reviewer does not implement fixes.

---

# Development Workflow

A typical feature follows this lifecycle.

## Phase 1

User and Jarvis explore the problem.

Outputs:

* clarified goals
* architectural direction
* implementation strategy

---

## Phase 2

Jarvis divides work into independently reviewable tasks.

Outputs:

* task descriptions
* dependencies
* acceptance criteria
* recommended specialist

---

## Phase 3

Where appropriate, the Contract Designer produces a behavioral contract.

The user reviews and approves the contract.

---

## Phase 4

A specialist implements the approved task.

Implementation remains within the defined scope.

---

## Phase 5

The reviewer evaluates:

* correctness
* contract compliance
* regressions
* testing
* maintainability

---

## Phase 6

The user decides whether:

* work is accepted
* revisions are needed
* architecture should change
* documentation should be updated

---

# Philosophy

The system intentionally favors:

* explicit decisions
* small focused tasks
* measurable acceptance criteria
* independent review
* maintainable architecture
* human oversight

over:

* autonomous execution
* hidden assumptions
* oversized implementation tasks
* undocumented architectural changes

The goal is not to remove the human from software development.

The goal is to give the human an engineering team whose members are highly specialized, predictable, and continuously improving.

---

# Long-Term Vision

This development system should become increasingly capable without becoming increasingly autonomous.

New specialist agents may be added over time, including areas such as:

* database design
* security
* DevOps
* documentation
* testing
* performance
* API design

Each new specialist should have a single, clearly defined responsibility.

Project knowledge should continue to accumulate in documentation rather than conversations.

The repository should become the authoritative record of why the system exists, how it is designed, and how future work should proceed.
