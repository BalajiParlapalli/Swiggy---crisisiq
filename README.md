# CrisisIQ — Swiggy Builders Club

> **AI informational layer for fuel-aware rider welfare, restaurant cost foresight, and customer fee transparency**

A Swiggy MCP platform submission. Purely informational — no new charges, no ranking changes, no dark patterns.

---

## Live Demo

👉 **[https://balajiparlapalli.github.io/Swiggy---crisisiq/](https://balajiparlapalli.github.io/Swiggy---crisisiq/)**

---

## The Problem

By mid-2026, Swiggy faces simultaneous shocks that no current feature addresses proactively:

| Crisis | Impact on Swiggy ecosystem |
|--------|---------------------------|
| ⛽ Petrol quarterly average spikes ₹10–15 | Riders absorb full cost; BPCL card is static |
| 🌡 Super El Niño — WMO 70%+ probability, peaks 2027 | Riders face 42°C+ heat with no proactive safety layer |
| 🍳 LPG + cooking oil surge | Restaurants raise prices or silently shrink portions; customers blame Swiggy |
| 🌧 Erratic monsoon — drought + flash floods | Rural routes fail with zero advance warning |

---

## Three Modules — Three Audiences — Purely Informational

### 01 · FuelSense — Rider welfare (inside delivery partner app only)

**What it does:**
- Monitors quarterly average petrol price via PPAC India open data
- If Q2 quarterly average rises ₹10+ above Q1 baseline → unlocks a bike servicing voucher (₹500–₹800) redeemable at Swiggy-partnered garages
- Trigger is quarterly, not daily — no pay changes for every ₹1–2 price movement
- Urban and rural riders both eligible
- IMD heat alert (40°C+ for 3+ consecutive days) → shows rest window recommendation + protects incentive streak during declared alert
- Monsoon route advisory: flood-risk road segments flagged before rider accepts order — informational only, rider decides

**What it does NOT do:**
- No per-delivery fuel calculations
- No daily pay changes
- No voice alerts in any language
- No override of Swiggy's order assignment or routing engine
- No manipulation of incentive structures beyond the declared streak-protection welfare measure

---

### 02 · AffordaMatch — Customer transparency (inside Swiggy customer app only)

**What it does:**
- Makes the existing "GST & Other Charges" line tap-to-expand — showing the breakdown of what is already inside it
- Customer's total bill does not change by a single rupee
- Fuel component visibility only activates when Q2 quarterly average is ₹10+ above Q1 baseline — not for daily fluctuations
- When fuel is at or below baseline, no fuel mention appears at all
- Weather-adaptive discovery: on IMD-confirmed 40°C+ for 3+ days, a curated shelf surfaces cold/hot food — labeled "not a paid placement" with data source disclosed
- Rural pre-scheduling: optional additional feature for disruption-prone zones — does not replace standard ordering

**What it does NOT do:**
- No new charges added to any order
- No changes to Swiggy's ranking algorithm or order flow
- No manipulation of delivery time estimates
- No dark patterns, no urgency framing, no scarcity language
- The curated weather shelf does not override standard ranking — it sits alongside it, fully labeled

---

### 03 · RestoCost Shield — Restaurant foresight (inside Swiggy partner portal only)

**What it does:**
- Reads wholesale price indices from AGMARKNET (Ministry of Agriculture open data)
- Cuisine-mapped: an Andhra rice restaurant sees basmati + oil alerts only
- 3–4 week price forecasts clearly labeled as forecasts with uncertainty ranges
- Shrinkflation monitor: private to the restaurant only — never shown to customers, never used in ranking
- Group buy coordination: fully opt-in, no commitment, no penalty for not joining

**What it does NOT do:**
- No changes to restaurant's Swiggy menu or pricing
- Shrinkflation signal never shared with customers or used in any Swiggy ranking decision
- Group buy participation does not affect restaurant listing, ranking, or visibility — stated explicitly
- No instruction given to restaurant — advisory only, restaurant decides

---

## What Is NOT Duplicated From Existing Swiggy Features

| Existing Swiggy feature | Why CrisisIQ doesn't touch it |
|-------------------------|-------------------------------|
| Basic route optimisation + GPS | Already live — CrisisIQ adds flood advisory layer only, informational |
| Driver Dost AI chatbot | Handles onboarding/earnings — CrisisIQ handles external economic signals |
| Real-time demand heatmaps | Already in rider app — CrisisIQ adds quarterly fuel welfare layer |
| Basic surge pricing | Already implemented — CrisisIQ adds transparent breakdown of existing charges |
| BPCL fuel card | Already exists — CrisisIQ adds quarterly welfare voucher when price crosses threshold |
| Basic heatwave cooling vests | Already doing — CrisisIQ adds IMD-triggered digital heat safety alert |

---

## Swiggy Builders Club Compliance

### What We Allow ✅

| Rule | CrisisIQ |
|------|----------|
| Building apps that make ordering / discovery better | Fee transparency reduces confusion. Climate discovery helps customers find relevant food. |
| AI copilot using MCP to automate commerce workflows | Reads Swiggy Food + Instamart MCP. External signals from PPAC, IMD, AGMARKNET. |
| Creative side project / experimental prototype | This is a hackathon-style prototype built for Builders Club. |
| Integrations following Swiggy security and branding guidelines | Embedded inside Swiggy's own apps. Never hides Swiggy's brand. |
| Sharing demos and walkthroughs | Live demo above. Full source in this repo. |
| Commercial partnership where both sides win | Swiggy retains riders + restaurants + customer trust. CrisisIQ gets MCP access. |

### Not Allowed ✅ (CrisisIQ avoids all of these)

| Rule | CrisisIQ status |
|------|----------------|
| Reselling or sharing MCP access | Not applicable — single developer submission |
| Building aggregation layers that hide Swiggy's brand | CrisisIQ is embedded inside Swiggy's apps, never standalone |
| Misrepresenting prices, availability, or delivery times | Fee breakdown shows existing charges only — total unchanged. No delivery time shown. |
| Scraping or extracting data beyond what APIs provide | PPAC, IMD, AGMARKNET are open government APIs. MCP data within agreed scope only. |
| Using APIs for competitive intelligence or benchmarking | No competitor data read, stored, or benchmarked at any point |
| Bypassing rate limits, logging, or platform safeguards | PPAC: daily poll. IMD: 6-hourly. AGMARKNET: weekly. Standard usage. |

### Prohibited Conduct — Zero Tolerance ✅ (CrisisIQ violates none)

| Rule | CrisisIQ status |
|------|----------------|
| 01 Manipulating order flows, incentives, or ranking systems | Order flow: untouched. Ranking: untouched. Incentive: untouched except declared streak-protection during IMD heat alerts — a welfare measure, disclosed to riders. |
| 02 Dark patterns, deceptive UX, or misattributing data sources | Every data source labeled inline. Weather shelf labeled "not a paid placement." Fee note says explicitly it is not a new charge. |
| 03 Generating fake traffic or abusing rate limits | No real-time hammering. All API calls within normal usage patterns. |
| 04 Harvesting data beyond agreed scope | Only rider earnings, menu prices, order history via MCP. Nothing beyond this. |
| 05 Reverse engineering MCP internals | Documented endpoints only. No inspection of internal Swiggy systems. |
| 06 Circumventing whitelisting or access controls | Standard OAuth 2.0. No access to non-whitelisted endpoints. |
| 07 Violating user privacy or security regulations | Rider data stays in partner app scope. Shrinkflation signals private to restaurant only. No personal data stored. |

---

## Data Sources — Open Government Data Only

| Source | Data used | Purpose |
|--------|-----------|---------|
| [PPAC India](https://ppac.gov.in) | Monthly retail petrol prices by city | Quarterly average for rider voucher trigger |
| [IMD API](https://mausam.imd.gov.in) | Temperature + humidity by district | Heat alerts, monsoon route advisories |
| [AGMARKNET](https://agmarknet.gov.in) | Wholesale commodity prices | Restaurant input cost forecasts |
| [MOSPI CPI](https://mospi.gov.in) | Consumer Price Index | Restaurant cost benchmarking context |

No competitor data. No scraping. No copyright issues. All sources are Indian government open data.

---

## Tech Stack

- **Frontend:** Vanilla HTML/CSS/JS — no build step, works on 2G and low-end Android
- **Auth:** OAuth 2.0 flow for Swiggy Food + Instamart MCP servers
- **External data:** PPAC (daily), IMD (6-hourly), AGMARKNET (weekly) — stateless, cached
- **AI layer:** Claude API (claude-sonnet-4-6) for advisory text generation only
- **Storage:** No user data stored beyond session

**Redirect URI for auth:** `https://balajiparlapalli.github.io/Swiggy---crisisiq/callback`

---

## Deploy This Demo

```bash
# Fork this repo
git clone https://github.com/BalajiParlapalli/Swiggy---crisisiq.git

# No build step needed — pure HTML/CSS/JS
# Enable GitHub Pages: Settings → Pages → Branch: main → / (root)
# Live at: https://balajiparlapalli.github.io/Swiggy---crisisiq/
```

---

## Project Name
**CrisisIQ by Swiggy** — *Stable delivery in an unstable world*

**Submitted by:** BalajiParlapalli  
**Track:** AI Agent / Copilot  
**MCP servers needed:** Swiggy Food, Swiggy Instamart  
**Builders Club:** [mcp.swiggy.com/builders](https://mcp.swiggy.com/builders/access/)
