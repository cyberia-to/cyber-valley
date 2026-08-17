---
tags: cyber valley, cyberia, legal, ceo, draft, dzin
alias: ceo economics, ceo kpi, ceo options
crystal-type: entity
crystal-domain: socio
crystal-size: article
icon: "🧾"
---
# CEO economics

Annex to [[cve/ceo/agreement]] · source numbers from [[cve/ceo/offer]] · replaces [[ceo compensation schedule]].

---

## 1. What the CEO is paid in

| component | rule |
|---|---|
| **Fixed salary** | optional — amount in appointment resolution only if founders want cash salary |
| **Options** | §2 — up to 10% @ $4M |
| **Ladder equity** | §3 — 10% of each sold package (except seed) |
| **Nothing else** | no land % grid, no referral stack, no raise fee in this pack |

---

## 2. Options — 5% + 5% @ $4M

| | |
|---|---|
| **Strike basis** | company valuation **USD 4,000,000** (1% ≈ USD 40,000) |
| **Pool** | up to **10%** of the company |
| **Tranche A** | **5%** · exercise within **2 years** of start |
| **Tranche B** | **5%** · exercise within **7 years** of start |

Source of shares (issue vs founder transfer): [[cve/ceo/open]].  
Commercial term is pool + strike + windows. Options ≠ KPI ladder.

---

## 3. KPI ladder — DS + AV only → founders ~10%, company → **$1B**

### Counts / does not

| counts | does not count |
|---|---|
| Sale/transfer of **DS** and **AV** founder shares at real price | Free print of new share classes |
| Cash + valuation on those sales | Cash-out theatre without third-party price |
| | Capital raise that does **not** move DS/AV on this ladder |

### Package split (every step **except seed**)

| | |
|---|---|
| **Package** | `step` of company equity leaving founders |
| **CEO** | **10% × step** (equity) |
| **Buyers** | **90% × step** (pay cash) |
| **Cash** | `0.90 × step × val` |

**Seed (1% @ $4M):** no CEO cut · cash = `1% × val` · **not** a CEO sale.

**First CEO sale:** **10%** cumulative · **val ≥ $10M**.

### Target ownership

| block | hands |
|---|---|
| Package 1 | Indonesian holders |
| Package 2 | Foreign / Cyberia holding |
| Residual ~10% | Founders (DS+AV) |
| CEO | ladder ~**8.9%** + options ≤10% @ $4M |

### Table

| sold cum. | step | val (USD) | CEO step | CEO cum. | cash step (USD) |
|---:|---:|---:|---:|---:|---:|
| **1%** | 1% | **4,000,000** | **—** | **0%** | **40,000** |
| **10%** | 9% | **10,000,000** | **0.90%** | **0.90%** | **810,000** |
| **20%** | 10% | **18,000,000** | **1.00%** | **1.90%** | **1,620,000** |
| **30%** | 10% | **30,000,000** | **1.00%** | **2.90%** | **2,700,000** |
| **40%** | 10% | **50,000,000** | **1.00%** | **3.90%** | **4,500,000** |
| **50%** | 10% | **90,000,000** | **1.00%** | **4.90%** | **8,100,000** |
| **60%** | 10% | **160,000,000** | **1.00%** | **5.90%** | **14,400,000** |
| **70%** | 10% | **280,000,000** | **1.00%** | **6.90%** | **25,200,000** |
| **80%** | 10% | **500,000,000** | **1.00%** | **7.90%** | **45,000,000** |
| **90%** | 10% | **1,000,000,000** | **1.00%** | **8.90%** | **90,000,000** |

Miss the val floor → step does not count (unless founders waive in writing).  
Between rows: log-interpolate val. CEO cut always 10% of that deal’s package (from $10M step on).

---

## 4. Survival

Ladder equity from **closed** steps survives CEO departure.  
Unvested options: as in option deed (Good Leaver keep time-pro-rata or forfeit — set at signing; default: keep earned time, forfeit unearned).
