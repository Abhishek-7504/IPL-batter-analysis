# IPL-batter-analysis

This repository contains code and resources for analyzing batting intent in IPL 2025 matches using ball-by-ball data. The analysis classifies batting phases (Powerplay, Middle Overs, Death Overs) and computes key metrics such as strike rate, boundary percentage, dot-ball percentage, and over-wise scoring trends to uncover strategic insights.

Raw Data: Ball-by-ball deliveries with columns such as over, ball, batter, bowler, runs_off_bat, wicket_type, etc.

Phase Classification: Implemented in preprocess.py via a get_phase() function:
* Powerplay: Overs 0–5
* Middle Overs: Overs 6–14
* Death Overs: Overs 15+

Analysis Modules

* Strike Rate Analysis : Group by batter & phase to compute balls faced, total runs, and strike rate (runs/balls × 100).

* Boundary vs. Dot-Ball : Annotate deliveries as Boundary, Dot, or Run, and calculate percentages for batters with ≥ 10 deliveries.

* Over-Wise Scoring Trends : Aggregate runs and wickets per over to profile momentum shifts.

Visualizations are built with Plotly for interactive charts:
* Bar Charts: Phase-wise strike rate comparisons.
* Radar Charts: Boundary & dot-ball profiles per batter.
* Line Charts: Over-wise scoring and wickets trends.

Sample Results

* Top Powerplay Aggressors: Players with strike rate > 140 in overs 0–5.
* Death Overs Finishers: High-strike-rate batters (> 220) in overs 15+.
* Boundary vs. Dot-Ball Profiles: Visual clusters showing risk-reward trade-offs.
