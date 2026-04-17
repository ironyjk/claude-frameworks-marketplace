# Claude Frameworks Marketplace

> 의사결정·투자·부동산·건강·학습·개발·심리·양육·소통 9개 프레임워크 묶음.
> Claude Code plugin marketplace for decision-making, investment, real estate, health, learning, software, psychology, parenting, and communication frameworks.

[한국어](#korean) | [English](#english)

---

## Korean

### 개요

이 마켓플레이스는 **160+ 검증된 프레임워크**를 Claude Code 플러그인으로 제공합니다. 각 플러그인은 독립적으로 설치 가능하며, 메타 라우터 방식으로 상황에 맞는 프레임워크를 자동 선택합니다.

### 특징

- **학술 근거**: Porter·Drucker·Markowitz·Dalio·Ebbinghaus·Bjork·Ericsson 같은 검증된 이론 기반
- **한국 맥락 내장**: ISA·연금저축·IRP·건보료, 전세·청약·HUG, 수능·공무원·자격증 등
- **메타 라우터**: 상황을 분류해 1~3개 프레임워크 자동 선택, 충돌 해소 규칙 포함
- **과적용 경고**: 각 프레임워크가 틀리거나 해로울 때를 명시
- **한영 문서**: README.ko.md와 README.md 병행 제공

### 설치

```bash
# Claude Code에서 마켓플레이스 추가
/plugin marketplace add ironyjk/claude-frameworks-marketplace

# 원하는 플러그인만 설치
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

### 짧은 이름으로 쓰기 (Optional)

플러그인으로 설치하면 `/strategy-frameworks:think`처럼 긴 이름이 됩니다. `/think`처럼 짧게 쓰고 싶다면 래퍼 파일을 만드세요.

**한 번에 전부 설정 (터미널에서 실행):**

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

echo "Done! /think, /money, /code, /fit 등 짧은 이름 사용 가능"
```

설정 후 사용:
- `/think "우리 회사 성장 전략"` → strategy-frameworks의 47개 프레임 중 자동 선택
- `/money "ISA 절세 전략"` → investment-framework의 12개 프레임 중 자동 선택
- `/fit "디스크 있는데 운동법"` → health-framework의 13개 프레임 중 자동 선택

### 포함 플러그인 (9개, 160+ 하위 프레임)

#### 전략·비즈니스

| 플러그인 | 슬래시 | 프레임 수 | 라이선스 |
|---|---|---|---|
| **strategy-frameworks** | `/think` | 47 | MIT |

Porter Five Forces, Drucker MBO/5Q, BSC, Blue Ocean, Wardley Mapping, BCG Matrix, BMC, Lean Startup, OKR, Disruptive Innovation, Scenario Planning, Real Options, Game Theory 등.

#### 재무·자산

| 플러그인 | 슬래시 | 프레임 수 | 라이선스 |
|---|---|---|---|
| **investment-framework** | `/money` | 12 | CC-BY-NC-4.0 |
| **real-estate-framework** | `/realty` | 9 | CC-BY-NC-4.0 |

투자: MPT, All Weather, Bogleheads, Barbell, Value, Factor, DCA, Rebalancing, Behavioral Biases, Kelly Criterion, Korean Tax Optimization, Korean FIRE.

부동산: Hedonic, DiPasquale-Wheaton, Alonso-Muth-Mills, Cap Rate/DCF, Harrison 18.6-Year Cycle, Highest & Best Use, Redevelopment Feasibility, Korean Subscription Points, Gap Investment.

> ⚠️ **상업 이용 금지** (CC BY-NC 4.0). 자본시장법·유사투자자문업 이슈 방어. 상업 라이선스는 ironyjk@gmail.com 문의.

#### 건강·학습·개발

| 플러그인 | 슬래시 | 프레임 수 | 라이선스 |
|---|---|---|---|
| **health-framework** | `/fit` | 12 | CC-BY-NC-4.0 |
| **learning-framework** | `/learn` | 12 | CC-BY-NC-4.0 |
| **software-framework** | `/code` | 12 | CC-BY-NC-4.0 |

건강: Mediterranean, Low Carb/Keto, Intermittent Fasting, Macro Tracking, Progressive Overload, Strength, Hypertrophy, Polarized Endurance, Sleep, Recovery/Periodization (번아웃·과훈련 구분 포함), Blood Biomarkers, Body Composition.

학습: Zettelkasten, PARA, Evergreen Notes, Spaced Repetition, Active Recall, Feynman (AI 피드백 워크플로 포함), Interleaving, Deliberate Practice, Chunking, Deep Work, Pomodoro, Metalearning.

개발: Scientific Debugging, Bisection, Observability, Hexagonal, DDD, Event Sourcing/CQRS, Modular Monolith, SOLID, 12-Factor, Resilience Patterns, Strangler Fig, Team Topologies.

#### 심리·양육·소통

| 플러그인 | 슬래시 | 프레임 수 | 라이선스 |
|---|---|---|---|
| **counsel-frameworks** | `/counsel` | 14 | MIT |
| **parenting-frameworks** | `/parenting` | 16 | MIT |
| **howtotalk** | `/howtotalk` | 14 | MIT |

심리: CBT, ACT, SFBT, MI, IFS, Narrative Therapy, MBSR, MBCT, PPT, REBT, Gottman, DBT Skills, Worden's Grief, PCT.
> ⚠️ 학습·자기 성찰 도구로만. **전문 치료 대체 아님**.

양육: Positive Discipline, PET, CPS, Emotion Coaching, Triple P, Attachment Parenting, SDT, Retrieval Practice, Growth Mindset, UbD, PBL, Montessori, DAP, UDL, Formative Assessment, Differentiated Instruction.

소통: NVC, Getting to Yes, Never Split the Difference, Radical Candor, Crucial Conversations, Difficult Conversations, Active Listening, DESC, Influence, Motivational Interviewing, SCARF, Socratic, Storytelling.

### 설계 원칙

모든 플러그인은 다음 원칙을 공유합니다:

1. **이론 복붙 금지, 한국 맥락으로 번역** — 영미권 프레임을 한국 제도·문화 위에 재적용
2. **메타 라우터 구조** — 상황을 분류하고 1~3개 프레임워크를 자동 선택
3. **과적용 경고 포함** — 각 프레임워크가 틀리거나 해로울 때를 명시
4. **범위 바깥 명시** — 다른 플러그인과 역할 분담
5. **의사결정 보조** — 정답 자판기가 아니라 사고 프레임 제공
6. **유효기간 메타** — `last_verified`, `valid_until` 필드로 6~12개월 주기 재검증

### 기여·문의

- 버그·오류·한국 맥락 보강: 각 플러그인 리포에 이슈 등록
- **상업 라이선스·B2B 도입**: ironyjk@gmail.com
- 관련 리포들:
  - [strategy-frameworks](https://github.com/ironyjk/strategy-frameworks)
  - [investment-framework](https://github.com/ironyjk/investment-framework)
  - [real-estate-framework](https://github.com/ironyjk/real-estate-framework)
  - [software-framework](https://github.com/ironyjk/software-framework)
  - [health-framework](https://github.com/ironyjk/health-framework)
  - [learning-framework](https://github.com/ironyjk/learning-framework)
  - [counsel-frameworks](https://github.com/ironyjk/counsel-frameworks)
  - [parenting-frameworks](https://github.com/ironyjk/parenting-frameworks)
  - [howtotalk](https://github.com/ironyjk/howtotalk)

### 라이선스

- 마켓플레이스 메타데이터(이 리포): MIT
- 각 플러그인: 상단 표 참조 — 대부분 MIT, 금융·부동산·건강·학습·개발은 CC-BY-NC-4.0

---

## English

### Overview

A curated Claude Code plugin marketplace of **160+ evidence-based frameworks** across 9 domains. Each plugin is independently installable with a meta-router pattern auto-selecting the optimal frameworks.

### Installation

```bash
# Add the marketplace
/plugin marketplace add ironyjk/claude-frameworks-marketplace

# Install individual plugins
/plugin install strategy-frameworks@claude-frameworks
# ... (see Korean section for full list)
```

### Short Command Setup (Optional)

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
- `/money "ISA tax optimization"` → auto-selects from 12 investment frameworks
- `/fit "exercise with a herniated disc"` → auto-selects from 13 health frameworks

### Plugins (9, 160+ sub-frameworks)

**Business & Strategy**: `strategy-frameworks` (/think, 47)
**Finance**: `investment-framework` (/money, 12), `real-estate-framework` (/realty, 9)
**Health · Learning · Software**: `health-framework` (/fit, 12), `learning-framework` (/learn, 12), `software-framework` (/code, 12)
**Psychology · Parenting · Communication**: `counsel-frameworks` (/counsel, 14), `parenting-frameworks` (/parenting, 16), `howtotalk` (/howtotalk, 14)

### Design Principles

1. **No theory copy-paste** — adapted to Korean context (law, culture, market)
2. **Meta-router pattern** — auto-selects 1–3 relevant frameworks
3. **Anti-pattern warnings** — explicit notes on when each framework misleads
4. **Scope boundaries** — plugins explicitly delegate to one another
5. **Decision support, not answer machine** — provides thinking frames, not verdicts
6. **Meta validity dates** — `last_verified` and `valid_until` metadata, 6–12 month re-verification cadence

### Licensing

- Marketplace metadata (this repo): MIT
- Each plugin: mixed — Korean-tax/regulation-sensitive domains (investment, real estate, health, learning, software) use CC BY-NC 4.0 to block commercial copying while allowing personal/educational use. Others (strategy, counsel, parenting, communication) use MIT.
- For commercial licensing, enterprise deployment, or framework consulting: ironyjk@gmail.com

---

## Maintainer

**Choi Hee Chul** ([@ironyjk](https://github.com/ironyjk))
CEO of DY Industrial Development · 10+ years in C#/Python · active user of Claude Code as a decision-making platform.

Contact: ironyjk@gmail.com
