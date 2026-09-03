# TASK-001: Clarify Design by Contract lineage

Owner role: Human
Assigned agent: Codex
Proposed by: Codex
Proposed date: 2026-09-03
Approved by: Patrick
Approved date: 2026-09-03
Related contracts: None
Related ADRs: None
Dependencies: None

## Desired outcome

Describe the template as a contract-driven human/AI workflow inspired by
Bertrand Meyer's Design by Contract without implying that its full governance
system is a direct implementation of Meyer's technical method.

## Context

The README already describes the relationship as borrowing DbC's spirit, but the
presentation makes stronger equivalence claims and conflates postconditions with
review, invariants with continuously true conditions, and exceptions with
ambiguity escalation.

## Scope

### Included

- Clarify the presentation title and opening framing.
- Distinguish the DbC-inspired contract discipline from the surrounding
  governance workflow.
- Correct the definitions and process mappings for invariants, postconditions,
  review, and exceptions.
- Align the development-system documentation with this distinction.
- Add an early presentation slide contrasting Meyer's executable software
  contracts with this system's human-readable process contracts.

### Excluded

- Renaming the repository.
- Changing the workflow, roles, lifecycle, or approval authority.
- Adding executable contract enforcement.

## Plan

1. Update the development-system explanation of DbC.
2. Revise the presentation's strongest equivalence claims and mapping table.
3. Check the repository for contradictory DbC wording.

## Acceptance criteria

- [x] The presentation explicitly identifies the system as inspired by DbC.
- [x] The presentation accurately describes invariants and postconditions.
- [x] Review is presented as verification rather than as a postcondition.
- [x] Ambiguity escalation is not presented as the process equivalent of a DbC
      exception.
- [x] Governance features are distinguished from concepts attributed to Meyer.
- [x] An early slide makes the foundational difference in purpose, form, and
      enforcement explicit.

## Validation requirements

- Search all project documentation and presentation text for remaining strong
  equivalence claims.
- Verify that presentation JavaScript remains syntactically valid.

## Risks and assumptions

- The existing repository name remains unchanged and is understood as shorthand
  for the system's inspiration.

## Blocker

None.

## Implementation handoff

Updated the presentation title, origin explanation, governance framing, reframe,
mapping table, and closing attribution. Added an early side-by-side slide that
contrasts Meyer's precise, runtime-checkable software assertions with this
system's mostly human-readable requirements and workflow enforcement. Corrected
the invariant definition, separated behavioral postconditions from independent
review, and removed the exception/ambiguity equivalence. Updated
`docs/AI_DEVELOPMENT_SYSTEM.md` to make the adaptation boundary durable in the
repository documentation.

Validation:

- Searched repository documentation and presentation copy for the superseded
  equivalence claims.
- Parsed every inline presentation script with Node's JavaScript parser.
- Ran `git diff --check`.
- Rendered the new slide at 1600x900 in headless Chromium and visually checked
  its layout, wrapping, and boundaries.

Deviations and assumptions: None beyond retaining the repository's existing name
as required by scope.

Unresolved risks: None identified.

## Review

Not reviewed.

## Human acceptance

Pending.
