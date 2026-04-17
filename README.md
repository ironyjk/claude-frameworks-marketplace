# Claude Frameworks Marketplace

> 의사결정·커뮤니케이션·학문 프레임워크 6종 묶음. Claude Code 플러그인으로 제공.
> Decision-making, communication, and academic frameworks as Claude Code plugins.

[한국어](#korean) | [English](#english)

---

## Korean

### 개요

이 마켓플레이스는 **130+ 검증된 프레임워크**를 Claude Code 슬래시 명령으로 제공합니다. 각 플러그인은 독립적으로 설치 가능하며, 메타 라우터 방식으로 상황에 맞는 프레임워크를 자동 선택합니다.

### 설치

```bash
# Claude Code에서 마켓플레이스 추가
/plugin marketplace add ironyjk/claude-frameworks-marketplace

# 원하는 플러그인만 설치
/plugin install strategy-frameworks@claude-frameworks
/plugin install counsel-frameworks@claude-frameworks
/plugin install parenting-frameworks@claude-frameworks
/plugin install howtotalk@claude-frameworks
/plugin install triz-agents@claude-frameworks
/plugin install toc-agents@claude-frameworks
```

### 포함 플러그인

| 플러그인 | 슬래시 명령 | 설명 | 프레임워크 수 |
|---|---|---|---|
| **strategy-frameworks** | `/think` | Porter·Drucker·Wardley·Blue Ocean 등 경영전략 메타 라우터 | 47 |
| **counsel-frameworks** | `/counsel` | CBT·ACT·IFS·Gottman 등 심리상담 프레임 (전문가 치료 대체 아님) | 14 |
| **parenting-frameworks** | `/parenting` | Positive Discipline·PET·Montessori 등 양육·교육 프레임 | 16 |
| **howtotalk** | `/howtotalk` | NVC·Getting to Yes·Radical Candor 등 소통·협상 프레임 | 20+ |
| **triz-agents** | `/triz` | TRIZ — 40 원리·모순 매트릭스·IFR·ARIZ | 10+ |
| **toc-agents** | `/toc` | TOC — CRT·EC·FRT·Five Focusing Steps·DBR·CCPM | 11 |

### 설계 원칙

모든 플러그인은 다음 원칙을 공유합니다:

1. **이론 복붙 금지, 한국 맥락으로 번역** — 영미권 프레임을 한국 제도·문화 위에 재적용
2. **메타 라우터 구조** — 상황을 분류하고 1~3개 프레임워크를 자동 선택
3. **과적용 경고 포함** — 각 프레임워크가 틀리거나 해로울 때를 명시
4. **범위 바깥 명시** — 다른 플러그인과 역할 분담
5. **의사결정 보조** — 정답 자판기가 아니라 사고 프레임 제공

### 기여

버그·오류·한국 맥락 보강 제안은 각 플러그인 리포에 이슈 등록:
- [strategy-frameworks](https://github.com/ironyjk/strategy-frameworks)
- [counsel-frameworks](https://github.com/ironyjk/counsel-frameworks)
- [parenting-frameworks](https://github.com/ironyjk/parenting-frameworks)
- [howtotalk](https://github.com/ironyjk/howtotalk)
- [triz-agents](https://github.com/ironyjk/triz-agents)
- [toc-agents](https://github.com/ironyjk/toc-agents)

### 라이선스

- 마켓플레이스 메타데이터(이 리포): MIT
- 각 플러그인 콘텐츠: 각 플러그인 리포의 LICENSE 파일 참조 (대부분 MIT)

---

## English

### Overview

A curated marketplace of **130+ evidence-based frameworks** delivered as Claude Code plugins. Each plugin is independently installable and uses a meta-router pattern to auto-select the optimal framework(s) for your situation.

### Installation

```bash
# Add the marketplace
/plugin marketplace add ironyjk/claude-frameworks-marketplace

# Install individual plugins
/plugin install strategy-frameworks@claude-frameworks
# ... etc
```

### Plugins

| Plugin | Slash Command | Description | Framework Count |
|---|---|---|---|
| **strategy-frameworks** | `/think` | Business strategy meta-router (Porter, Drucker, Wardley, Blue Ocean, BMC, etc.) | 47 |
| **counsel-frameworks** | `/counsel` | Psychology frameworks (CBT, ACT, IFS, Gottman). **Not a replacement for therapy.** | 14 |
| **parenting-frameworks** | `/parenting` | Parenting & education (Positive Discipline, PET, Montessori, UbD, PBL) | 16 |
| **howtotalk** | `/howtotalk` | Communication & negotiation (NVC, Getting to Yes, Radical Candor) | 20+ |
| **triz-agents** | `/triz` | Systematic innovation (40 Principles, Contradiction Matrix, ARIZ) | 10+ |
| **toc-agents** | `/toc` | Theory of Constraints (CRT, EC, FRT, Five Focusing Steps, CCPM) | 11 |

### Design Principles

1. **No theory copy-paste** — frameworks are adapted to Korean context (law, culture, market)
2. **Meta-router pattern** — classifies the situation and auto-selects 1–3 relevant frameworks
3. **Anti-pattern warnings** — explicit notes on when each framework misleads
4. **Scope boundaries** — plugins explicitly delegate to one another
5. **Decision support, not answer machine** — provides thinking frames, not verdicts

### License

- Marketplace metadata (this repo): MIT
- Each plugin's content: see LICENSE in each plugin repository (mostly MIT)

---

## Maintainer

[Choi Hee Chul (@ironyjk)](https://github.com/ironyjk) — CEO of DY Industrial Development, 10+ years in C#/Python, active user of Claude Code as a decision-making platform.

Commercial licensing inquiries, framework consulting, or enterprise deployment: ironyjk@gmail.com
