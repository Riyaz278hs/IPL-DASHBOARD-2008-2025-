# IPL Analytics Dashboard (2008-2025)


[![Power BI](https://img.shields.io/badge/Power_BI-Data_Visualization-yellow?style=flat&logo=powerbi)](https://powerbi.microsoft.com/)
[![SQL](https://img.shields.io/badge/SQL-Data_Analysis-blue?style=flat&logo=sqlite)](https://www.sqlite.org/)
[![Excel](https://img.shields.io/badge/MS_Excel-Data_Cleaning-green?style=flat&logo=microsoftexcel)](https://www.microsoft.com/excel)

---


## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Strategic Recommendations](#strategic-recommendations)
- [Result](#result)


---

### Project Overview

The IPL Analytics Dashboard (2008-2025) is a comprehensive data analytics project designed to extract actionable insights from 18 seasons of the Indian Premier League. As a Computer Science Engineering graduate specializing in data analysis, I built this project to track historical team dominance, player efficiency, toss dependencies, and shifting match dynamics over nearly two decades.

1. Historical Performance Tracking: Evaluates how team win rates, formats, and strategies have evolved from 2008 to 2025.
2. Granular Player Metrics: Drill-down analysis of batter and bowler performances using ball-by-ball granularity.
3. Strategic Decision Support: Uncovers the hidden impact of toss decisions and venues on final match outcomes.

![Image alt](https://github.com/Riyaz278hs/IPL-DASHBOARD-2008-2025-/blob/main/IPL_Dashboard.jpg)



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

### Data Analysis

Below is an optimized relational SQL script demonstrating how the system connects granular ball-by-ball micro-events to master player attributes to isolate the all-time top run-scorers in IPL history:




