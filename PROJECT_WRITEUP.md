# The Evolution of Pitching and Hitting in MLB

## Research Question
To what extent have changes in modern pitching affected batting average and offensive production in Major League Baseball from 2000 to 2025?

## Context
Modern MLB pitching has emphasized velocity, strikeouts, pitch specialization, and data-driven strategy. This exploratory analysis tests whether league-season changes in strikeout rate and four-seam fastball velocity are associated with batting average and OPS.

## Data
The MLB Stats API supplies traditional hitting and pitching season statistics for 2000–2025. Baseball Savant supplies four-seam fastball velocity for 2008–2025. The unit of analysis is the MLB league-season. The traditional dataset has 26 seasons and the velocity-overlap dataset has 18 seasons.

## Variables
- AVG = hits / at-bats
- OBP = (H + BB + HBP) / (AB + BB + HBP + SF)
- SLG = total bases / at-bats
- OPS = OBP + SLG
- K% = strikeouts / batters faced × 100
- K/9 = strikeouts per nine innings
- Fastball velocity = average four-seam fastball velocity in MPH

## Preparation
Player-level season records were aggregated to league-season totals. Pitching innings were converted to outs before calculating K/9 because baseball notation such as 5.2 represents five innings and two outs. Hitting and pitching tables were merged on Year, followed by the velocity merge for 2008–2025. Missing-value checks were performed.

## Findings
From 2008 to 2025, average four-seam velocity increased 2.50 MPH, K% increased 4.69 percentage points, AVG decreased 0.019, and OPS decreased 0.030. Correlations were r = -0.263 for velocity vs. OPS, r = -0.932 for K% vs. AVG, and r = -0.581 for K% vs. OPS.

The strongest association in this analysis is between strikeout rate and batting average. Velocity alone has a much weaker relationship with OPS, suggesting that pitch velocity is only one part of the broader changes in modern pitching.

## Limitations and Ethics
The analysis uses public statistics and no sensitive personal information. It is observational and cannot establish causation. League-season results should not be generalized to individuals. Velocity begins in 2008, and pitch-tracking measurement systems changed over time. Hitter approach, pitch selection, defensive positioning, rules, baseball composition, and league strategy may also influence offense.

## Academic Sources
Mercier, M.-A., Tremblay, M., Daneau, C., & Descarreaux, M. (2020). Individual factors associated with baseball pitching performance: Scoping review. *BMJ Open Sport & Exercise Medicine, 6*(1), e000704. https://doi.org/10.1136/bmjsem-2019-000704

Slowik, J. S., Aune, K. T., Diffendaffer, A. Z., Cain, E. L., Dugas, J. R., & Fleisig, G. S. (2019). Fastball velocity and elbow-varus torque in professional baseball pitchers. *Journal of Athletic Training, 54*(3), 296–301. https://doi.org/10.4085/1062-6050-558-17

Manzi, J. E., Dowling, B., Wang, Z., Sudah, S. Y., Moran, J., Chen, F. R., Estrada, J. A., Nicholson, A., Ciccotti, M. G., Ruzbarsky, J. J., & Dines, J. S. (2024). Kinematic modeling of pitch velocity in high school and professional baseball pitchers: Comparisons with the literature. *Orthopaedic Journal of Sports Medicine, 12*(8). https://doi.org/10.1177/23259671241262730

## AI Transparency
Generative AI was used as a coding and writing support tool during project development. It helped troubleshoot Python/API errors, explain code logic, improve organization and wording, and suggest ways to communicate findings. The student reviewed the code, calculations, visualizations, interpretations, and final written material.
