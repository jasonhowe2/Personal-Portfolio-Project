# DTSC 2301 Code Review Guide

Use this outline during the required 10–15 minute instructor/TA code review.

1. **Question:** Explain the research question and why MLB pitching and offense are interesting to compare.
2. **Sources:** MLB Stats API for 2000–2025 traditional statistics and Baseball Savant for four-seam velocity from 2008–2025.
3. **Unit of analysis:** One MLB league-season.
4. **Variables:** AVG, OBP, SLG, OPS, K%, K/9, and four-seam fastball velocity.
5. **API collection:** Explain that hitting and pitching season records were collected with `MLB-StatsAPI`.
6. **Aggregation:** Explain that player-season records were summed to create league-season totals.
7. **Important coding decision:** Baseball innings notation is converted to outs because 5.2 means five innings and two outs, not 5.2 mathematical innings.
8. **Merge:** Hitting and pitching tables are merged on Year; velocity is then merged for 2008–2025.
9. **Quality checks:** Explain the missing-value checks and the resulting complete analyzed variables.
10. **Visualizations:** Figure 1 shows K% and AVG over time; Figure 2 directly examines velocity vs. OPS.
11. **Results:** Velocity vs. OPS r = -0.263; K% vs. AVG r = -0.932; K% vs. OPS r = -0.581.
12. **Interpretation:** K% has a stronger association with offensive decline than velocity alone.
13. **Limitations:** Correlation is not causation; league-season analysis cannot establish individual-level effects; velocity is available only from 2008; other MLB changes matter.
14. **AI transparency:** Explain that AI helped with troubleshooting, code explanations, organization, wording, and communication, while the student reviewed the final work.

**Reminder:** The instructor/TA review itself must be completed by the student; this guide prepares the student for that conversation but does not replace it.
