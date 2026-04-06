# How Can a Wellness Technology Company Play It Smart?

**Bellabeat — Capstone for Google Data Analytics Professional Certificate**

A comprehensive analysis of smart device usage data to uncover behavioral patterns and inform strategic marketing decisions. This project demonstrates end-to-end data analysis: preparation, processing, exploratory analysis, visualization, and actionable recommendations for a high-tech wellness company.

---

## 📊 Project Resources

- **[Data Analysis Notebook](notebooks/bellabeat_wellness_analysis.ipynb)** — Python-based analysis with derived metrics, pattern discovery, and segment profiling
- **[Strategic Insights](https://docs.google.com/presentation/d/1RmR7E-n8LG3ChkKzMdp_hvu58NEcJupVKOYmFJNkl4g)** — Stakeholder-ready presentation with findings and recommendations

---

## 📁 Project Structure

```
bellabeat/
├── README.md                                # Project overview and guide
├── notebooks/
│   └── bellabeat_wellness_analysis.ipynb    # Main Python analysis notebook
├── outputs/
│   └── strategic_insights.pdf               # Presentation export
└── data/
    └── raw/
        └── fitabase_4.12.16-5.12.16/
            ├── dailyActivity_merged.csv     # Daily activity: steps, distance, calories, intensity levels
            └── sleepDay_merged.csv          # Sleep: time in bed, time asleep, sleep efficiency
```

---

## 📋 Data Sources & Ethics

- **Source:** [FitBit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit) (CC0: Public Domain, Kaggle dataset)
- **Sample:** 33 FitBit users (activity dataset) and 24 users (sleep dataset) who consented to share personal tracker data (April–May 2016)
- **Privacy:** Analysis uses only aggregated metrics with no personal identifiers; user consent obtained
- **Credibility:** Kaggle usability score of 9.41; publicly available for reproducibility
- **Usage:** Data analyzed to understand non-Bellabeat smart device patterns applicable to Bellabeat's product strategy

---

## 🔍 Analysis Overview

### Data Preparation & Cleaning
- Loaded daily activity and sleep datasets
- Validated data quality (no missing values, removed duplicates if present)
- Created derived features: sleep efficiency (`TotalMinutesAsleep / TotalTimeInBed × 100`), sleep duration in hours, activity segments based on step thresholds, temporal variables

### Key Metrics Analyzed
- **Activity patterns:** Daily steps, sedentary hours, activity intensity levels (very active, fairly active, lightly active), calories
- **Sleep quality:** Total sleep duration, time in bed, sleep efficiency percentage
- **User segmentation:** Three activity tiers based on step counts (10k+, 5–10k, <5k)
- **Behavioral relationships:** Correlation between steps and sedentary time, sleep efficiency patterns

### Visualization Approach
- Custom color palettes for brand alignment
- LOESS trend smoothing to identify patterns
- Segment-based histograms for audience targeting
- Sleep efficiency scatter plots with diagonal reference lines

---

## 💡 Key Findings

1. **The Sedentary Paradox:** Users average **16.5 hours of sedentary time daily**, even those hitting 10,000+ steps. Step count alone doesn't capture total health — active users can still be highly sedentary.

2. **Three Distinct User Segments:** Behavior clusters into clear activity levels:
   - **Highly Active** (10k+ steps): Need advanced analytics & performance tracking
   - **Moderately Active** (5–10k steps): Benefit from progress tracking & achievable milestones
   - **Low Activity** (<5k steps): Require gentle reminders, micro-goals, and encouraging content

3. **Sleep Quality Gap:** Average sleep duration (~7 hours) is acceptable, but poor **sleep efficiency** means some users visibly lose 30+ minutes in bed without sleeping. Users could feel more rested with the same time investment by improving efficiency.

---

## 🎯 Recommendations

1. **"Beyond Steps" Campaign** — Market Bellabeat's holistic health tracking as superior to step-only trackers. Message: "Your fitness tracker counts steps. Bellabeat transforms your entire day." Target all user segments with emphasis on sedentary break alerts.

2. **Segment-Specific Onboarding** — Customize app experience based on initial activity assessment:
   - Highly Active → Advanced analytics, performance trends, competitive challenges
   - Moderately Active → Progress tracking, streak rewards, achievable milestones
   - Low Activity → Gentle reminders, micro-goals, educational content

3. **"Sleep Smarter" Feature Set** — Emphasize sleep efficiency metrics over just duration. Market Bellabeat's ability to identify environmental factors (temperature, light, noise) affecting sleep quality. Create shareable "Sleep Score" to encourage engagement.

4. **Product Development Priorities:**
   - **Sedentary Break Alerts:** Smart notifications that learn user patterns
   - **Sleep Environment Monitoring:** Integrations for temperature, light, and sound tracking
   - **Personalized Insights Engine:** ML-driven segment-appropriate recommendations

---

## ⚠️ Data Limitations

- **Small sample size** (33 users for activity, 24 for sleep) may not fully represent Bellabeat's target demographic
- **One-month observation window** (April–May 2016) limits understanding of long-term or seasonal behavior patterns
- **No demographic data** (age, gender, lifestyle) prevents deeper segmentation
- **Missing compliance context:** No data on device-wearing consistency or measurement accuracy

---

## 🔄 How to Reproduce Results

1. Open [bellabeat_wellness_analysis.ipynb](notebooks/bellabeat_wellness_analysis.ipynb) in Jupyter or VS Code
2. Ensure Python packages are installed: `pandas`, `matplotlib`, `seaborn`, `statsmodels`
3. Verify dataset paths point to `data/raw/fitabase_4.12.16-5.12.16/`
4. Run all cells from top to bottom
5. Review visualizations and insights in-notebook

---

## 📈 Next Steps

- Survey existing Bellabeat users to validate findings and gather demographic context
- Conduct A/B testing on segment-specific messaging to measure engagement impact
- Analyze seasonal variations in activity and sleep patterns for better feature timing
- Investigate correlations between sleep efficiency and next-day activity levels