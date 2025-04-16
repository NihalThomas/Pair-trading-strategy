# Pair Trading Strategy Using Hidden Markov Models (HMM)

This project implements a statistical arbitrage strategy based on pair trading, enhanced with a regime-switching filter using Hidden Markov Models (HMM). It aims to identify and exploit temporary deviations in the price relationship between two historically correlated assets.

## 📈 Strategy Overview

- **Pair Selection:** Selected highly correlated stocks (`GOOGL` and `MSFT`) for mean-reversion opportunities.  
- **Spread Modeling:** Constructed the price spread using linear regression residuals.  
- **Z-Score Signal:** Generated trading signals when the spread diverges significantly from its mean.  
- **Regime Detection:** Applied a Gaussian HMM to classify the market into distinct hidden regimes.  
- **Signal Filtering:** Executed trades only during the identified mean-reverting regime to reduce noise and false signals.  
- **Performance Tracking:** Evaluated the strategy with cumulative log returns based on historical price data.

## 🛠️ Core Concepts

- **Pairs Trading:** Market-neutral strategy profiting from the convergence of two asset prices.  
- **Z-Score Thresholds:** Used to determine entry and exit points for trades.  
- **Hidden Markov Models:** Capture underlying market dynamics and structural shifts in spread behavior.  
- **Risk Control:** Positions are exited when the spread returns near its mean, minimizing exposure.
