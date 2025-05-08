# RSI_BB_Scalping

# RSI Scalping Strategy
This project implements a scalping strategy using RSI and Bollinger Bands on 5-minute candlestick data. It combines technical indicators, leveraged trading, and risk management to generate and evaluate trading signals. The strategy's performance is analyzed through detailed metrics and visualizations. This repository is shared solely for informational and demonstration purposes to showcase the project's structure, outputs, and results.

## About the Script
The script (rsi_scalping_strategy_inr_15x_dynamic_capital_redacted.py) provided in this repository is a redacted version of the original code. Sensitive components, such as the proprietary trading logic, specific parameter values (e.g., RSI thresholds, leverage settings), and detailed calculations, have been redacted to protect intellectual property and prevent misuse. The redacted script retains the overall structure to demonstrate the workflow—data loading, indicator calculation, backtesting, and visualization—while ensuring that critical strategy details remain confidential. The results and outputs shared below were generated using the full, unredacted script. This project is shared solely for informational and demonstration purposes. Any use, replication, or derivation of the strategy, including for personal, educational, commercial, or financial purposes, is strictly prohibited, as outlined in the LICENSE file.

## Features

### Plots (Output Results):

#### 1. Equity Curve (Figure 1a):
- Shows equity growth over time with cumulative trade counts on a secondary axis.
 ![figure1a_equity_curve_7_5m_inr_15x_10m](https://github.com/user-attachments/assets/12e79da6-c2b1-4b0a-818d-46c280273714)




#### 2. Drawdown (Figure 1b):
- Displays drawdown percentage over time.
 ![figure1b_drawdown_7_5m_inr_15x_10m](https://github.com/user-attachments/assets/a01008d9-9472-440e-8082-ff16130d7281)



#### 3. Monthly Performance (Figure 1c):
- Shows cumulative monthly returns with trade counts.
![figure1c_monthly_performance_7_5m_inr_15x_10m](https://github.com/user-attachments/assets/479eda93-c41d-4e69-9b3b-506f5372ac71)



#### 4. Price with Volume Overlay (Figure 1d):
- Plots price with a volume overlay.
![figure1d_price_volume_7_5m_inr_15x_10m](https://github.com/user-attachments/assets/d298e1a4-7645-4231-aec1-db035eec0dfb)


### 5. RSI and Bollinger Bands (Figure 2):

Sample: sample_outputs/figure2_rsi_bollinger_combined_plot_7_5m_inr_15x_10m.png


### Technical Indicators:
- RSI (Relative Strength Index) to detect overbought/oversold conditions.
- Bollinger Bands to identify price volatility and potential reversals.
- ATR (Average True Range) for volatility-based trade filtering and trailing stops.


### Trading Logic:
- Enters trades based on RSI thresholds and Bollinger Band positions.
- Exits via stop-loss, take-profit, or ATR-based trailing stops.
- Supports leveraged trading with liquidation checks.


### Risk Management:
- Configurable risk per trade and maximum position sizes.
- Limits concurrent trades to control exposure.
- Skips trades during extreme price movements or low volatility.

### Performance Metrics:
- Computes total return, win rate, max drawdown, Sharpe ratio, Sortino ratio, and profit factor.
- Provides monthly performance breakdowns and trade statistics.


### Visualization:
- Equity curve with cumulative trade counts.
- Drawdown over time.
- Monthly performance with trade frequency.
- Price and volume overlay.
- Combined RSI and Bollinger Bands plot (trade markers disabled).


### Dynamic Capital Support:
- Adjusts file names and visualizations based on initial capital (e.g., 10m for ₹10,000,000).



## Outputs
The script generates the following outputs in the rsi_scalping_strategy_outputs/ directory:

### Trades CSV:

- File: rsi_scalping_trades_7_5m_inr_15x_<capital>_with_combined_rsi_bb_plot.csv
- Contains trade details: entry/exit times, prices, position sizes, profits, and durations.
- Sample: sample_outputs/rsi_scalping_trades_7_5m_inr_15x_10m_with_combined_rsi_bb_plot.csv





#### 5. RSI and Bollinger Bands (Figure 2):
- Combines price with Bollinger Bands (top) and RSI (bottom).
- File: figure2_rsi_bollinger_combined_plot_7_5m_inr_15x_<capital>.png
- Sample: sample_outputs/figure2_rsi_bollinger_combined_plot_7_5m_inr_15x_10m.png





## Results
The script was run with an initial capital of ₹10,000,000 (10m) and 15x leverage over a 16-month backtest period (January 2024 to April 2025). Below are the key results:

### Trade Statistics:

- Average Trade Duration: 0.49 hours
- Average Win: 1.36%
- Average Loss: 0.35%
- Trades per Day: 1.03


### Monthly Performance:

- 2024-01: Return: -4.11%, Trades: 100
- 2024-02: Return: 4.78%, Trades: 71
- 2024-03: Return: 22.38%, Trades: 15
- 2024-04: Return: 65.03%, Trades: 24
- 2024-05: Return: 76.54%, Trades: 21
- 2024-06: Return: 80.07%, Trades: 25
- 2024-07: Return: 76.80%, Trades: 28
- 2024-08: Return: 119.36%, Trades: 24
- 2024-09: Return: 133.39%, Trades: 27
- 2024-10: Return: 132.75%, Trades: 29
- 2024-11: Return: 130.86%, Trades: 25
- 2024-12: Return: 140.93%, Trades: 25
- 2025-01: Return: 154.25%, Trades: 31
- 2025-02: Return: 153.88%, Trades: 16
- 2025-03: Return: 175.44%, Trades: 22
- 2025-04: Return: 184.66%, Trades: 18


### Summary:

- Starting Capital: ₹10,000,000.00
- Final Capital: ₹28,466,115.98
- Total Return: 184.66%
- Total Trades: 501
- Win Rate: 34.13%
- Max Drawdown: -1.82%
- Sharpe Ratio: 0.29
- Sortino Ratio: Not available (NaN)
- Profit Factor: 1.9834





## License
This project is shared solely for informational and demonstration purposes under the RSI Scalping Strategy Notice, which prohibits any use, modification, or distribution. See the LICENSE file for details.
