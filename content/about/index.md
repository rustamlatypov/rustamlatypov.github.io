---
title: "Automated Business Cycle Dashboard"
author: [Rustam Latypov]
description: "This dashboard provides real-time charts on US unemployment rate, vacancy rate, labor market tightness, FERU, unemployment gap, and recession probability."
cover:
    image: /dashboard.png
    alt: "US recession probability from dual-threshold Michez rule"
editPost:
    URL: https://github.com/pmichaillat/pmichaillat.github.io/blob/main/content/dashboard/dashboard.py
    Text: "Source code"
showToc: true
disableAnchoredHeadings: false

---

This dashboard provides real-time indicators of labor market slack and business cycle conditions in the United States. All charts automatically update as new data become [available on FRED](https://fred.stlouisfed.org/).

## Unemployment rate

+ [View in full screen](/dashboard/unemployment_rate.html)
+ [Download unemployment rate](/dashboard/unemployment_rate.csv)
+ *Construction* - The unemployment rate is the number of job seekers divided by the number of labor force participants.
+ *Interpretation* - The unemployment rate measures the share of people who have not succeeded in finding a job, among all those who are available and willing to work. This is the standard, official unemployment rate (U3).
+ *Source* - The numbers of [job seekers](https://fred.stlouisfed.org/series/UNEMPLOY) and [labor force participants](https://fred.stlouisfed.org/series/CLF16OV) are measured by the US Bureau of Labor Statistics (BLS) from the [Current Population Survey](https://www.bls.gov/cps/home.htm) (CPS), which is a large-scale household survey.

This dashboard provides real-time indicators of labor market slack and business cycle conditions in the United States. All charts automatically update as new data become [available on FRED](https://fred.stlouisfed.org/).
