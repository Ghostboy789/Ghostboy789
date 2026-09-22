<p align="center">
  <img src="assets/header.svg?v=2" alt="Terminal: Medhansh Shekhawat, product manager moving into credit risk analytics. Projects: Pit Wall, an F1 strategy model validated against a plan written first; LimitIQ, a live credit-line decision system." width="900">
</p>

<p align="center">
  <img src="assets/neofetch.svg?v=2" alt="Profile summary: role, focus, the two projects and their results, evidence, scope, stack." width="900">
</p>

---

### `Pit Wall` — an F1 strategy model that failed the test I wrote for it first

Before a single result existed, I wrote down the number that would call the model broken: if the
strategy optimiser claimed to beat professional race strategists by more than **2 seconds** a car,
it was wrong, not brilliant.

It claimed **17.6**. Four rounds of genuine bug fixes walked that down 23.5 → 21.3 → 20.4 → 17.7,
and then I stopped fixing — adjusting a model until a pre-registered check passes is how such a
check gets quietly defeated. So I localised the failure instead. The simulator charges **+9.9 s
[+2.3, +17.3]** for an extra pit stop that real races price at roughly nothing, because it runs
every car flat out on its fitted wear rate while real drivers manage the tyre. **The per-team and
per-driver strategy audit that depended on the optimiser is not published.**

| | |
|---|---|
| **Data** | 185 races · 203,644 laps of public timing data |
| **What passed** | Overtaking model, out-of-fold by race: AUC **0.915** · Brier 0.0487 · ECE 0.0025 on 64,646 opportunities |
| **The finding** | A place on track is worth **≥ 8.7×** more at Monte Carlo than at the Circuit of the Americas — and those two are statistically separable while adjacent circuits are not, which is also reported |
| **The hard part** | Teams pit when a tyre is finished, so wear is censored non-randomly — uncorrected data says hard tyres wear *faster* than soft. Censoring weights fix 11/29 circuits to 21/29 |
| **Ships as** | 7 interactive dashboards, a 5-page Power BI report on a star schema checked against the pipeline by 48 DAX queries, and 118 tests |

Two calibrated fixes for the failed gate were **rejected**: each matched the quantity it was fitted
to and missed the one it wasn't, and one made the gate worse.

The reason this sits next to a credit model: censoring and survivorship, calibration over
discrimination, partial pooling for thin segments, and effective challenge are the same problems a
PD model has, wearing a different set of tyres.

**[Live dashboard](https://pitwall-f1-strategy.onrender.com)** · **[Code, methodology and validation plan](https://github.com/Ghostboy789/pitwall-f1-strategy)**
<br><sub>Free tier — the first load can take up to a minute to wake. Independent analysis of public timing data, not affiliated with Formula 1, the FIA or any team.</sub>

---

### `LimitIQ` — a credit-line decision system that documents why you shouldn't trust it

I spent weeks building it. Then I made its headline number **85% smaller**.

The first version reported ₹2.98M of incremental contribution. The action distribution gave it
away: **all 288 eligible accounts were getting the maximum 30% increase.** That isn't an
optimiser, it's a threshold rule in a costume. The cause was my own maths — a contribution
function linear in the size of the increase, so the optimum was always a corner.

Adding response saturation and risk-dependent drawdown spread the decisions to 157 at +10%
and 37 at +20%, and dropped contribution to **₹454,414**. That second number is the one I trust.

| | |
|---|---|
| **Model** | Sigmoid-calibrated histogram gradient boosting, next-month default |
| **Test** | ROC-AUC **0.781** (bootstrap CI 0.767–0.796) · PR-AUC 0.568 · Brier 0.133 |
| **Discipline** | Frozen 18k/6k/6k split · test set read **once** · threshold fixed on validation first |
| **Decisions** | Constrained +10/+20/+30%, hold, review, freeze under exposure, loss, capital and customer-protection limits |
| **Governance** | Model card · validation review mapped to Fed SR 26-2 · 12-item issue ledger · randomised pilot design |

A calibration challenge picked isotonic as the winner — by 0.00004 Brier score. The confidence
interval crossed zero, so **I didn't promote it.** Choosing a calibrator after seeing the
comparison needs a fresh holdout I don't have. That decision is the part I'd most want a risk
person to read.

**What it is not.** The data is Taiwan, 2005. There is no Indian validation and this is not a
regulatory or IFRS 9 PD. Every rupee of economics is **simulated**, because no public dataset
observes what happens when you actually raise someone's limit — which is why the repo ships a
randomised pilot design instead of an uplift number. Five validation findings stay open because
they cannot be closed without real institutional data. It is **educational, and not for real
lending decisions.**

**[Live app](https://limitiq-credit-line-optimization.onrender.com)** · **[Code and governance docs](https://github.com/Ghostboy789/limitiq-credit-line-optimization)**
<br><sub>Free tier — the first load can take up to a minute to wake.</sub>

---

### Other work

| Project | What it is |
|---|---|
| [Financial fraud detection](https://github.com/Ghostboy789/Advanced-Model-For-Financial-Fraud-Detection) | Co-authored a **filed** patent application and a published paper on the approach with a faculty advisor |
| [TikTok claims classification](https://github.com/Ghostboy789/TikTok-Analysis-Project) | Claim-vs-opinion modelling on a large annotated corpus |
| [Salifort Motors attrition](https://github.com/Ghostboy789/Salifort-Motors) | Attrition modelling and driver analysis |
| [Healthcare dashboard](https://github.com/Ghostboy789/Healthcare-Dashboard) · [Housing market analysis](https://github.com/Ghostboy789/Housing-market-analysis-using-tableau) | Analytics and visualisation work |

---

### About

Product management intern at GaragePlug, moving toward **credit risk analytics and model
development**. I built LimitIQ to find out whether I could do the model-layer work myself
rather than only writing the brief for it, and Pit Wall to find out what happens when you
write the validation plan before the results — and then publish the run that failed it.

Open to credit risk analyst, risk analytics and model development roles in Pune and Mumbai.

**[LinkedIn](https://www.linkedin.com/in/medhansh-shekhawat/)**
