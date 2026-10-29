# Inflation Macro Monitor

An institutional surveillance dashboard tracking headline, core, underlying, and market-implied inflation across official and alternative data feeds.

## Key Features
- **Official Price Indices**: CPI & PCE breakdowns across goods, services, and shelter (with switchable $y/y$, $3\text{m}$ annualized, and uncompounded $m/m$ views).
- **Underlying Measures**: Trimmed-mean and median measures (Dallas Fed Trimmed PCE, Cleveland Fed Median/Trimmed CPI, Atlanta Fed Sticky CPI).
- **Shelter & Pipeline Tracking**: Zillow Observed Rent Index (ZORI) vs. CPI shelter stock, NY Fed GSCPI, and Regional Fed price diffusion metrics (NY Fed & Philly Fed).
- **Market Expectations**: TIPS breakevens (5y, 10y, 5y5y forward) and live Kalshi CPI probability distribution with the 50% toss-up threshold highlighted.
- **Activity Heatmap**: Standardized $z$-score grid relative to 2015–2019 pre-pandemic baselines. Thermal colors: Blue = cool/below trend, Red = hot/expansion.
- **Data & Image Export**: Every chart includes client-side `⤓ PNG` (complete with title, subtitle, active color legend, and source stamp) and `⤓ CSV` export buttons.

## Data Sources
- **FRED API**: BLS, BEA, Federal Reserve Board, and Regional Federal Reserve Banks.
- **Zillow Research**: ZORI marginal rent index.
- **Indeed Hiring Lab**: Wage growth tracker (3mma).
- **Kalshi Exchange**: Event contract market pricing.

## Quickstart
1. Set `FRED_API_KEY` in your environment or Google Colab Secrets (🔑).
2. Run the script:
   ```bash
   python fetch.py && python compute.py && python render.py
