Crypto Trading Sentiment Analysis

This repository contains a Python-based analysis to explore the relationship between trader performance and market sentiment, uncovering hidden patterns to drive smarter trading strategies. The project leverages historical trading data and the Fear & Greed Index to provide actionable insights.
Objective
The primary goal is to analyze how market sentiment influences trader performance (e.g., profit/loss, trade size) and identify patterns that can optimize cryptocurrency trading strategies.
Features

Data Preprocessing: Handles timestamp conversion, merges historical trading data with sentiment data, and manages missing values.
Feature Engineering: Creates features like log_size, pnl_per_usd, abs_pnl, ClosedPnL_winsor, and hour for enhanced analysis.
Exploratory Visualizations: Includes histograms, scatterplots, countplots, barplots, and heatmaps to visualize trade distributions and sentiment effects.
Statistical Analysis: Performs aggregations, correlations, cross-correlations, and statistical tests (e.g., Welch’s t-test, chi-square test).
Insights: Delivers findings on sentiment-driven profitability and timing strategies.


Data

historical_data.csv: Contains trade data (e.g., Closed PnL, Size USD, Timestamp IST).
fear_greed_index.csv: Provides sentiment data (e.g., date, value, classification).


View generated plots and printed outputs for insights.

Output

Plots: Visualizations of trade size distribution, PnL vs. sentiment, sentiment class distribution, profitable vs. not profitable trades, correlations, and lagged effects.
Statistics: Summary metrics by sentiment, daily correlations, and p-values from statistical tests.

Key Findings

Extreme Greed offers high returns (mean PnL $67.89, 46.49% profitability) but with significant risks (min pnl_per_usd -384).
Fear provides stable trade sizes (median $735.96) with lower volatility (std 0.072), though more non-profitable trades (-9,799).
A -24-day lagged correlation (-0.181) suggests delayed sentiment impacts on daily PnL.
Significant profitability variation across sentiments (chi-square p-value 1.96e-176), with no significant mean PnL difference between Greed and Fear (p-value 0.0868).

Strategies

Target Extreme Greed with risk controls (e.g., stop-loss at -5%).
Stabilize trades in Fear with smaller sizes.
Mitigate losses in Greed and Fear with tighter exits.
Use -24-day lagged sentiment for timing.
Optimize coin selection by sentiment (e.g., low-value coins in Neutral).
