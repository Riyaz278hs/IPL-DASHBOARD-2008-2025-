# IPL Analytics Dashboard (2008-2025)


[![Power BI](https://img.shields.io/badge/Power_BI-Data_Visualization-yellow?style=flat&logo=powerbi)](https://powerbi.microsoft.com/)
[![SQL](https://img.shields.io/badge/SQL-Data_Analysis-blue?style=flat&logo=sqlite)](https://www.sqlite.org/)
[![Excel](https://img.shields.io/badge/MS_Excel-Data_Cleaning-green?style=flat&logo=microsoftexcel)](https://www.microsoft.com/excel)

---


## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Strategic Recommendations](#strategic-Recommendations)
- [Results](#Results)


---

### Project Overview

The IPL Analytics Dashboard (2008-2025) is a comprehensive data analytics project designed to extract actionable insights from 18 seasons of the Indian Premier League. As a Computer Science Engineering graduate specializing in data analysis, I built this project to track historical team dominance, player efficiency, toss dependencies, and shifting match dynamics over nearly two decades.

1. Historical Performance Tracking: Evaluates how team win rates, formats, and strategies have evolved from 2008 to 2025.
2. Granular Player Metrics: Drill-down analysis of batter and bowler performances using ball-by-ball granularity.
3. Strategic Decision Support: Uncovers the hidden impact of toss decisions and venues on final match outcomes.

![Image alt](https://github.com/Riyaz278hs/IPL-DASHBOARD-2008-2025-/blob/main/Ipl%20dashboard.jpg)



---

### Data Sources

The project's relational architecture handles four main structured datasets containing records for over 1,100 matches:
1. ipl_matches_data.csv – High-level match metadata profiling dates, locations, toss winners, match winners, and victory margins (win_by_runs, win_by_wickets).
2. ball_by_ball_data.csv – Micro-level delivery rows tracking innings details, batsmen, bowlers, runs scored (batter_runs), extra types, and structural dismissals.
3. players-data-updated.csv – Master mapping directory indexing player profiles against their specific batting preference (bat_style) and bowling hand variations (bowl_style).
4. teams_data.csv – Reference lookup registry standardizing full franchise titles and unique shorthand identifier codes.

---

### Tools

1. MS Excel [Data Cleaning]: Utilized for visual column profiling, validation checks, and building interactive final dashboard views powered by pivot tables, custom charts, and slicers.
2. SQL Query [Data Analysis]: Employed to write fast relational multi-table JOIN operations, aggregate deep stats from large multi-million row datasets, and query career performance milestones.
3. Python (Pandas) [ETL Engine]: Leveraged to programmatic bypass file loading anomalies (latin1 streams), handle missing data fields, and perform automated preprocessing steps.
4. BI Tool: Power BI Desktop
5. Data Transformation: Power Query (ETL, Data Cleaning, Null Handling)
6. Modeling: DAX (Data Analysis Expressions) for custom KPIs and measures

---

### Data Cleaning / Explanation
1. Character Encoding Rectification: Addressed execution crashes by configuring data loading streams to process files through explicit latin1 parsing matrices.
2. Franchise Name Standardization: Resolved naming changes over 18 seasons by creating uniform mapping rules to normalize re-branded clubs (e.g., merging historical data for Delhi Daredevils into Delhi Capitals).
3. Feature Flag Engineering: Transformed raw text descriptors into explicit boolean variables (is_wicket, is_wide_ball, is_no_ball) to perfectly isolate true batter runs from extra penalties.

---

### Exploratory Data Analysis (EDA)

1. Margin Vector Tracking: Plotted the distribution of matches won by runs versus matches won by wickets to evaluate historical venue chasing habits.
2. Franchise Dominance Scaling: Plotted overall match victories across seasons to clearly separate stable elite-tier performers from volatile teams.
3. Tactical Strategy Mapping: Mapped historical shifts in toss preferences (field vs bat) against night-game coordinates to evaluate how dew factors influence strategies.

---

## 🚀 Results

* Comprehensive Season Tracking: Successfully modeled and visualized data across 17+ seasons, detailing championship trends, boundaries, and venue dynamics.
* Top Performance Metrics: Dynamically isolates individual milestones, such as Shubman Gill's 2023 Orange Cap run (890 runs, 84 fours) and Mohammed Shami's Purple Cap dominance (28 wickets).
* Boundaries Analytics: Tracks historical power-hitting trends, showcasing peak seasons like 2023 with 1,110 sixes and 2,160 fours across 74 matches.
* Automated Points Table: Built a dynamic, real-time points table calculating Wins, Losses, Net Run Rate (NRR), and Total Points per season.

---

## 💡 Strategic Recommendations

* Data-Driven Auction Scouting: Use historical performance thresholds (like Orange/Purple cap trajectories) to optimize player acquisition budgets and predict future consistency.
* Venue-Specific Strategies: Analyze team performance across the 12+ unique venues to optimize team composition (e.g., spin vs. pace heavy line-ups) based on ground-specific boundary data.
* Anchoring vs. Power Hitting: Balance team structures by contrasting high-volume boundary hitters (e.g., F du Plessis with 36 sixes) with high-average anchors to maximize projectable team totals.
* Toss & Match Condition Modeling: Integrate toss decision patterns to recommend optimal bat/bowl choices depending on specific venue histories.

---

## ⚠️ Project Limitations

* Lack of Live/In-Play Data: The current dashboard relies on historical post-match datasets and does not support real-time, ball-by-ball live match tracking.
* External Variables Omitted: Strategic insights exclude crucial external factors such as player injuries, pitch degradation reports, and weather conditions.
* Data Granularity: The modeling primarily focuses on aggregate seasonal stats rather than micro-situations (e.g., performance specifically in the death overs or powerplay).

---

