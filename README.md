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

### Project Structure
`text
├── data/
│   ├── ipl_matches_data.csv        # Match metadata, dates, venues, results
│   ├── ball_by_ball_data.csv       # Ball-by-ball events, runs, extras, dismissals
│   ├── players-data-updated.csv   # Player profiles, batting/bowling styles
│   └── teams_data.csv             # Full team names and short tags
├── sql_queries/
│   ├── data_cleaning.sql
│   └── advanced_analysis.sql
├── notebooks/
│   └── ipl_eda_notebook.ipynb      # Python data analysis script
├── dashboards/
│   └── ipl_dashboard_excel.xlsx    # Interactive MS Excel Dashboard
└── README.md                       # Documentation
