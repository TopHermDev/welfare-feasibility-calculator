# Welfare Scheme Feasibility Calculator

A single-page, dependency-free calculator for sectorial welfare funds: enter membership,
contributions, benefit incidence rates and fund-management assumptions, and it reports
whether contribution income can sustainably cover expected welfare outgo.

## What it computes

- **Annual contribution income** — members × monthly contribution × 12
- **Expected claims per benefit category** — members × incidence rate × average benefit
  (birth, bereavement, medical, marriage, other — modelled separately, not as one blended rate)
- **Funding ratio** — annual contribution income ÷ annual welfare outgo
  (below 1.00 indicates an expected annual deficit)
- **Status** — `FEASIBLE`, `FEASIBLE — LOW MARGIN` (ratio < 1.10), or `NOT FEASIBLE`
- **Projected year-end fund** — starting fund + surplus − retirement payments + investment return

## Scenarios

| Scenario | Effect |
|---|---|
| Expected | rates as entered |
| Conservative | claim incidence +25% |
| Stress | claim incidence +60%, benefit size +10% |

Retirement obligations are displayed **separately** from the welfare funding ratio,
because current welfare cash flow does not by itself prove future retirement
obligations are funded.

## Usage

Open `index.html` in any browser — no build step, no server, no network calls.
All computation runs client-side in vanilla JavaScript.

## Caveat

This is a planning model, not a formal actuarial valuation. Replace the illustrative
incidence rates with the scheme's own historical experience, and model retirement from
the member age distribution, mortality, benefit rules and investment assumptions.

## Related

Companion article: *From Welfare Contributions to Sustainability: A Simple Model for
Predicting the Future of Sectorial Welfare Funds* — jawotwi.top
