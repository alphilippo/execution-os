# Changelog — execution-os

All notable changes to this project are documented here.

Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
This project adheres to [Semantic Versioning](https://semver.org/).

## [1.0.0] — 2026-04-21

### Initial release

First public release of `execution-os` — a personal execution system skill for Claude that turns intent into results, with 4 modular modules.

### Added

#### Core routing system
- `SKILL.md` with module router and linguistic signature triggers
- Composition principle with `thinking-os` (WHAT vs. HOW separation)

#### 4 execution modules
- `sprint-planner` — plan a 1-2 week sprint with a single central deliverable, 70% time budget, Thursday buffer, risk mitigation
- `deep-work-designer` — structure 2-4h sessions with obstacle identification, 45-50 min blocks + breaks, mandatory wrap-up
- `weekly-ritual` — retro-before-plan ritual with factual delivery rate, 3 honest questions, energy diagnostic, max 3 secondary goals + 2 explicit "no"s
- `accountability-check` — 4-question protocol distinguishing real obstacles from internal resistance, with 3 decision outputs (re-engage at 30%, explicit abandon, or investigation)

#### Templates (reusable markdown)
- Sprint plan template
- Weekly ritual template
- Deep work session template

#### Documentation & validation
- End-to-end examples for sprint planning, weekly ritual, and accountability cases
- 11 test cases with expected module routing + red flags
- Apache 2.0 license
- CONTRIBUTING.md guide for new modules and improvements

### Design principles enforced
- One central promise per sprint (refuses to accept multiple goals)
- Time is the constraint, not the task (allocate blocks, not intentions)
- Retro beats plan (retro always precedes planning)
- No motivational fluff, no gamification, no points/streaks
- Safety rule: if user shows burnout signs, module stops and redirects to human support

### Known limitations in v1.0
- Trigger descriptions are French-first
- Module content is French-only (English translation on roadmap)
- No memory of past sprints for estimation calibration (planned v2.0)
- No explicit auto-redirect to `thinking-os` when the problem is a decision, not execution (planned v1.3)

### Tested on
- Claude Opus 4.7
- Claude Sonnet 4.6

---

## [Unreleased]

### Planned for v1.1
- Monthly ritual (retro + plan at monthly scale)

### Planned for v1.2
- Energy tracking (correlation energy / task types)

### Planned for v1.3
- Explicit composition with `thinking-os` (automatic redirection when problem is a decision)

### Planned for v2.0
- Memory of past sprints to improve future time estimates
