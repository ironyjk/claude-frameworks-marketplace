# Claude Frameworks Marketplace

> Claude Code plugin marketplace for decision-making, investment, real estate, health, learning, software, psychology, parenting, and communication frameworks.

[한국어](README.ko.md) | **English**

---

## Overview

A curated Claude Code plugin marketplace of **160+ evidence-based frameworks** across 9 domains. Each plugin is independently installable with a meta-router pattern that auto-selects the optimal frameworks for your situation.

### Features

- **Academic foundations**: Built on validated theories — Porter, Drucker, Markowitz, Dalio, Ebbinghaus, Bjork, Ericsson, and more
- **Korean context built-in**: ISA (개인종합자산관리계좌), pension savings (연금저축), IRP, health insurance premiums (건보료); jeonse (전세), subscription scoring (청약), HUG; CSAT (수능), civil service exams (공무원), certifications (자격증), and more
- **Meta-router pattern**: Classifies your situation and auto-selects 1–3 frameworks; includes conflict-resolution rules
- **Anti-pattern warnings**: Every framework explicitly states when it is wrong or harmful
- **Bilingual docs**: README.md (English) and README.ko.md (Korean) in each repo

## Installation

```bash
# Add the marketplace
/plugin marketplace add ironyjk/claude-frameworks-marketplace

# Install individual plugins
/plugin install strategy-frameworks@claude-frameworks
/plugin install investment-framework@claude-frameworks
/plugin install real-estate-framework@claude-frameworks
/plugin install software-framework@claude-frameworks
/plugin install health-framework@claude-frameworks
/plugin install learning-framework@claude-frameworks
/plugin install counsel-frameworks@claude-frameworks
/plugin install parenting-frameworks@claude-frameworks
/plugin install howtotalk@claude-frameworks
```

## Short Command Setup (Optional)

After plugin install, commands look like `/strategy-frameworks:think`. To use short names like `/think`, create wrapper files.

**Set up all at once (run in terminal):**

```bash
mkdir -p ~/.claude/commands

for cmd in think money realty code fit learn counsel parenting howtotalk peel; do
  case $cmd in
    think)    plugin="strategy-frameworks" ;;
    money)    plugin="investment-framework" ;;
    realty)   plugin="real-estate-framework" ;;
    code)     plugin="software-framework" ;;
    fit)      plugin="health-framework" ;;
    learn)    plugin="learning-framework" ;;
    counsel)  plugin="counsel-frameworks" ;;
    parenting) plugin="parenting-frameworks" ;;
    howtotalk) plugin="howtotalk" ;;
    peel)     plugin="police-frameworks" ;;
  esac
  cat > ~/.claude/commands/${cmd}.md << EOF
---
description: "Shortcut for /${plugin}:${cmd}"
---
Invoke the skill \`${plugin}:${cmd}\` with these arguments: \$ARGUMENTS
EOF
done

echo "Done! /think, /money, /code, /fit and more are ready"
```

After setup:
- `/think "our company growth strategy"` → auto-selects from 47 strategy frameworks
- `/money "ISA (개인종합자산관리계좌) tax optimization"` → auto-selects from 12 investment frameworks
- `/fit "exercise with a herniated disc"` → auto-selects from 13 health frameworks

## Plugins (9, 160+ sub-frameworks)

### Business & Strategy

| Plugin | Slash | Frameworks | License |
|---|---|---|---|
| **strategy-frameworks** | `/think` | 47 | MIT |

Porter Five Forces, Drucker MBO/5Q, BSC, Blue Ocean, Wardley Mapping, BCG Matrix, BMC, Lean Startup, OKR, Disruptive Innovation, Scenario Planning, Real Options, Game Theory, and more.

### Finance & Assets

| Plugin | Slash | Frameworks | License |
|---|---|---|---|
| **investment-framework** | `/money` | 12 | CC-BY-NC-4.0 |
| **real-estate-framework** | `/realty` | 9 | CC-BY-NC-4.0 |

Investment: MPT, All Weather, Bogleheads, Barbell, Value, Factor, DCA, Rebalancing, Behavioral Biases, Kelly Criterion, Korean Tax Optimization (ISA/연금저축/IRP), Korean FIRE.

Real estate: Hedonic, DiPasquale-Wheaton, Alonso-Muth-Mills, Cap Rate/DCF, Harrison 18.6-Year Cycle, Highest & Best Use, Redevelopment Feasibility, Korean Subscription Points (청약 가점제), Gap Investment (갭투자).

> ⚠️ **Non-commercial use only** (CC BY-NC 4.0). Protects against capital-markets-law / unlicensed advisory liability. Commercial licensing: ironyjk@gmail.com.

### Health · Learning · Software

| Plugin | Slash | Frameworks | License |
|---|---|---|---|
| **health-framework** | `/fit` | 12 | CC-BY-NC-4.0 |
| **learning-framework** | `/learn` | 12 | CC-BY-NC-4.0 |
| **software-framework** | `/code` | 12 | CC-BY-NC-4.0 |

Health: Mediterranean, Low Carb/Keto, Intermittent Fasting, Macro Tracking, Progressive Overload, Strength, Hypertrophy, Polarized Endurance, Sleep, Recovery/Periodization (burnout vs. overtraining distinction), Blood Biomarkers, Body Composition.

Learning: Zettelkasten, PARA, Evergreen Notes, Spaced Repetition, Active Recall, Feynman (with AI feedback workflow), Interleaving, Deliberate Practice, Chunking, Deep Work, Pomodoro, Metalearning.

Software: Scientific Debugging, Bisection, Observability, Hexagonal, DDD, Event Sourcing/CQRS, Modular Monolith, SOLID, 12-Factor, Resilience Patterns, Strangler Fig, Team Topologies.

### Psychology · Parenting · Communication

| Plugin | Slash | Frameworks | License |
|---|---|---|---|
| **counsel-frameworks** | `/counsel` | 14 | MIT |
| **parenting-frameworks** | `/parenting` | 16 | MIT |
| **howtotalk** | `/howtotalk` | 14 | MIT |

Psychology: CBT, ACT, SFBT, MI, IFS, Narrative Therapy, MBSR, MBCT, PPT, REBT, Gottman, DBT Skills, Worden's Grief, PCT.
> ⚠️ For learning and self-reflection only. **Not a substitute for professional therapy.**

Parenting: Positive Discipline, PET, CPS, Emotion Coaching, Triple P, Attachment Parenting, SDT, Retrieval Practice, Growth Mindset, UbD, PBL, Montessori, DAP, UDL, Formative Assessment, Differentiated Instruction.

Communication: NVC, Getting to Yes, Never Split the Difference, Radical Candor, Crucial Conversations, Difficult Conversations, Active Listening, DESC, Influence, Motivational Interviewing, SCARF, Socratic, Storytelling.

## Design Principles

All plugins share the following principles:

1. **No theory copy-paste — translated to Korean context** — Western frameworks re-applied onto Korean institutions and culture
2. **Meta-router pattern** — classifies situation, auto-selects 1–3 frameworks
3. **Anti-pattern warnings** — explicitly states when each framework misleads or causes harm
4. **Scope boundaries explicit** — plugins delegate to each other by role
5. **Decision support, not answer machine** — provides thinking frames, not verdicts
6. **Validity metadata** — `last_verified` and `valid_until` fields, 6–12 month re-verification cadence

## Contributing & Contact

- Bugs, errors, Korean context improvements: open an issue in the relevant plugin repo
- **Commercial licensing / B2B adoption**: ironyjk@gmail.com
- Related repos:
  - [strategy-frameworks](https://github.com/ironyjk/strategy-frameworks)
  - [investment-framework](https://github.com/ironyjk/investment-framework)
  - [real-estate-framework](https://github.com/ironyjk/real-estate-framework)
  - [software-framework](https://github.com/ironyjk/software-framework)
  - [health-framework](https://github.com/ironyjk/health-framework)
  - [learning-framework](https://github.com/ironyjk/learning-framework)
  - [counsel-frameworks](https://github.com/ironyjk/counsel-frameworks)
  - [parenting-frameworks](https://github.com/ironyjk/parenting-frameworks)
  - [howtotalk](https://github.com/ironyjk/howtotalk)

## Licensing

- Marketplace metadata (this repo): MIT
- Each plugin: mixed — Korean-tax/regulation-sensitive domains (investment, real estate, health, learning, software) use CC BY-NC 4.0 to block commercial copying while allowing personal/educational use. Others (strategy, counsel, parenting, communication) use MIT.
- For commercial licensing, enterprise deployment, or framework consulting: ironyjk@gmail.com

---

## Maintainer

**Choi Hee Chul** ([@ironyjk](https://github.com/ironyjk))
CEO of DY Industrial Development · 10+ years in C#/Python · active user of Claude Code as a decision-making platform.

Contact: ironyjk@gmail.com
