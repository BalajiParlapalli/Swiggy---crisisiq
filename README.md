# CrisisIQ — Swiggy Builders Club

> **AI copilot for fuel-aware delivery optimization and affordability intelligence**

A Swiggy MCP platform submission that protects riders, restaurant partners, and customers through fuel price volatility, the 2026–27 Super El Niño, and supply-chain disruptions.

---

## Live Demo

👉 **[View the interactive demo](https://BalajiParlapalli.github.io/crisisiq/)** ← replace after GitHub Pages deploy

---

## The Problem

By mid-2026, Swiggy faces simultaneous shocks that no current feature addresses:

| Crisis | Impact |
|--------|--------|
| ⛽ Petrol price volatility | Riders absorb fuel costs directly; existing BPCL card is static |
| 🌡 Super El Niño (70%+ probability, WMO Apr 2026) | Riders face 42°C+ heat with no proactive warning system |
| 🍳 LPG + cooking oil surge | Restaurants raise prices or shrink portions; customers blame Swiggy |
| 🌧 Erratic monsoon | Rural routes become impassable with zero advance warning |

---

## Three Modules

### 1. FuelSense — Dynamic fuel-parity pay for riders
- Reads live petrol prices by PIN code from **PPAC India** (open government data)
- Auto-adds a per-km fuel-parity top-up to rider payout when price exceeds baseline
- Tracks E20 ethanol blends — rural riders get calibrated rates, not metro flat rates
- Heat index alerts from **IMD API** — unlocks "heat break" status (15 min rest, streak protected)
- Monsoon route intelligence for flood/drought-affected zones
- **Literacy-first UI**: colour + icons + local language voice clip (Telugu, Tamil, Hindi, Kannada, Bengali)

### 2. RestoCost Shield — Restaurant input cost intelligence
- Aggregates wholesale price indices from **AGMARKNET** (Ministry of Agriculture)
- Cuisine-mapped alerts (biryani place gets basmati + oil alerts, not irrelevant items)
- 2–4 week price forecasts using El Niño crop impact + commodity trend models
- Portion-shrinkflation detector: stable price + dropping ratings = likely portion reduction flag
- **Group buy coordination**: clusters nearby restaurant partners for wholesale LPG/oil pricing

### 3. AffordaMatch — Customer fee transparency + climate discovery
- Itemised delivery fee showing exact fuel cost component — updated daily from PPAC
- "Steady Price" badge for restaurants whose prices haven't exceeded local CPI rate
- Weather-adaptive discovery: cold drinks on 44°C days, hot soups on monsoon days — utility feature, fully labeled, not paid placement
- Rural pre-scheduling for El Niño disrupted routes

---

## What's NOT Duplicated from Swiggy

| Existing Swiggy feature | Why CrisisIQ doesn't touch it |
|-------------------------|-------------------------------|
| Basic route optimization | Already live — CrisisIQ adds climate disruption layer only |
| Driver Dost chatbot | Already handles onboarding/earnings — CrisisIQ handles external signals |
| Real-time demand heatmaps | Already in rider app — CrisisIQ adds forward-looking climate intelligence |
| Basic surge pricing | Already implemented — CrisisIQ adds transparent fuel-component disclosure |
| BPCL fuel card | Already exists — CrisisIQ makes it dynamic and PIN-code specific |

---

## Data Sources (Open Government Data Only)

| Source | Data | Use |
|--------|------|-----|
| [PPAC India](https://ppac.gov.in) | Daily retail petrol/diesel prices by city | FuelSense payout calculation |
| [IMD API](https://mausam.imd.gov.in) | Temperature, humidity, rainfall | Heat alerts, monsoon routing |
| [AGMARKNET](https://agmarknet.gov.in) | Wholesale commodity prices | RestoCost Shield forecasts |
| [MOSPI CPI](https://mospi.gov.in) | Consumer Price Index | Steady Price badge threshold |

No competitor data. No scraping. No data beyond agreed MCP scope.

---

## MCP Compliance

| Rule | Status | How |
|------|--------|-----|
| Makes ordering/discovery better | ✅ | Fee transparency + climate-adaptive UX |
| AI copilot using MCP workflows | ✅ | Reads rider earnings, menu prices, order data via MCP |
| No misrepresentation of prices | ✅ | Fee breakdown discloses every component and source |
| No ranking manipulation | ✅ | Weather suggestions labeled as utility, not ranking |
| No data harvesting beyond scope | ✅ | MCP data + open govt APIs only |
| No dark patterns | ✅ | All logic disclosed; voice alerts are accessibility, not manipulation |
| Swiggy brand respected | ✅ | CrisisIQ is a layer on Swiggy — never hides the platform |
| Commercial win for both sides | ✅ | Swiggy retains riders + restaurants; margins stabilize |

---

## Deploy as Demo (GitHub Pages)

```bash
# 1. Fork / clone this repo
git clone https://github.com/YOUR-USERNAME/crisisiq.git

# 2. No build step needed — pure HTML/CSS/JS
# 3. Enable GitHub Pages: Settings → Pages → Source: main branch / root

# Your demo will be live at:
# https://YOUR-USERNAME.github.io/crisisiq/
```

---

## Competitor-Inspired Concepts (Safe to Use)

All borrowed concepts are publicly disclosed industry practices — no proprietary code or implementation details:

- **Uber (US, 2022)**: Temporary fuel surcharge passed 100% to drivers → adapted as dynamic, PIN-code-specific real-time top-up
- **BigBasket B2B**: Bulk procurement for small retailers → adapted as group-buy for restaurant LPG/oil clusters
- **Zepto surge model**: Bad-weather pay bonuses → adapted as El Niño climate-event bonuses
- **Namma Yatri**: Fee transparency model → adapted as fuel-cost itemisation for customers

---

## Project Name
**CrisisIQ by Swiggy** — *Stable delivery in an unstable world*

---

## Contact / Application

Submitting as **Developer track** via [Swiggy Builders Club](https://mcp.swiggy.com/builders/access/)

For questions: [builders@swiggy.in](mailto:builders@swiggy.in)
