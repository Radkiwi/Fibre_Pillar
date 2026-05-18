# Craffft Pillars — Interactive Industrial Timelines

**An educational web experience tracing the history of New Zealand's four industrial pillars — from te ao Māori to the machine age.**

→ **[craffft.earth](https://craffft.earth)**

---

## Overview

This repository contains a suite of interactive, single-page HTML timelines and an educational hub built for [Craffft](https://craffft.earth) — a New Zealand learning platform where the second *F* in Craffft stands for **Fibre**.

Each timeline covers one of Craffft's four industry pillars, tracing its evolution across hundreds of years. Together they form an educational framework aligned with **Te Mātaiaho** (the New Zealand Curriculum refresh), with a specific focus on the Aotearoa New Zealand's Histories strand and English/Literacy achievement objectives.

---

## Pages

| File | Title | Span |
|------|-------|------|
| [`education.html`](education.html) | Why History Matters — Learning Hub | Big Bang → Present |
| [`fibre-timeline.html`](fibre-timeline.html) | NZ Fibre Industry | c.1300 → 2026+ |
| [`food-timeline.html`](food-timeline.html) | NZ Food Systems | c.1300 → 2026+ |
| [`Factory-timeline.html`](Factory-timeline.html) | NZ Advanced Manufacturing | c.1300 → 2026+ |
| [`transport-timeline.html`](transport-timeline.html) | NZ Transport | c.1300 → 2026+ |

---

## The Learning Hub — `education.html`

A comprehensive single-page educational site covering:

- **The Cosmic Timeline** — Big Bang (13.8 Bya) through the formation of our Solar System
- **The Geologic Time Scale** — Precambrian, Phanerozoic, and the emerging Anthropocene epoch
- **Aotearoa Industrial History** — An overview timeline across all four pillars from te ao Māori to Industry 4.0
- **Five Reasons Timelines Matter** — the systems-thinking rationale for Craffft's methodology
- **Te Mātaiaho Curriculum Alignment** — the Understand / Know / Do framework, Histories strand skill strips, and Literacy strand connections
- **The NPC Mindset** — the pedagogical goal of empowering students as ecopreneurs, not passive inhabitants of the existing system

---

## The Four Pillar Timelines

Each timeline is a self-contained, interactive horizontal scroll experience. All share the same design system.

### 🌿 Fibre — `fibre-timeline.html`
| Era | Year | Accent |
|-----|------|--------|
| Te Ao Tawhito | c.1300 | Gold |
| The Age of Sail | 1769 | Ocean teal |
| Industrial Fibre | 1880 | Amber |
| Synthetic Era | 1950 | Steel grey |
| Deregulation | 1984 | Sage |
| Bio-Economy | 2010 | Vibrant green |
| Regenerative Now | 2025 | Electric cyan |
| Ngā Ara | 2026+ | Future green |

### 🌱 Food — `food-timeline.html`
| Era | Year | Accent |
|-----|------|--------|
| Te Ao Tawhito | c.1300 | Leaf green |
| Age of Sail & Trade | 1769 | Harvest amber |
| The Refrigeration Revolution | 1882 | Sky blue |
| The Protected Farm | 1950 | Weathered earth |
| Rogernomics & Reform | 1984 | Data blue |
| Precision Agriculture | 1995 | Lush green |
| Regenerative Turn | 2020 | Science purple |
| Ngā Ara | 2026+ | Future mint |

### ⚙️ Factory — `Factory-timeline.html`
| Era | Year | Accent |
|-----|------|--------|
| The Craft Age | c.1300 | Clay ochre |
| Colonial Industry | 1840 | Colonial brass |
| The Protected Factory | 1950 | Factory blue |
| Deregulation Shock | 1984 | Disruption orange |
| Niche Mastery | 1990 | Precision gold |
| Industry 4.0 Arrives | 2016 | Digital indigo |
| The Automation Surge | 2020 | Innovation purple |
| Ngā Ara | 2026+ | Future mint |

### 🚢 Transport — `transport-timeline.html`
| Era | Year | Accent |
|-----|------|--------|
| Te Ara o Ngā Tīpuna | c.1300 | Waka green |
| Age of Ships | 1840 | Ocean teal |
| Iron Roads | 1870 | Iron gold |
| Road Era | 1922 | Asphalt grey |
| Digital Era | 1990 | Digital indigo |
| Green Infrastructure | 2019 | Electric green |
| The Electric Age | 2025 | Electric cyan |
| Ngā Ara | 2026+ | Future lime |

---

## Features

- **Horizontal scroll** with `scroll-snap-type: x mandatory` — one era per viewport
- **Full-width historical slider** — 8 clickable era segments coloured by accent; TODAY marker positioned at the boundary of the current era
- **Default landing** on the most substantive present-day era (index 6), not the first
- **Entrance animations** via `IntersectionObserver` — staggered fade-up on panel entry
- **Keyboard navigation** — `←` `→` `Home` `End`
- **Gold progress bar** — fills left-to-right as user moves through the timeline
- **Universal topbar** — 36px fixed nav on every page; active pillar highlighted; `← Craffft` links back to the learning hub
- **Bilingual headings** — English title (large, Playfair Display, accented) + Te Reo Māori subtitle (Inter, muted)
- **Era 8: Future Paths** — four scenario cards (invest / partner / delay / wild card) replace event cards in the final era of each timeline
- **Fully self-contained** — no frameworks, no external JS, no build step

---

## Curriculum Alignment — Te Mātaiaho

These timelines directly address the **Understand / Know / Do** framework:

**Aotearoa New Zealand's Histories strand**
- *Continuity and Change* — traced through the Transport pillar (waka → coal → EV)
- *Perspectives and Bias* — explored through Food and Fibre (Maramataka vs. pastoral farming)
- *Historical Narratives* — constructed through the Factory pillar (cause-and-effect chains to the present)

**English / Literacy strand**
- *Critical reading and data synthesis* — timelines as primary source documents
- *Persuasive writing* — industrial history as evidence for civic submissions
- *Contextual vocabulary* — syntropic, decortication, extractive, telemetry, kaitiakitanga, mātauranga, Maramataka acquired through context, not rote lists

---

## Design System

| Property | Value |
|----------|-------|
| Background | Dark near-black (varies per pillar: `#0C1A10`, `#0D180A`, `#0C1018`, `#0A0F18`) |
| Cream | `#F5EDD8` |
| Gold | `#C8A84B` |
| Heading font | Playfair Display (Google Fonts) |
| Body font | Inter (Google Fonts) |
| Layout | Fixed header + slider, full-height scroll track, fixed footer |
| Animations | CSS transitions + `IntersectionObserver`, no JS animation libraries |

---

## Deployment

The site is deployed via **Railway** with `serve` as the static file server.

```bash
# Local development
npm install
npm start     # serves on http://localhost:3000
```

Railway reads `railway.json` and runs:
```
serve . --listen $PORT --single
```

**GitHub Pages** (fallback): also available at  
`https://radkiwi.github.io/Craffft_Pillars/`

---

## Repository Structure

```
Craffft_Pillars/
├── education.html          # Learning hub — the homepage
├── fibre-timeline.html     # Fibre pillar interactive timeline
├── food-timeline.html      # Food pillar interactive timeline
├── Factory-timeline.html   # Factory pillar interactive timeline
├── transport-timeline.html # Transport pillar interactive timeline
├── package.json            # serve dependency for Railway
├── railway.json            # Railway deployment config
└── README.md
```

---

## About Craffft

Craffft is a New Zealand educational platform building the next generation of ecopreneurs — young people with the systems-thinking skills, historical context, and technical capability to design and build the sustainable industries of the future.

The four pillars — **Food, Fibre, Factory, Transport** — are the systems that built the modern world. Understanding their history is the first step to reimagining them.

**[craffft.earth](https://craffft.earth)**
