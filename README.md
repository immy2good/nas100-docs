Certainly! Here’s your README.md content converted from HTML to a clean, Markdown-only README format, with all sections and structure preserved, suitable for a GitHub README:

---

# The Ultimate NAS100 Strategy by iTradeAIMS - DST Version

Welcome to **The Ultimate NAS100 Strategy by iTradeAIMS - DST Version**, a comprehensive Pine Script strategy designed for TradingView. This strategy is tailored specifically for the NAS100 market, providing robust risk management, signal filtering, and flexible trading hours management.

---

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Configuration](#configuration)
- [Inputs and Parameters](#inputs-and-parameters)
  - [Risk Management](#risk-management)
  - [Scaling Out](#scaling-out)
  - [Signal & Trades Management](#signal--trades-management)
  - [Trading Hours Management](#trading-hours-management)
  - [Signal Management](#signal-management)
  - [Close All Trades Management](#close-all-trades-management)
  - [Additional Inputs](#additional-inputs)
- [Strategy Logic](#strategy-logic)
  - [Trend Detection](#trend-detection)
  - [Signal Generation](#signal-generation)
  - [Trade Execution](#trade-execution)
  - [Order Cancellation](#order-cancellation)
  - [Closing Trades](#closing-trades)
- [Plotting and Visuals](#plotting-and-visuals)
- [Usage Instructions](#usage-instructions)
- [Recommendations](#recommendations)
- [FAQs & Troubleshooting](#faqs--troubleshooting)
- [Contact & Support](#contact--support)
- [Appendix](#appendix)
- [Conclusion](#conclusion)

---

## Introduction

Welcome to **The Ultimate NAS100 Strategy by iTradeAIMS - DST Version**, a comprehensive Pine Script strategy designed for TradingView. This strategy is tailored specifically for the NAS100 market, providing robust risk management, signal filtering, and flexible trading hours management.

---

## Features

- **Compounding Option:** Enables risk calculation based on starting equity plus accrued profits.
- **Risk Management:** Adjustable risk percentage per trade with maximum lot size constraints.
- **Signal Filtering:** Utilize bar delay and close price conditions to manage signal cancellations.
- **Trade Limits:** Set maximum numbers of concurrent long and short trades.
- **Trading Hours Management:** Define specific trading windows with DST adjustments for London time.
- **Custom Trade Closure:** Specify exact times to close all open trades independently of trading sessions.
- **Visual Indicators:** Plot entry, stop-loss, and take-profit levels for better trade visualization.
- **Scalable:** Easily adjustable parameters to fit various trading styles and risk appetites.

---

## Installation

1. **Access TradingView:**
   - Ensure you have a TradingView account. If not, [sign up here](https://www.tradingview.com/).
2. **Open Pine Script Editor:**
   - Navigate to the [Pine Script Editor](https://www.tradingview.com/pine-script-docs/en/v5/).
3. **Create a New Script:**
   - Click on **"New"** to create a new Pine Script.
4. **Paste the Strategy Code:**
   - Copy the entire Pine Script code provided and paste it into the editor.
5. **Save the Script:**
   - Click on **"Save"** and give your strategy a meaningful name, e.g., _"Ultimate NAS100 Strategy by iTradeAIMS - DST Version"_.
6. **Add to Chart:**
   - Click on **"Add to Chart"** to apply the strategy to your desired NAS100 chart.

---

## Configuration

After adding the strategy to your chart, you'll need to configure its settings to match your trading preferences. This involves adjusting various input parameters that control risk management, trade management, and visual indicators.

---

## Inputs and Parameters

The strategy offers a range of configurable inputs grouped into different categories for ease of use.

### Risk Management

| Input Name                                 | Type    | Description                                                                                         |
|---------------------------------------------|---------|-----------------------------------------------------------------------------------------------------|
| **Enable Compounding**                     | Boolean | If enabled, risk is calculated based on starting equity plus accrued profits.                       |
| **Max Lot Size**                           | Float   | Defines the maximum position size allowed to prevent excessive risk when compounding is enabled.    |
| **Normalize Max Lot Size for Compounding** | Boolean | Caps position size at defined maximum when compounding is enabled.                                  |
| **Risk Percentage**                        | Float   | Percentage of equity to risk per trade. Adjust according to your risk tolerance.                    |

### Scaling Out

| Input Name     | Type  | Description                                          |
|----------------|-------|------------------------------------------------------|
| **TP1 Multiple** | Float | Multiplier for the first take-profit level.         |
| **TP1 Percent**  | Float | Percentage of the position to take profit at TP1.   |

### Signal & Trades Management

| Input Name         | Type    | Description                                                |
|--------------------|---------|------------------------------------------------------------|
| **Factor**         | Float   | Distance between candle high/low and entry price.           |
| **Longs**          | Integer | Max concurrent long trades allowed.                         |
| **Shorts**         | Integer | Max concurrent short trades allowed.                        |
| **Take Buy Signals**  | Boolean | Enable/disable buy signals.                              |
| **Take Sell Signals** | Boolean | Enable/disable sell signals.                             |

### Trading Hours Management

| Input Name      | Type    | Description                                   |
|-----------------|---------|-----------------------------------------------|
| **Start: Hour** | Integer | Start hour (0-23) for trading session.        |
| **Start: Min**  | Integer | Start minute (0-59) for trading session.      |
| **End: Hour**   | Integer | End hour (0-23) for trading session.          |
| **End: Min**    | Integer | End minute (0-59) for trading session.        |

*Note: Trading hours are adjusted based on DST for London time.*

### Signal Management

| Input Name                                      | Type    | Description                                                     |
|-------------------------------------------------|---------|-----------------------------------------------------------------|
| **Use Bar Delay for Signal Cancellation**        | Boolean | Cancel signals after max number of bars if not filled.          |
| **Max Signal Bars**                             | Integer | Max bars to wait before cancelling unfilled order.              |
| **Use Close Price Condition for Cancellation**   | Boolean | Cancel signals based on price closing above/below signal candle.|

### Close All Trades Management

| Input Name                                  | Type    | Description                                      |
|----------------------------------------------|---------|--------------------------------------------------|
| **Enable Close All Trades at Specific Time** | Boolean | Enable closing all trades at a user-specified time.|
| **Close All Trades: Hour**                   | Integer | Specify hour (0-23) to close all trades.         |
| **Close All Trades: Minute**                 | Integer | Specify minute (0-59) to close all trades.       |

### Additional Inputs

| Input Name                    | Type    | Description                                         |
|-------------------------------|---------|-----------------------------------------------------|
| **Close all trades at session end** | Boolean | Enable closing all trades at session end.      |

---

## Strategy Logic

Understanding the underlying logic of the strategy is crucial for effective utilization and potential customization.

### Trend Detection

- Uses two EMAs:
  - **Faster EMA (5-period):** Quick response to price changes.
  - **Slower EMA (10-period):** Provides a broader trend view.
- **Crossover Up:** Faster EMA crosses above slower EMA (bullish).
- **Crossover Down:** Faster EMA crosses below slower EMA (bearish).

### Signal Generation

**Bullish Patterns:**
- "Bull Pattern" is identified using specific high/low candle logic.

**Bearish Patterns:**
- "Bear Pattern" is identified using specific low/high candle logic.

**Signal Conditions:**
- **Buy Signal:** On bullish pattern, buy signals enabled, confirmed bar, within trading hours, and trade limits not exceeded.
- **Sell Signal:** On bearish pattern, sell signals enabled, confirmed bar, within trading hours, and trade limits not exceeded.

### Trade Execution

- **Entry Price:**  
  - Long: Above signal candle high by factor * tick size.  
  - Short: Below signal candle low by factor * tick size.
- **Stop-Loss:**  
  - Long: Below signal candle low by the same factor.  
  - Short: Above signal candle high by the same factor.
- **Take-Profit:**  
  - Calculated as 50% of the distance between entry and stop-loss.

### Order Cancellation

- **Bar Delay-Based:** Cancel unfilled orders after a set number of bars.
- **Close Price Condition-Based:** Cancel buy orders if price closes below signal candle’s low, and cancel sell orders if price closes above signal candle’s high.
- **Combined Conditions:** Use either or both.

### Closing Trades

Trades can be closed based on:
1. **Specific Time Closure:** Close all open trades at a user-specified time.
2. **Session End Closure:** Close all open trades at the end of the trading session.

---

## Plotting and Visuals

- **Entry Price Lines:** Green lines for long/short entries.
- **Stop-Loss Lines:** Red lines for long/short SL.
- **Take-Profit Lines:** Blue lines for long/short TP1.
- **Signal Markers:** Blue triangle (long), red triangle (short).
- **Moving Averages:** Red (fast EMA), Blue (slow EMA).

These visual indicators provide real-time insight into strategy operations.

---

## Usage Instructions

1. **Add the Strategy to Your Chart:**  
   Follow [Installation](#installation) steps and apply to NAS100 chart.
2. **Configure Inputs:**  
   Open strategy settings (gear icon) and adjust parameters.
3. **Define Trading Hours:**  
   Set start/end times for your session (DST auto-adjusted).
4. **Set Risk Parameters:**  
   Adjust risk percentage and max lot size as desired.
5. **Manage Signals:**  
   Set cancellation conditions and max bars for unfilled orders.
6. **Set Trade Closure Times:**  
   Enable and specify close-all-trades time or session end closure.
7. **Monitor the Strategy:**  
   Use visual cues for entries, exits, and performance.
8. **Backtest and Optimize:**  
   Use TradingView’s tools to backtest and optimize parameters.
9. **Deploy in Live Trading:**  
   When satisfied, move to live/simulated trading and monitor performance.

---

## Recommendations

- **Backtesting:** Always backtest thoroughly before live trading.
- **Risk Management:** Set risk percentage to match your tolerance.
- **Optimize Parameters:** Experiment with Factor, TP1 Multiple, and TP1 Percent.
- **Monitor DST Adjustments:** Mind time zones and DST changes.
- **Regular Reviews:** Periodically review results and fine-tune as needed.
- **Diversify:** Use this strategy alongside other tools for better results.

---

## FAQs & Troubleshooting

**1. Why are my orders being canceled too frequently?**  
Possible reasons:  
- Low _Max Signal Bars_
- Tight _Factor_ setting
- High market volatility  
**Solutions:**  
- Increase _Max Signal Bars_
- Adjust _Factor_ for more room
- Review and adjust settings for current market conditions

**2. How does DST adjustment affect my trading hours?**  
The strategy adjusts trading hours automatically based on London DST. Ensure your TradingView chart matches this logic.

**3. Can I disable the compounding feature?**  
Yes. Set _Enable Compounding_ to `false` in Risk Management.

**4. Why are there no trade signals displayed?**  
Possible reasons:  
- Trading session not active
- Signal conditions not met
- Trade limits reached  
**Solutions:**  
- Check trading session hours
- Review chart timeframe and logic
- Adjust _Max Long/Short Trades_

**5. How do I change the time to close all trades?**  
Go to **Close All Trades Management** in settings:  
- Enable _Close All Trades at Specific Time_
- Set desired hour and minute

---

## Contact & Support

For help, customization, or feedback:

- **Email:** [support@itradeaims.com](mailto:support@itradeaims.com)
- **Website:** [iTradeAIMS](https://www.itradeaims.com)
- **TradingView:** [iTradeAIMS on TradingView](https://www.tradingview.com/u/itradeaims)

---

## Appendix

### Pine Script Code Overview

- **Strategy Declaration:** Name, overlay, calculation, initial capital.
- **Input Definitions:** Organized input groups.
- **DST Adjustments:** Auto London DST trading hours.
- **Trend Detection:** EMA-based.
- **Signal Patterns:** Candle formation logic.
- **Risk Calculation:** Based on percentage and equity.
- **Order Management:** Advanced buy/sell and cancellation logic.
- **Trade Closure:** Session end and specific time.
- **Visual Indicators:** Entry, SL, TP, and EMAs plotted.

---

## Conclusion

**The Ultimate NAS100 Strategy by iTradeAIMS - DST Version** is a robust and flexible trading strategy for the NAS100 market. With advanced risk management, signal filtering, and visual tools, it empowers traders to approach the NAS100 with confidence and discipline.

---

Let me know if you want to further customize the wording, add images, or format tables differently!
