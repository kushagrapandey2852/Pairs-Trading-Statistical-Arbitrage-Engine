<div align="center">

# ⚖️ Pairs Trading & Statistical Arbitrage Engine

### Cointegration • Mean Reversion • Market Neutral Alpha

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/Statsmodels-Econometrics-success?style=for-the-badge">
  <img src="https://img.shields.io/badge/Backtrader-Strategy_Backtesting-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Statistical_Arbitrage-Quant_Trading-orange?style=for-the-badge">
</p>

<p align="center">
  <b>Cointegration</b> • <b>Mean Reversion</b> • <b>OU Process</b> • <b>Market Neutral</b>
</p>

</div>

---

## Overview

Most assets drift apart.

Some repeatedly come back together.

This project identifies statistically linked securities, models their spread dynamics, and executes market-neutral trading strategies that profit from temporary deviations from equilibrium.

The framework combines cointegration testing, stochastic process modelling, and systematic backtesting to replicate workflows used by statistical arbitrage desks and quantitative hedge funds.

---

## Statistical Arbitrage Pipeline

<div align="center">

```text
         Asset Universe
                │
                ▼

      Cointegration Tests

                │
                ▼

      Candidate Pairs

                │
                ▼

      Spread Modelling

                │
                ▼

      Trading Signals

                │
                ▼

         Backtesting

                │
                ▼

      Performance Analysis
```

</div>

---

## Pair Selection Engine

<div align="center">

```text
       Asset A
          │
          │
          ▼

     Statistical
      Relationship

          ▲
          │
          │

       Asset B
```

</div>

Only pairs exhibiting long-term equilibrium relationships proceed to strategy generation.

---

## Cointegration Framework

<div align="center">

```text
 Historical Prices

         │

         ▼

 ┌─────────────────┐
 │ Engle-Granger   │
 └─────────────────┘

         │

         ▼

 ┌─────────────────┐
 │   Johansen      │
 └─────────────────┘

         │

         ▼

 Cointegrated Pair
```

</div>

### Statistical Tests

| Test | Purpose |
|--------|---------|
| Engle-Granger | Two-Asset Cointegration |
| Johansen | Multi-Asset Cointegration |
| ADF Test | Stationarity Validation |
| Hurst Exponent | Mean-Reversion Strength |

---

## Spread Construction

<div align="center">

```text
 Asset A Price

        │

        ▼

 Hedge Ratio

        │

        ▼

 Asset B Price

        │

        ▼

      Spread

        │

        ▼

 Mean-Reverting Series
```

</div>

The spread becomes the tradable object rather than the individual assets.

---

## Ornstein-Uhlenbeck Model

The spread is modeled as a mean-reverting stochastic process.

<div align="center">

```text
         Long-Term Mean

                ▲

                │

     /\/\/\/\/\/\/\/\/\

                │

                ▼

      Temporary Deviations
```

</div>

### Process Intuition

```text
Spread Moves Away

        │

        ▼

Mean Reversion Force

        │

        ▼

Spread Returns
```

</div>

---

## Signal Generation

<div align="center">

```text
      Spread

         │

         ▼

    Z-Score

         │

         ▼

 Entry Threshold

         │

 ┌───────┴───────┐

 ▼               ▼

 Long Spread   Short Spread

         │

         ▼

 Exit Signal
```

</div>

---

## Trading Logic

### Spread Too Wide

```text
 Asset A ↑

 Asset B ↓

      │

      ▼

 Short Spread
```

### Spread Too Narrow

```text
 Asset A ↓

 Asset B ↑

      │

      ▼

 Long Spread
```

The strategy remains market-neutral by simultaneously holding long and short positions.

---

## Strategy Lifecycle

<div align="center">

```text
 Cointegrated Pair

          │

          ▼

 Spread Divergence

          │

          ▼

 Trade Entry

          │

          ▼

 Mean Reversion

          │

          ▼

 Trade Exit
```

</div>

---

## Backtesting Framework

<div align="center">

```text
 Historical Data

         │

         ▼

 Signal Generation

         │

         ▼

 Position Management

         │

         ▼

 Transaction Costs

         │

         ▼

 Net Returns
```

</div>

---

## Transaction Cost Model

A profitable strategy must survive realistic execution costs.

<div align="center">

```text
 Gross Profit

       │

       ▼

 Commissions

       │

       ▼

 Slippage

       │

       ▼

 Borrow Costs

       │

       ▼

 Net Alpha
```

</div>

---

## System Architecture

<div align="center">

```text
┌──────────────────────────┐
│ Market Data Universe     │
└─────────────┬────────────┘
              │
              ▼

┌──────────────────────────┐
│ Cointegration Engine     │
├──────────────────────────┤
│ Engle-Granger Test       │
│ Johansen Test            │
│ Stationarity Analysis    │
└─────────────┬────────────┘
              │
              ▼

┌──────────────────────────┐
│ Spread Modelling Layer   │
│ OU Process Estimation    │
└─────────────┬────────────┘
              │
              ▼

┌──────────────────────────┐
│ Signal Generator         │
└─────────────┬────────────┘
              │
              ▼

┌──────────────────────────┐
│ Backtrader Engine        │
└──────────────────────────┘
```

</div>

---

## Research Dashboard

| Module | Purpose |
|----------|---------|
| Pair Discovery | Cointegration Screening |
| Spread Monitor | Mean-Reversion Analysis |
| OU Calibration | Process Estimation |
| Signal Dashboard | Entry & Exit Signals |
| Backtest Results | Strategy Performance |
| Cost Analytics | Net Alpha Analysis |
| Risk Metrics | Drawdown & Exposure |

---

## Quantitative Foundation

<div align="center">

```text
      Market Efficiency

              │

              ▼

 Statistical Relationships

              │

              ▼

 Cointegration

              │

              ▼

 Mean Reversion

              │

              ▼

 Statistical Arbitrage
```

</div>

---

## Example Research Workflow

<div align="center">

```text
 Universe Selection

         │

         ▼

 Cointegration Scan

         │

         ▼

 Spread Construction

         │

         ▼

 OU Calibration

         │

         ▼

 Strategy Backtest

         │

         ▼

 Alpha Validation
```

</div>

---

## Technology Stack

```text
Python
│
├── Pandas
├── NumPy
├── Statsmodels
├── Backtrader
└── Matplotlib
```

---

## Real-World Applications

### Statistical Arbitrage Funds

- Pair Selection
- Market-Neutral Strategies
- Alpha Generation

### Quantitative Hedge Funds

- Relative Value Trading
- Spread Trading
- Portfolio Diversification

### Proprietary Trading Desks

- Mean-Reversion Strategies
- Factor Neutral Trading
- Quant Research

---

## Skills Demonstrated

✅ Cointegration Analysis

✅ Engle-Granger Testing

✅ Johansen Testing

✅ Ornstein-Uhlenbeck Processes

✅ Statistical Arbitrage

✅ Market-Neutral Portfolio Design

✅ Time-Series Econometrics

✅ Backtesting

✅ Quantitative Trading

✅ Alpha Research

---

## Repository Structure

```text
pairs-trading-statistical-arbitrage-engine/
│
├── data/
│
├── cointegration/
│   ├── engle_granger.py
│   ├── johansen.py
│
├── spread_models/
│   ├── ou_process.py
│
├── signals/
│
├── backtesting/
│
├── analytics/
│
├── dashboards/
│
└── README.md
```

---

<div align="center">

### ⚖️ Trade Relationships, Not Directions

*"The market can stay irrational. Cointegrated spreads eventually remember where home is."*

</div>
