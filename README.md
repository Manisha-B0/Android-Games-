# Android Games Data Analysis and Business Insights

An end-to-end data analytics project on **6,142 mobile games (2018-2025)** covering revenue, engagement, retention, and ratings. Built with Excel, Python (Pandas), and a three-page interactive Power BI dashboard, it shows that genre, monetization model, and crash rate matter more than art style or session length.

**Team:** Insights Hub - Manisha, Kavya, Nishanth | **Institution:** Teks Academy | **Program:** Data Science

---

## Project Objective

Turn detailed mobile game performance data into insights that developers and publishers can act on, by finding what drives higher active users, longer sessions, stronger ratings, and greater revenue across genres, art styles, monetization models, and regions.

## Dataset

| Attribute | Details |
|---|---|
| Name | Mobile Games Engagement & Monetization Dataset |
| Source | Kaggle |
| Records | 6,142 rows (one row per game) |
| Columns | 43 |
| Period | 2018-2025 |
| Regions | Global, US, Europe, India, LATAM, SEA |

Key columns: `genre`, `sub_genre`, `monetization_model`, `art_style`, `publisher_tier`, `downloads`, `active_users`, `avg_session_minutes`, `retention_day1/7/30_pct`, `rating_avg`, `crash_rate_pct`, `marketing_spend_usd`, `arpu_usd`, `total_revenue_usd`.

## Tools and Technologies

- **Excel** - initial inspection, pivot checks, validation
- **Python (Pandas, NumPy, scikit-learn)** - cleaning, correlation analysis, EDA, regression model
- **Microsoft Power BI** - interactive three-page dashboard

## Methodology

1. **Data validation** - null checks, category consistency, datetime and range checks (a few slightly negative `crash_rate_pct` values were flagged, not removed)
2. **Feature engineering** - `release_year`, review rate %, post-30-day rating velocity
3. **Exploratory analysis** - revenue, engagement, retention, ratings, marketing ROI
4. **Correlation analysis** against revenue, active users, session length, and rating
5. **Predictive analysis** - linear regression revenue model and a 2026-2028 trend forecast
6. **Dashboard** - three Power BI pages for interactive exploration

## Headline Numbers

| Metric | Value |
|---|---|
| Total Revenue | $271.60M |
| Total Downloads | 714M |
| Avg Revenue / Game | $44.22K |
| Revenue / Active User | $5.40 |
| Avg Session Duration | 19.52 min |
| Avg Rating | 3.63 |
| Retention (Day 1 / 7 / 30) | 30.1% / 16.5% / 7.8% |

## Key Insights

1. **Genre beats art style for revenue** - Puzzle, Casual, and Action generate over 54% of revenue; art styles are almost evenly split.
2. **Crash rate is the clearest driver of rating** - under 2% crash rate averages 3.75 stars vs. 3.30 above 6% (r = -0.37).
3. **Session length is design-independent** - about 19.5 minutes across genres, tiers, and styles; focus on session frequency and retention.
4. **Downloads do not equal engagement** - only about 7% of downloads become active users.
5. **Retention decays predictably** - onboarding, not genre, is the main lever.
6. **Indie studios punch above their weight** - largest revenue pool ($159.7M) and best marketing return (7.85x).
7. **Racing and Simulation have the best marketing ROI** - 8.48x and 8.28x.
8. **Revenue and ratings are stable, not trending** - cohort revenue stays within $31M-$38M per year; baseline forecast is about $33.5M per year for 2026-2028.





## Repository Contents

```
.
├── Android_Game_RAW.xlsx      # Raw dataset
├── AG_project.csv             # Project dataset (CSV)
├── games_dashboard.pbix       # Power BI dashboard
├── Problem_Statement.pdf      # Objective, problem statement, dataset overview
├── Insights.pdf               # Key findings and business implications
└── README.md
```

## How to View the Dashboard

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows).
2. Download `games_dashboard.pbix` and open it.
3. Use the slicers to filter by genre, art style, monetization model, and more.

## Limitations

- Correlation does not imply causation.
- Data is game-level and cross-sectional (no per-game time series or user-level data), so the forecast is only a baseline.
- The linear model is directional, not precise.

## Future Improvements

- Random Forest / XGBoost for revenue and rating prediction
- Monthly time-series tracking and forecasting (ARIMA, Prophet)
- Churn and retention prediction from Day 1 and Day 7 behavior
- What-if parameters in Power BI (for example, a crash-rate slider)

