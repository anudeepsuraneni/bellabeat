# How Can a Wellness Technology Company Play It Smart?

**Bellabeat — Capstone for Google Data Analytics Professional Certificate**

A comprehensive analysis of smart device usage data to uncover behavioral patterns and inform strategic marketing decisions. This project demonstrates end-to-end data analysis: preparation, processing, exploratory analysis, visualization, and actionable recommendations for a high-tech wellness company.

---

## 📊 Project Resources

- **[Data Analysis Notebook](notebooks/bellabeat_wellness_analysis.ipynb)** — Complete R-based analysis with data transformation and insights
- **[Google Slides Presentation](https://docs.google.com/presentation/d/1RmR7E-n8LG3ChkKzMdp_hvu58NEcJupVKOYmFJNkl4g)** — Executive summary and strategic recommendations for stakeholders

---

## 📁 Project Structure

```
bellabeat/
├── README.md                                  # Project overview and guide
├── bellabeat_wellness_analysis.ipynb          # Main R-based analysis notebook
└── data/
    └── raw/
        └── fitabase_4.12.16-5.12.16/         # FitBit fitness tracker dataset
            ├── dailyActivity_merged.csv       # Daily activity metrics
            ├── sleepDay_merged.csv            # Sleep tracking data
            └── [other CSV files...]
```

---

## 📋 Data Sources & Ethics

- **Source:** [FitBit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit) (CC0: Public Domain, Kaggle dataset)
- **Sample:** 30 FitBit users who consented to share personal tracker data (April-May 2016)
- **Privacy:** Analysis uses only aggregated metrics with no personal identifiers; user consent obtained
- **Credibility:** Kaggle usability score of 9.41; publicly available for reproducibility
- **Usage:** Data analyzed to understand non-Bellabeat smart device patterns applicable to Bellabeat's product strategy

---

## 🔍 Analysis Overview

### Data Preparation & Cleaning
- Loaded daily activity and sleep datasets (940 and 413 observations respectively)
- Validated data quality (no missing values, removed duplicates if present)
- Created derived features: sleep efficiency, activity segments, temporal variables

### Key Metrics Analyzed
- **Activity patterns:** Daily steps, sedentary minutes, activity intensity levels
- **Sleep quality:** Total sleep duration, time in bed, sleep efficiency percentage
- **User segmentation:** Three activity tiers based on step counts (10k+, 5-10k, <5k)
- **Behavioral relationships:** Correlation between steps and sedentary time, sleep efficiency patterns

### Visualization Approach
- Custom color palettes for brand alignment
- Trend smoothing to identify patterns
- Segment-based histograms for audience targeting
- Sleep efficiency scatter plots with diagonal reference lines

---

## 💡 Key Findings

1. **The Sedentary Paradox:** Users average **16.5 hours of sedentary time daily**, even those hitting 10,000+ steps. Step count alone doesn't capture total health—active users can still be highly sedentary.

2. **Three Distinct User Segments:** Behavior clusters into clear activity levels:
   - **Highly Active** (10k+ steps): Need advanced analytics & performance tracking
   - **Moderately Active** (5-10k steps): Benefit from progress tracking & achievable milestones
   - **Low Activity** (<5k steps): Require gentle reminders, micro-goals, and encouraging content

3. **Sleep Quality Gap:** Average sleep duration (~7 hours) is acceptable, but poor **sleep efficiency** means users lose 30+ minutes to restlessness or difficulty falling asleep. Users could feel more rested with same time investment by improving efficiency.

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

## 🔄 How to Reproduce Results

1. Open [bellabeat_wellness_analysis.ipynb](notebooks/bellabeat_wellness_analysis.ipynb) in RStudio or Jupyter with R kernel
2. Ensure R packages are installed: `tidyverse`, `lubridate`
3. Verify dataset paths point to `data/raw/fitabase_4.12.16-5.12.16/`
4. Run all cells from top to bottom
5. Review visualizations and insights in-notebook

---

## 📈 Next Steps

- Survey existing Bellabeat users to validate findings and gather demographic context
- Conduct A/B testing on segment-specific messaging to measure engagement impact
- Analyze seasonal variations in activity and sleep patterns for better feature timing
- Investigate correlations between sleep efficiency and next-day activity levels
- Develop prototype sleep environment monitoring features for beta testing
