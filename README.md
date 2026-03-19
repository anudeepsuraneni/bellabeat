# How Can a Wellness Technology Company Play It Smart?

**Bellabeat — Capstone for Google Data Analytics Professional Certificate**

---

## 🎯 Business Question

Bellabeat is a high-growth wellness technology company targeting women. To fuel its next marketing push, leadership needs to understand: **how are people actually using smart wellness devices today — and what does that reveal about unmet needs Bellabeat can address?** Using publicly available FitBit usage data as a proxy for smart device behavior, this analysis surfaces behavioral patterns across activity and sleep to inform Bellabeat's positioning and product marketing strategy.

---

## 📊 Project Resources

- **[Data Analysis Notebook](notebooks/bellabeat_wellness_analysis.ipynb)** — Complete R-based analysis with data transformation and insights
- **[Google Slides Presentation](https://docs.google.com/presentation/d/1RmR7E-n8LG3ChkKzMdp_hvu58NEcJupVKOYmFJNkl4g)** — Executive summary and strategic recommendations for stakeholders

---

## 📁 Project Structure

```
bellabeat/
├── README.md                                 # Project overview and guide
├── notebooks/
│   └── bellabeat_wellness_analysis.ipynb     # Main R-based analysis notebook
└── data/
    └── raw/
        └── fitabase_4.12.16-5.12.16/         # FitBit fitness tracker dataset
            ├── dailyActivity_merged.csv      # Daily activity metrics
            └── sleepDay_merged.csv           # Sleep tracking data
```

---

## 📋 Data Sources & Ethics

- **Source:** [FitBit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit) (CC0: Public Domain, Kaggle dataset)
- **Sample:** 30 FitBit users who consented to share personal tracker data (April–May 2016)
- **Privacy:** Analysis uses only aggregated metrics with no personal identifiers; user consent obtained
- **Credibility:** Kaggle usability score of 9.41; publicly available for reproducibility
- **Limitation:** 30-user sample from 2016 — findings are directional, not statistically representative. Validated against general wellness research where possible.

---

## 🔍 Methodology

### Why These Variables?

Activity and sleep were selected as the primary dimensions because they're Bellabeat's core product value proposition — and because they're where wearables most commonly underdeliver on insight (tracking the metric without explaining what to do about it). Sedentary time was specifically added as a derived variable because step count alone masks a critical health risk: users can hit step goals while remaining sedentary for the majority of the day.

Sleep efficiency (time asleep ÷ time in bed) was computed rather than relying on raw sleep duration because duration is a poor proxy for sleep quality — a distinction Bellabeat's marketing can own.

### Data Preparation & Cleaning

- Loaded daily activity (940 observations) and sleep datasets (413 observations)
- Validated data quality: no missing values in primary fields; removed duplicate records
- Created derived features:
  - **Sleep efficiency** = total minutes asleep ÷ total time in bed — captures restlessness that raw duration hides
  - **Activity segments** = three tiers based on daily step count (10k+, 5–10k, <5k) — enables segment-specific recommendations
  - **Temporal variables** = day of week, hour — for behavioral rhythm analysis

### Visualization Approach

- Custom color palettes aligned to Bellabeat brand identity — analysis was positioned as a stakeholder-facing deliverable, not just exploratory
- Trend smoothing applied to daily patterns to reduce noise and surface underlying rhythms
- Diagonal reference line on sleep efficiency scatter plot — visually encodes the "perfect efficiency" benchmark, making the gap immediately visible

---

## 💡 Key Findings

1. **The Sedentary Paradox:** Users average **16.5 hours of sedentary time daily** — even those consistently hitting 10,000+ steps. This means step count, the metric most fitness trackers lead with, is masking a significant health risk. Active users are not necessarily healthy users.

2. **Three Distinct User Segments:** Activity data clusters into clear behavioral tiers with different needs:
   - **Highly Active** (10k+ steps, ~21% of users): Already engaged — want performance depth and competitive features
   - **Moderately Active** (5–10k steps, ~43% of users): Responsive to progress framing and achievable milestones
   - **Low Activity** (<5k steps, ~36% of users): Need low-friction nudges and encouraging content, not metrics overload

3. **Sleep Quality Gap:** Average sleep duration (~7 hours) looks acceptable — but sleep efficiency tells a different story. Users lose an average of **30+ minutes per night** to restlessness or delayed sleep onset. The problem isn't time in bed; it's the quality of that time. This is an insight most trackers don't surface.

---

## 🎯 Recommendations

1. **"Beyond Steps" Campaign** — Lead Bellabeat's marketing with sedentary break awareness. The message: step count is an incomplete health signal. Bellabeat tracks your whole day, not just your active minutes. This directly differentiates from competitors who lead with steps and distance.

2. **Segment-Specific Onboarding** — Match the app experience to the user's actual behavior profile from day one:
   - Highly Active → Advanced analytics, performance trends, challenge features
   - Moderately Active → Progress tracking, streak rewards, milestone framing
   - Low Activity → Gentle reminders, micro-goals, educational content — never raw metrics

3. **"Sleep Smarter" Positioning** — Shift the sleep narrative from duration to efficiency. Market Bellabeat's ability to identify what's disrupting sleep quality (environment, stress, activity timing) rather than just measuring hours. A shareable "Sleep Score" drives engagement and social proof.

---

## 📈 Impact

This analysis reframes Bellabeat's competitive positioning around two overlooked gaps in the current wearable market: the sedentary blind spot in activity tracking and the duration-vs-efficiency gap in sleep tracking. Both represent specific, data-backed claims Bellabeat can own in its marketing. The three-segment user model provides a direct input to product and marketing teams — enabling personalized onboarding, targeted campaigns, and feature prioritization grounded in observed behavior rather than assumptions.

---

## 🔄 How to Reproduce Results

1. Open [bellabeat_wellness_analysis.ipynb](notebooks/bellabeat_wellness_analysis.ipynb) in RStudio or Jupyter with R kernel
2. Ensure R packages are installed: `tidyverse`, `lubridate`
3. Verify dataset paths point to `data/raw/fitabase_4.12.16-5.12.16/`
4. Run all cells from top to bottom
5. Review visualizations and insights in-notebook

---

## 📌 Next Steps

- Survey existing Bellabeat users to validate the three-segment model and gather demographic context
- Conduct A/B testing on segment-specific messaging to measure engagement and retention impact
- Investigate correlations between sleep efficiency and next-day activity levels — potential for a "recovery score" feature
- Analyze seasonal patterns across a longer data window to time feature marketing more precisely
