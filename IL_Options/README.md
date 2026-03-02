# IL_Options - Cross-Asset Regime Intelligence

Unified options surface dashboard for macro funds trading both TradFi and crypto. Identifies regime shifts, cross-asset dislocations, and positioning asymmetries through the vol surface.

## What This Is

A cross-asset regime identification system that uses options-implied metrics across equities, commodities, bonds, and digital assets to detect:

- **Regime shifts** - When BTC stops trading like QQQ and starts trading like GLD
- **Skew velocity** - Speed of positioning changes across 1D/1W/2W/1M/1Q timeframes
- **Vol dislocations** - Cross-asset spreads at extreme Z-scores
- **Carry opportunities** - IV vs RV harvesting signals

## Core Thesis

BTC doesn't trade in a crypto vacuum. It rotates between behaving as a leveraged Nasdaq proxy, digital gold, and its own beast. The options surface reveals when those regime shifts happen before spot confirms.

## Dashboard Sections

| Tab | Purpose |
|-----|---------|
| **Dashboard** | 25+ asset cross-asset grid with skew velocity panel |
| **Portfolio** | Holdings overlay, Greeks, hedge ratios, performance track |
| **Regime Matrix** | BTC correlation pairs vs VIX/GLD/QQQ with shift alerts |
| **Strategy Compass** | IV Z-score vs Skew Z-score scatter (4 quadrants) |
| **TradFi-Crypto Flow** | IBIT/Deribit OI, dealer gamma, ETF flow bridge |
| **Carry Matrix** | Vol carry + funding + basis with bar visualization |
| **Strategy Engine** | Theta/Delta/Vol trade buckets with regime-aware recs |
| **Weekly Synthesis** | 3 trade expressions with EV math |

## Key Innovation: Skew Velocity

The dashboard tracks skew changes across 5 timeframes (1D, 1W, 2W, 1M, 1Q) and computes a velocity indicator. The speed of skew change is the signal, not the level:

- **PANIC SPIKE** = Fresh deleveraging (sell puts into it)
- **ACCELERATING** = Protection demand building (regime shifting)
- **NORMALIZING** = Mean reversion underway (fade the move)
- **DORMANT** = No flow signal

## Data Sources

- Lakha/Options Insight macro weekly + crypto options weekly
- Deribit options surface
- IBIT/ETF options flow
- Cross-asset vol metrics (Bloomberg equivalent)

## Usage

Open `index.html` in any modern browser. No server required - fully self-contained HTML/CSS/JS with Chart.js from CDN.

## Roadmap

- [ ] JSON data layer for weekly updates without touching HTML
- [ ] CSV/API import for Lakha PDF data
- [ ] Portfolio-grid linkage (regime signals mapped to position management)
- [ ] Historical time-series toggle (4-week lookback)
- [ ] PDF export of current view
- [ ] Live Deribit API integration

## License

Private - proprietary trading tool.
