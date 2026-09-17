# TASK-002: Presentation teleprompter

Owner role: Frontend implementation
Assigned agent: Codex
Proposed by: Patrick
Proposed date: 2026-09-17
Approved by: Patrick (direct request to add presentation/index2.html)
Approved date: 2026-09-17
Related contracts: Acceptance criteria below
Related ADRs: None
Dependencies: Existing presentation/Talk Markdown files

## Desired outcome

Read the talk on a laptop with automatic scrolling, speed adjustment, and pause.

## Scope

Add a plain HTML/CSS/JavaScript teleprompter and usage documentation. Load Intro
first, then numbered p files in numeric order. Preserve the slides and talk text.
No external dependencies or changes to the slide presentation.

## Plan

Load the current talk files over HTTP; offer local Markdown selection for file
URLs. Render readable text safely, provide scrolling and navigation controls,
and validate file ordering and implementation syntax.

## Acceptance criteria

- Intro and all current numbered sections appear in numeric order.
- Start/pause and speed adjustment work with buttons and keyboard controls.
- Text size and section navigation are available.
- Loading failures are visible; playback starts only after loading completes.
- Existing presentation and talk files remain unchanged.

## Validation requirements

Check source coverage, JavaScript syntax, and available browser behavior checks.
Document any validation limitations in the handoff.

## Risks and assumptions

Direct file URLs cannot automatically fetch neighboring files in browsers; local
file selection is provided. The default manifest covers the current talk.

## Blocker

None.

## Implementation handoff

Task: TASK-002
Implementer: Codex
Date: 2026-09-17

### Changes made

Added `presentation/index2.html` with automatic scrolling, start/pause, speed
buttons and slider, keyboard shortcuts, text sizing, section navigation,
restart, full screen, and local file selection. HTTP loading reads the current
27 source files; file selection also supports additional numbered sections.
Added `presentation/TELEPROMPTER.md` with usage and maintenance instructions.

### Validation performed

Node parsed the inline JavaScript successfully. A lightweight DOM simulation
verified all 27 source filenames, Intro-first numeric ordering, start/pause,
frame timing, speed bounds, restart, HTML escaping, end-of-talk stop, and loading
failure disabling playback. `git diff --check` passed. Git status confirms only
the three new files; the slide deck and talk sources were not modified.

### Acceptance criteria evidence

Source coverage and ordering were checked against the actual Talk directory.
Playback logic was exercised through the simulated DOM. Controls and readable
loading status are implemented; final visual and browser interaction checks
remain for human review.

### Assumptions and deviations

No third-party repository is needed for this small plain JavaScript page.
Markdown rendering intentionally supports a limited readable subset, documented
in the usage guide. New HTTP-loaded sections require updating the file manifest.

### Unresolved risks

Browser automation packages are unavailable in this workspace. Full-screen,
file-picker, actual layout, and native scrolling have not been browser-tested.

### Documentation updated

`presentation/TELEPROMPTER.md` and this task handoff.

### Requested revision: continuous talk and page navigation

The human requested movement through all files or a combined Markdown file with
page separators. The existing continuous document now has prominent numbered
page separators, Previous/Next page buttons, Left/Right shortcuts, and a page
counter. Navigation tracks the reading position during scrolling and pauses on
jumps. The usage guide explains selecting all files together; no duplicate
combined source is needed. Node DOM-simulation checks passed for numeric order,
separator labels, previous/next navigation, bounds, scroll tracking, pause on
jump, restart, and disabled controls during loading. JavaScript syntax and
`git diff --check` passed. Visual browser validation remains outstanding.

## Review

Not reviewed.

## Human acceptance

Pending.
