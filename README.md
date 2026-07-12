# IPL Analytics Dashboard (2008-2025)

## Table of Contents
- [Project Overview](#project-overview)
- [Project Structure](#project-structure)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Data Cleaning & Transformation](#data-cleaning--transformation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Analysis & SQL Queries](#data-analysis--sql-queries)
- [Key Insights & Results](#key-insights--results)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

---

### Project Overview
The IPL Analytics Dashboard (2008-2025) is a comprehensive data analytics project designed to extract actionable insights from 18 seasons of the Indian Premier League. As a Computer Science Engineering graduate specializing in data analysis, I built this project to track historical team dominance, player efficiency, toss dependencies, and shifting match dynamics over nearly two decades.

1. Historical Performance Tracking: Evaluates how team win rates, formats, and strategies have evolved from 2008 to 2025.
2. Granular Player Metrics: Drill-down analysis of batter and bowler performances using ball-by-ball granularity.
3. Strategic Decision Support: Uncovers the hidden impact of toss decisions and venues on final match outcomes.

---

ipl_analytics_system/
│
├── data_pipeline/
│   ├── init.py
│   └── etl_engine.py          # Data Extraction, Cleaning & Transformation Engine
│                               # - Custom data loaders for 4 core CSV datasets
│                               # - 5-step preprocessing (latin1 encoding fix, null handling)
│                               # - Automated team name standardization & renaming map
│                               # - Feature engineering (is_wicket, is_wide_ball flags)
│
├── database/
│   ├── init.py
│   └── query_engine.py        # SQL Relational & Analytical Query Engine
│                               # - Multi-table INNER JOIN configurations
│                               # - Aggregation logic for career runs and match counts
│                               # - Historical team win/loss ratio computations
│                               # - High-resolution venue performance matrices
│
├── analytics/
│   ├── init.py
│   └── edb_engine.py          # Exploratory Data Analysis & Metric Engine
│                               # - 1,169 match records processed (2008-2025)
│                               # - Toss decision impact distribution metrics:
│                               #     Fielding First Wins:      413 matches (54.0%)
│                               #     Batting First Wins:       185 matches (45.8%)
│                               # - Historical Franchise Dominance Ranking:
│                               #     Mumbai Indians:           153 wins
│                               #     Chennai Super Kings:      142 wins
│
├── dashboard/
│   └── app.py                 # Interactive Dynamic Presentation Dashboard
│                               # Tab 1: Historical Franchise Dominance
│                               # Tab 2: Toss Strategy & Venue Impact
│                               # Tab 3: Ball-by-Ball Player Performance
│                               # Tab 4: Advanced SQL Audit & Insights
│
├── requirements.txt
└── README.md
