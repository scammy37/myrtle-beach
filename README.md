# Ocean Keyes Investment Explorer

An interactive tool for evaluating a condo purchase at **Ocean Keyes, North Myrtle Beach** as a self-managed short-term rental. Tap a scenario, fine-tune the sliders, and watch year-one cash flow, a multi-year projection, and profit-at-sale recompute live.

**Live site:** once GitHub Pages is enabled → <https://scammy37.github.io/myrtle-beach/>

## What it does

- **One-tap scenarios** — unit (2BR / 3BR), financing (all cash → 10% down), rental intensity (light / base / max), appreciation (flat / 3% / 5%), plus four full strategy presets.
- **Year-one P&L** — gross rental, taxes, HOA, insurance, management/booking fees, mortgage, net operating income, cash flow, cap rate, cash-on-cash.
- **Multi-year projection** — property value, loan balance, equity, and cumulative cash flow across an adjustable hold period.
- **Profit at sale** — appreciation + loan paydown + cumulative cash flow − selling costs, with annualized return.
- **Self-contained SVG charts** — equity build-up, cumulative cash flow, and a total-return breakdown. No external libraries; works offline.

## Spreadsheet model

`ocean-keyes-buyside-model.xlsx` is the underlying buy-side model in spreadsheet form — a 2BR/2BA, self-managed short-term-rental underwrite you can edit in Excel, Numbers, or Google Sheets.

- **Buy-Side Model** sheet — purchase & financing (price, down payment, rate, term, P&I), total cash invested (closing costs + furnishing), annual operating assumptions (HOA, second-home property tax, STR insurance, electric, cleaning slippage, supplies, permit, capital reserve, booking-fee and R&M percentages), and a three-column pro forma (Conservative / Base / Optimistic) running gross revenue → operating expenses → NOI → debt service → pre-tax cash flow.
- **Return metrics** — cap rate, cash-on-cash, DSCR, break-even gross revenue, plus a memo line for the management fee avoided by self-managing.
- **Notes & Sources** sheet — assumptions, the two must-verify inputs (exact HOA/regime fee and the Horry County tax estimate at the 6% second-home ratio), the accommodations-tax pass-through treatment, what the model excludes (appreciation, principal paydown, tax effects, special assessments), and source list.

Cells are color-coded: blue = your inputs, yellow = verify before relying on it, black = calculated. Every figure is a live formula, so changing an input recomputes the scenarios.

## Data sources

Defaults are grounded in AirDNA / AirROI short-term-rental data, Coastal Carolinas MLS sold comps, Horry County (SC) property-tax rules (6% second-home ratio), and August 2026 mortgage rates. They are estimates for planning, not quotes or financial advice.

## Running locally

It's a single static file. Just open `index.html` in any browser — no build step, no dependencies.

## Deploy on GitHub Pages

1. Push this repo to GitHub.
2. Repo **Settings → Pages → Build and deployment → Source: Deploy from a branch**.
3. Branch: `main`, folder: `/ (root)`. Save.
4. Wait ~1 minute; your live URL appears at the top of the Pages settings.
