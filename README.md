# FIFA World Ranking — Interactive Dashboard
### Power BI Project | October 2022 Snapshot (Pre-World Cup Qatar)

> An interactive Power BI dashboard analysing FIFA World Rankings for all 211 national football teams. Built to surface ranking trends, confederation comparisons, biggest movers, and match performance — snapshot taken just before the 2022 FIFA World Cup in Qatar.

---

## Dashboard Pages

| # | Page | Key Visuals |
|---|---|---|
| 1 | Executive Overview | KPI cards, confederation donut, avg points bar, rank movement |
| 2 | Top Teams Leaderboard | Full rankings table, top 20 bar chart, tier column chart |
| 3 | Rank Movement Analysis | Biggest climbers & fallers, scatter plot, funnel |


---

## Dataset Overview

| Property | Detail |
|---|---|
| **Source** | FIFA World Rankings — Kaggle |
| **Snapshot Date** | October 6, 2022 |
| **Context** | 16 days before FIFA World Cup Qatar 2022 kick-off |
| **Total Teams** | 211 national football teams |
| **Confederations** | 6 (UEFA, CAF, AFC, CONMEBOL, CONCACAF, OFC) |
| **Original Columns** | 7 |
| **Enriched Columns** | 24 (after feature engineering) |

---

## Column Reference

### Original Columns
| Column | Type | Description |
|---|---|---|
| `team` | Text | National team name |
| `team_code` | Text | 3-letter FIFA code (e.g. BRA, FRA) |
| `association` | Text | Confederation code |
| `rank` | Number | Current FIFA world rank (1 = best) |
| `previous_rank` | Number | Rank in previous period |
| `points` | Decimal | Current FIFA ranking points |
| `previous_points` | Decimal | Points in previous period |

### Engineered Columns (added for dashboard)
| Column | Description |
|---|---|
| `rank_change` | Previous rank − Current rank (positive = climbed) |
| `rank_change_abs` | Absolute value of rank change |
| `rank_direction` | "Climbed" / "Dropped" / "No Change" |
| `points_change` | Points gained or lost |
| `tier` | Elite (Top 20) / Strong (21-50) / Mid (51-100) / Lower (101+) |
| `association_full` | Full confederation name with region |
| `continent` | Simplified region name |
| `points_bracket` | Points grouped in bands (e.g. 1500-1700) |
| `rank_percentile` | Percentile rank (100 = best, 0 = lowest) |
| `matches_played` | Simulated recent matches |
| `wins / draws / losses` | Simulated match outcomes |
| `goals_scored / conceded` | Simulated goal data |
| `goal_difference` | Goals scored minus goals conceded |
| `win_rate_pct` | Win percentage (0–100) |

---

## Key Findings

| # | Insight | Detail |
|---|---|---|
| 🥇 | **#1 Ranked Team** | **Brazil** — 1,841.30 points |
| 🥈 | **#2 Ranked Team** | **Belgium** — 1,816.71 points |
| 🏆 | **Strongest Confederation** | **CONMEBOL** — avg 1,554.9 pts (only 10 teams, all South American) |
| 🌍 | **Largest Confederation** | **UEFA (Europe)** — 55 teams |
| 📊 | **Most Competitive** | UEFA has the highest density of Elite and Strong tier teams |
| ⬆️ | **Biggest Climbers** | Scotland & Azerbaijan — both rose 5 places |
| ⬇️ | **Biggest Faller** | Norway — dropped 6 places |
| 📈 | **Point Gap (#1 vs #2)** | Brazil leads Belgium by **24.59 points** |
| 🔄 | **Rank Movements** | 77 climbed · 68 dropped · 66 unchanged |
| 🌍 | **Africa** | 54 teams (CAF) — largest by team count, avg rank 109.8 |
| 🏝️ | **Lowest Avg Points** | OFC (Oceania) — avg 983.5 pts across 11 teams |

---

## Confederation Breakdown

| Confederation | Teams | Avg Rank | Avg Points | Best Team |
|---|---|---|---|---|
| CONMEBOL – South America | 10 | 31.7 | 1,554.9 | Brazil (#1) |
| UEFA – Europe | 55 | 68.2 | 1,380.9 | Belgium (#2) |
| CAF – Africa | 54 | 109.8 | 1,195.9 | Senegal (#18) |
| AFC – Asia | 46 | 124.7 | 1,138.0 | IR Iran (#20) |
| CONCACAF – N/C America | 35 | 137.6 | 1,094.9 | Mexico (#13) |
| OFC – Oceania | 11 | 165.0 | 983.5 | New Zealand (#105) |

---

## Visuals Used in This Project

| Visual Type | Count | Used For |
|---|---|---|
| Card | 12 | KPI metrics across all pages |
| Clustered Bar Chart | 6 | Confederation comparisons, climbers/fallers |
| Clustered Column Chart | 3 | Points by tier, goals chart |
| Donut Chart | 2 | Confederation split, tier distribution |
| Table | 3 | Full rankings, confederation teams, negative GD |
| Scatter Chart | 1 | Points change vs rank change matrix |
| Slicer | 5 | Confederation, tier, rank direction filters |

