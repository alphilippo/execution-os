# execution-os

![Version](https://img.shields.io/badge/version-1.0.0-blue) ![License](https://img.shields.io/badge/license-Apache%202.0-green) ![Claude](https://img.shields.io/badge/Claude-Skill-purple)

🌍 **[Français](README.md)** · **English**

> A personal execution system for Claude: turns intent into results, with 4 modular modules (sprint planning, deep work, weekly ritual, accountability).

## What it does

Most people confuse planning with execution. They build to-do lists that never get finished. `execution-os` applies 4 hard principles:

1. **A sprint has a single promise** — not 10 goals, ONE central deliverable
2. **Time is the constraint, not the task** — you allocate blocks, not intentions
3. **The retro beats the plan** — the weekly ritual matters more than the beauty of the initial planning
4. **Accountability is brutal but fair** — no sugar-coating when you drift

## The 4 modules

| Module | When to use it |
|---|---|
| **Sprint Planner** | Start a 1-2 week sprint, new project, new quarter |
| **Deep Work Designer** | When you have 2-4h ahead and a big topic to move forward |
| **Weekly Ritual** | Sunday evening / Monday morning, retro + weekly plan |
| **Accountability Check** | When you drift, procrastinate, or question your commitments |

## Triggers

The skill triggers automatically when you say:
- *"Plan my week / my sprint"* → Sprint Planner
- *"I have 3h ahead, what should I do"* → Deep Work Designer
- *"I'm doing my retro"*, *"Sunday evening"* → Weekly Ritual
- *"I'm drifting"*, *"I'm procrastinating on X"*, *"I can't stick to my plan"* → Accountability Check

## Complementary skills (full ecosystem)

- 🧠 [**thinking-os**](https://github.com/alphilippo/thinking-os) — cognitive router that applies the right thinking framework
- 📚 [**learning-os**](https://github.com/alphilippo/learning-os) — learning system with 5 modules

The 3 compose:
- `thinking-os` answers **WHAT** to do (decisions, trade-offs, diagnostics)
- `execution-os` answers **HOW** to do it (sprints, deep work, rituals)
- `learning-os` answers **HOW TO LEARN** it (plans, concepts, sessions, synthesis)

If you're unsure what to execute → `thinking-os`.
If you know what but you drift → `execution-os`.
If you want to learn/master a domain → `learning-os`.

## Installation

### Claude.ai

1. Download or clone this folder
2. Upload to `/mnt/skills/user/execution-os/`
3. The skill triggers automatically on matching prompts

### Claude Code

```bash
cp -r execution-os ~/.claude/skills/
```

### Claude API

Package as `.skill` and upload via the `/skills` endpoint.

## Examples

### Sprint planning
> *"I'm launching cohort 2 of my program in 3 weeks — I need to finish the curriculum, recruit 10 mentors, validate 15 startups."*

→ The skill **refuses** the 4 deliverables, forces picking ONE (the 15 startups), produces a calendarized plan with a protected Thursday buffer.

### Deep work
> *"I have 3h ahead of me. I want to move forward on my commercial strategy."*

→ The skill forces an observable deliverable (*"2-page doc, 3 options compared"*), breaks it into 45-50 min blocks with breaks, enforces the wrap-up.

### Weekly ritual
> *"This week's review: I didn't finish my main deliverable but I did a lot of other stuff."*

→ The skill **refuses** the "but", quantifies the delivery rate against the central promise (0%), identifies the avoidance pattern, produces a plan attacking that pattern.

### Accountability
> *"It's been 3 weeks that I've been saying I'll write a book. I haven't written anything. Maybe it's not the right moment?"*

→ The skill **refuses** the escape, asks the 4 hard questions, distinguishes obstacle from internal resistance, produces a clear decision (either re-engage at 30% scope, or explicit clean abandon).

## Structure

```
execution-os/
├── SKILL.md                            # Metadata + router
├── README.md                           # French version
├── README.en.md                        # This file
├── modules/
│   ├── sprint-planner.md
│   ├── deep-work-designer.md
│   ├── weekly-ritual.md
│   └── accountability-check.md
├── templates/                          # Reusable markdown templates
│   ├── sprint-plan-template.md
│   ├── weekly-ritual-template.md
│   └── deep-work-template.md
├── examples/                           # End-to-end examples
│   ├── sprint-example.md
│   ├── weekly-example.md
│   └── accountability-example.md
└── tests/
    └── test-cases.md                   # 11 validation cases
```

## Philosophy

- **Progressive disclosure**: the SKILL.md only contains the router. Each module is loaded on demand.
- **No free motivation**: no *"you can do it!"*, no coach quotes.
- **Reality priority**: no over-optimization — a livable plan beats a perfect one.
- **Safety rule**: if the user shows signs of burnout / exhaustion / distress, the skill stops and redirects to a real human support.

## Limitations

- Does not replace a therapist, a human coach, or a doctor
- No gamification (no points, no streaks)
- Time estimates remain estimates — the skill isn't magic
- Not a good fit for tasks under 15 min (overhead > value)

> **Note**: Content in French (modules, templates, examples) is currently the reference version. An English translation of module bodies is on the roadmap.

## Roadmap

- **v1.0** (current): 4 modules + 3 templates + routing
- **v1.1**: **Monthly ritual** (retro + plan at the monthly scale)
- **v1.2**: **Energy tracking** (correlation energy / task types)
- **v1.3**: **Explicit composition** with `thinking-os` (automatic redirection)
- **v2.0**: **Memory of past sprints** to improve future estimates

## License

Apache 2.0 — fork, adapt, republish.

## Credits

Built with Claude as Skill Architect. Inspired by the Cal Newport tradition (deep work), Eisenhower (prioritization), Ray Dalio (principles), and Agile sprint practice.
