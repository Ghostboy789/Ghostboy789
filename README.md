<p align="center">
  <img src="assets/header.svg" alt="Medhansh Shekhawat. Credit risk, data analytics and product. I build models, then write down what would prove them wrong before I look." width="900">
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/medhansh-shekhawat/"><img src="https://img.shields.io/badge/LinkedIn-medhansh--shekhawat-0a66c2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <img src="https://img.shields.io/badge/based_in-Bangalore_·_Pune-30363d?style=flat-square" alt="Bangalore and Pune">
  <img src="https://img.shields.io/badge/open_to-credit_risk_·_data_·_product_analyst-238636?style=flat-square" alt="Open to credit risk, data analyst and product analyst roles">
</p>

Every project below has a validation plan written **before** the first result, and each one reports the checks it failed.

## Projects

<a href="https://vintage-credit-risk.vercel.app"><img src="assets/card-vintage.svg" alt="Vintage: credit-risk pack on 1.3M Freddie Mac loans. Out-of-time Gini 0.53, ECL $272.4m on $80.0bn, 143 tests." width="900"></a>

<p align="center"><b><a href="https://vintage-credit-risk.vercel.app">Live site</a></b> · <a href="https://vintage-credit-risk.vercel.app/powerbi">Power BI report</a> · <a href="https://github.com/Ghostboy789/vintage-credit-risk">Code</a> · <a href="https://github.com/Ghostboy789/vintage-credit-risk/blob/main/docs/COMMITTEE_MEMO.md">Committee memo</a></p>

<a href="https://pitwall-f1-strategy.onrender.com"><img src="assets/card-pitwall.svg" alt="Pit Wall: F1 race-strategy model from 185 races. A place on track is worth at least 8.7 times more at Monaco than at COTA. Overtaking AUC 0.915, 118 tests." width="900"></a>

<p align="center"><b><a href="https://pitwall-f1-strategy.onrender.com">Live dashboard</a></b> · <a href="https://github.com/Ghostboy789/pitwall-f1-strategy">Code and validation plan</a></p>

<a href="https://limitiq-credit-line-optimization.onrender.com"><img src="assets/card-limitiq.svg" alt="LimitIQ: credit-line decision system. ROC-AUC 0.781 (CI 0.767–0.796), Brier 0.133, 161 tests." width="900"></a>

<p align="center"><b><a href="https://limitiq-credit-line-optimization.onrender.com">Live app</a></b> · <a href="https://github.com/Ghostboy789/limitiq-credit-line-optimization">Code and governance docs</a></p>

<p align="center"><sub>Pit Wall and LimitIQ run on a free tier: the first load can take up to a minute to wake.</sub></p>

<details>
<summary><b>The part I'd want a risk person to read</b></summary>
<br>

- **Vintage.** The scorecard ranks risk out of time (Gini 0.5336 [0.5055, 0.5625]) but six of seven grades fail out-of-time calibration. The overall ratio looks fine only because two windows err in opposite directions. The LightGBM challenger lost to a pre-set promotion rule and was not promoted. The memo recommends research use only.
- **Pit Wall.** The optimiser claimed 17.6 s per car against a 2.0 s limit. After four rounds of real bug fixes I stopped, because tuning until a pre-registered check passes defeats the check. The cause: the simulator charges +9.9 s [+2.3, +17.3] for an extra pit stop that real races price at roughly nothing.
- **LimitIQ.** Version one gave all 288 eligible accounts the maximum +30%: a corner solution from my own linear maths. Fixing it cut the headline contribution by 85%. A calibration challenge "won" by 0.00004 Brier with an interval crossing zero, so I didn't promote it.

</details>

## Toolkit

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white" alt="SQL">
  <img src="https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white" alt="dbt">
  <img src="https://img.shields.io/badge/DuckDB-FFF000?style=flat-square&logo=duckdb&logoColor=black" alt="DuckDB">
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" alt="scikit-learn">
  <img src="https://img.shields.io/badge/LightGBM-2c3e50?style=flat-square" alt="LightGBM">
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black" alt="Power BI">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker">
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions">
</p>

**Methods:** WoE/IV scorecards · IFRS 9 ECL · probability calibration · bootstrap intervals · survival and censoring · model validation

<p>
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=Ghostboy789&show_icons=true&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=39d0c8&text_color=c9d1d9&count_private=true" alt="GitHub stats">
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Ghostboy789&layout=compact&hide_border=true&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9" alt="Top languages">
</p>

## Other work

| Project | What it is |
|---|---|
| [Financial fraud detection](https://github.com/Ghostboy789/Advanced-Model-For-Financial-Fraud-Detection) | Co-authored a **filed** patent application and a published paper on the approach with a faculty advisor |
| [TikTok claims classification](https://github.com/Ghostboy789/TikTok-Analysis-Project) | Claim-vs-opinion modelling on a large annotated corpus |
| [Salifort Motors attrition](https://github.com/Ghostboy789/Salifort-Motors) | Attrition modelling and driver analysis |
| [Healthcare dashboard](https://github.com/Ghostboy789/Healthcare-Dashboard) · [Housing market analysis](https://github.com/Ghostboy789/Housing-market-analysis-using-tableau) | Analytics and visualisation work |

## About

Product Manager Intern, moving into **credit risk and data analytics**. B.Tech Computer Engineering, DY Patil University, 2026. I write the brief at work; these projects are where I do the model-layer work myself.

Open to credit risk, data analyst and product analyst roles in **Bangalore and Pune**.
