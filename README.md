<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Ultimate NAS100 Strategy by iTradeAIMS - DST Version</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- Optional: Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" integrity="sha512-Fo3rlrQd1kY5p1kE/mEjpCJDQKLy8NhvYtN6F/f19LaqX3G1nM/aGm1l+e8Q/S9doMFF3Tn9h/8+9i0wWgr4DA==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <style>
        body {
            overflow-x: hidden;
        }
        /* Sidebar styling */
        #sidebar {
            min-width: 250px;
            max-width: 250px;
            min-height: 100vh;
            background: #343a40;
            color: #fff;
            position: fixed;
        }
        #sidebar .nav-link {
            color: #fff;
        }
        #sidebar .nav-link:hover {
            background: #495057;
            color: #fff;
        }
        /* Main content styling */
        #content {
            margin-left: 250px;
            padding: 20px;
        }
        /* Responsive adjustments */
        @media (max-width: 768px) {
            #sidebar {
                min-width: 100%;
                max-width: 100%;
                height: auto;
                position: relative;
            }
            #content {
                margin-left: 0;
            }
        }
        /* Smooth scrolling */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body>

    <!-- Sidebar -->
    <nav id="sidebar" class="bg-dark">
        <div class="p-4 pt-5">
            <h5 class="text-center mb-4">Documentation</h5>
            <ul class="nav flex-column">
                <li class="nav-item">
                    <a class="nav-link active" href="#introduction"><i class="fas fa-info-circle me-2"></i>Introduction</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#features"><i class="fas fa-cogs me-2"></i>Features</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#installation"><i class="fas fa-download me-2"></i>Installation</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#configuration"><i class="fas fa-sliders-h me-2"></i>Configuration</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#inputs-and-parameters"><i class="fas fa-tasks me-2"></i>Inputs and Parameters</a>
                    <ul class="nav flex-column ms-3">
                        <li class="nav-item">
                            <a class="nav-link" href="#risk-management">Risk Management</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#scaling-out">Scaling Out</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#signal--trades-management">Signal & Trades Management</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#trading-hours-management">Trading Hours Management</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#signal-management">Signal Management</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#close-all-trades-management">Close All Trades Management</a>
                        </li>
                    </ul>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#strategy-logic"><i class="fas fa-project-diagram me-2"></i>Strategy Logic</a>
                    <ul class="nav flex-column ms-3">
                        <li class="nav-item">
                            <a class="nav-link" href="#trend-detection">Trend Detection</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#signal-generation">Signal Generation</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#trade-execution">Trade Execution</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#order-cancellation">Order Cancellation</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#closing-trades">Closing Trades</a>
                        </li>
                    </ul>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#plotting-and-visuals"><i class="fas fa-chart-line me-2"></i>Plotting and Visuals</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#usage-instructions"><i class="fas fa-play-circle me-2"></i>Usage Instructions</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#recommendations"><i class="fas fa-lightbulb me-2"></i>Recommendations</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#faqs--troubleshooting"><i class="fas fa-question-circle me-2"></i>FAQs & Troubleshooting</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#contact--support"><i class="fas fa-envelope me-2"></i>Contact & Support</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#appendix"><i class="fas fa-book me-2"></i>Appendix</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#conclusion"><i class="fas fa-clipboard-check me-2"></i>Conclusion</a>
                </li>
            </ul>
        </div>
    </nav>

    <!-- Main Content -->
    <div id="content">
        <div class="container-fluid">
            <!-- Introduction -->
            <section id="introduction">
                <h2>Introduction</h2>
                <p>Welcome to <strong>The Ultimate NAS100 Strategy by iTradeAIMS - DST Version</strong>, a comprehensive Pine Script strategy designed for TradingView. This strategy is tailored specifically for trading the NAS100 index, incorporating advanced risk and trade management features, dynamic signal filtering, and customizable trade closure options based on Daylight Saving Time (DST) adjustments for the UK market.</p>
                <hr>
            </section>

            <!-- Features -->
            <section id="features">
                <h2>Features</h2>
                <ul>
                    <li><strong>Compounding Option:</strong> Enables risk calculation based on starting equity plus accrued profits.</li>
                    <li><strong>Risk Management:</strong> Adjustable risk percentage per trade with maximum lot size constraints.</li>
                    <li><strong>Signal Filtering:</strong> Utilize bar delay and close price conditions to manage signal cancellations.</li>
                    <li><strong>Trade Limits:</strong> Set maximum numbers of concurrent long and short trades.</li>
                    <li><strong>Trading Hours Management:</strong> Define specific trading windows with DST adjustments for London time.</li>
                    <li><strong>Custom Trade Closure:</strong> Specify exact times to close all open trades independently of trading sessions.</li>
                    <li><strong>Visual Indicators:</strong> Plot entry, stop-loss, and take-profit levels for better trade visualization.</li>
                    <li><strong>Scalable:</strong> Easily adjustable parameters to fit various trading styles and risk appetites.</li>
                </ul>
                <hr>
            </section>

            <!-- Installation -->
            <section id="installation">
                <h2>Installation</h2>
                <ol>
                    <li><strong>Access TradingView:</strong>
                        <ul>
                            <li>Ensure you have a TradingView account. If not, <a href="https://www.tradingview.com/" target="_blank">sign up here</a>.</li>
                        </ul>
                    </li>
                    <li><strong>Open Pine Script Editor:</strong>
                        <ul>
                            <li>Navigate to the <a href="https://www.tradingview.com/pine-script-docs/en/v5/" target="_blank">Pine Script Editor</a>.</li>
                        </ul>
                    </li>
                    <li><strong>Create a New Script:</strong>
                        <ul>
                            <li>Click on <strong>"New"</strong> to create a new Pine Script.</li>
                        </ul>
                    </li>
                    <li><strong>Paste the Strategy Code:</strong>
                        <ul>
                            <li>Copy the entire Pine Script code provided above and paste it into the editor.</li>
                        </ul>
                    </li>
                    <li><strong>Save the Script:</strong>
                        <ul>
                            <li>Click on <strong>"Save"</strong> and give your strategy a meaningful name, e.g., <em>"Ultimate NAS100 Strategy by iTradeAIMS - DST Version"</em>.</li>
                        </ul>
                    </li>
                    <li><strong>Add to Chart:</strong>
                        <ul>
                            <li>Click on <strong>"Add to Chart"</strong> to apply the strategy to your desired NAS100 chart.</li>
                        </ul>
                    </li>
                </ol>
                <hr>
            </section>

            <!-- Configuration -->
            <section id="configuration">
                <h2>Configuration</h2>
                <p>After adding the strategy to your chart, you'll need to configure its settings to match your trading preferences. This involves adjusting various input parameters that control risk management, trade execution, signal filtering, and trade closure times.</p>
                <hr>
            </section>

            <!-- Inputs and Parameters -->
            <section id="inputs-and-parameters">
                <h2>Inputs and Parameters</h2>
                <p>The strategy offers a range of configurable inputs grouped into different categories for ease of use. Below is a detailed explanation of each input.</p>

                <!-- Risk Management -->
                <section id="risk-management">
                    <h3>Risk Management</h3>
                    <table class="table table-striped">
                        <thead class="table-dark">
                            <tr>
                                <th>Input Name</th>
                                <th>Type</th>
                                <th>Description</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><strong>Enable Compounding</strong></td>
                                <td>Boolean</td>
                                <td>If enabled, risk is calculated based on starting equity plus accrued profits, allowing for compounding growth.</td>
                            </tr>
                            <tr>
                                <td><strong>Max Lot Size</strong></td>
                                <td>Float</td>
                                <td>Defines the maximum position size allowed to prevent excessive risk when compounding is enabled.</td>
                            </tr>
                            <tr>
                                <td><strong>Normalize Max Lot Size for Compounding</strong></td>
                                <td>Boolean</td>
                                <td>If enabled, the position size will be capped at the defined maximum lot size when compounding is enabled to prevent excessive growth in position size.</td>
                            </tr>
                            <tr>
                                <td><strong>Risk Percentage</strong></td>
                                <td>Float</td>
                                <td>Percentage of equity to risk per trade. Adjust according to your risk tolerance and trading strategy.</td>
                            </tr>
                        </tbody>
                    </table>
                </section>

                <!-- Scaling Out -->
                <section id="scaling-out">
                    <h3>Scaling Out</h3>
                    <table class="table table-striped">
                        <thead class="table-dark">
                            <tr>
                                <th>Input Name</th>
                                <th>Type</th>
                                <th>Description</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><strong>TP1 Multiple</strong></td>
                                <td>Float</td>
                                <td>Defines the multiplier for the first take-profit level.</td>
                            </tr>
                            <tr>
                                <td><strong>TP1 Percent</strong></td>
                                <td>Float</td>
                                <td>Defines the percentage of the position to take profit at the first take-profit level.</td>
                            </tr>
                        </tbody>
                    </table>
                </section>

                <!-- Signal & Trades Management -->
                <section id="signal--trades-management">
                    <h3>Signal & Trades Management</h3>
                    <table class="table table-striped">
                        <thead class="table-dark">
                            <tr>
                                <th>Input Name</th>
                                <th>Type</th>
                                <th>Description</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><strong>Factor</strong></td>
                                <td>Float</td>
                                <td>The distance between candle high/low and entry price. It changes based on the broker's quoted prices.</td>
                            </tr>
                            <tr>
                                <td><strong>Longs</strong></td>
                                <td>Integer</td>
                                <td>Maximum number of concurrent long trades allowed.</td>
                            </tr>
                            <tr>
                                <td><strong>Shorts</strong></td>
                                <td>Integer</td>
                                <td>Maximum number of concurrent short trades allowed.</td>
                            </tr>
                            <tr>
                                <td><strong>Take Buy Signals</strong></td>
                                <td>Boolean</td>
                                <td>Enable or disable the strategy's buy signals.</td>
                            </tr>
                            <tr>
                                <td><strong>Take Sell Signals</strong></td>
                                <td>Boolean</td>
                                <td>Enable or disable the strategy's sell signals.</td>
                            </tr>
                        </tbody>
                    </table>
                </section>

                <!-- Trading Hours Management -->
                <section id="trading-hours-management">
                    <h3>Trading Hours Management</h3>
                    <table class="table table-striped">
                        <thead class="table-dark">
                            <tr>
                                <th>Input Name</th>
                                <th>Type</th>
                                <th>Description</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><strong>Start: Hour</strong></td>
                                <td>Integer</td>
                                <td>Enter the start hour (0-23) for the trading session.</td>
                            </tr>
                            <tr>
                                <td><strong>Start: Minutes</strong></td>
                                <td>Integer</td>
                                <td>Enter the start minute (0-59) for the trading session.</td>
                            </tr>
                            <tr>
                                <td><strong>End: Hour</strong></td>
                                <td>Integer</td>
                                <td>Enter the end hour (0-23) for the trading session.</td>
                            </tr>
                            <tr>
                                <td><strong>End: Minutes</strong></td>
                                <td>Integer</td>
                                <td>Enter the end minute (0-59) for the trading session.</td>
                            </tr>
                        </tbody>
                    </table>
                    <p><strong>Note:</strong> The trading hours are adjusted based on DST for London time.</p>
                </section>

                <!-- Signal Management -->
                <section id="signal-management">
                    <h3>Signal Management</h3>
                    <table class="table table-striped">
                        <thead class="table-dark">
                            <tr>
                                <th>Input Name</th>
                                <th>Type</th>
                                <th>Description</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><strong>Use Bar Delay for Signal Cancellation</strong></td>
                                <td>Boolean</td>
                                <td>Enable or disable cancellation of signals based on a maximum number of bars.</td>
                            </tr>
                            <tr>
                                <td><strong>Max Signal Bars</strong></td>
                                <td>Integer</td>
                                <td>Maximum number of bars to wait before cancelling the order if not filled.</td>
                            </tr>
                            <tr>
                                <td><strong>Use Close Price Condition for Cancellation</strong></td>
                                <td>Boolean</td>
                                <td>Enable or disable cancellation of signals based on price closing above/below the signal candle.</td>
                            </tr>
                        </tbody>
                    </table>
                </section>

                <!-- Close All Trades Management -->
                <section id="close-all-trades-management">
                    <h3>Close All Trades Management</h3>
                    <table class="table table-striped">
                        <thead class="table-dark">
                            <tr>
                                <th>Input Name</th>
                                <th>Type</th>
                                <th>Description</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><strong>Enable Close All Trades at Specific Time</strong></td>
                                <td>Boolean</td>
                                <td>Enable or disable closing all trades at a user-specified time.</td>
                            </tr>
                            <tr>
                                <td><strong>Close All Trades: Hour</strong></td>
                                <td>Integer</td>
                                <td>Specify the hour (0-23) to close all trades.</td>
                            </tr>
                            <tr>
                                <td><strong>Close All Trades: Minute</strong></td>
                                <td>Integer</td>
                                <td>Specify the minute (0-59) to close all trades.</td>
                            </tr>
                        </tbody>
                    </table>
                </section>

                <!-- Additional Inputs -->
                <section id="additional-inputs">
                    <h3>Additional Inputs</h3>
                    <table class="table table-striped">
                        <thead class="table-dark">
                            <tr>
                                <th>Input Name</th>
                                <th>Type</th>
                                <th>Description</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><strong>Close all trades at session end</strong></td>
                                <td>Boolean</td>
                                <td>Enable or disable closing all trades at the end of the trading session.</td>
                            </tr>
                        </tbody>
                    </table>
                </section>
                <hr>
            </section>

            <!-- Strategy Logic -->
            <section id="strategy-logic">
                <h2>Strategy Logic</h2>
                <p>Understanding the underlying logic of the strategy is crucial for effective utilization and potential customization. Here's a breakdown of how the strategy operates.</p>

                <!-- Trend Detection -->
                <section id="trend-detection">
                    <h3>Trend Detection</h3>
                    <p>The strategy utilizes two Exponential Moving Averages (EMAs) to detect the market trend:</p>
                    <ul>
                        <li><strong>Faster EMA (5-period):</strong> Responds quickly to price changes.</li>
                        <li><strong>Slower EMA (10-period):</strong> Responds more slowly, providing a broader view of the trend.</li>
                    </ul>
                    <p><strong>Crossover Conditions:</strong></p>
                    <ul>
                        <li><strong>Crossover Up:</strong> When the faster EMA crosses above the slower EMA, indicating a potential bullish trend.</li>
                        <li><strong>Crossover Down:</strong> When the faster EMA crosses below the slower EMA, indicating a potential bearish trend.</li>
                    </ul>
                </section>

                <!-- Signal Generation -->
                <section id="signal-generation">
                    <h3>Signal Generation</h3>
                    <p><strong>Bullish Patterns:</strong></p>
                    <ul>
                        <li><strong>Bull Pattern:</strong> Identified when the current high is less than or equal to the previous high, the previous high is greater than or equal to two bars ago, and the current low is greater than or equal to two bars ago.</li>
                    </ul>
                    <p><strong>Bearish Patterns:</strong></p>
                    <ul>
                        <li><strong>Bear Pattern:</strong> Identified when the current low is greater than or equal to the previous low, the previous low is less than or equal to two bars ago, and the current high is less than or equal to two bars ago.</li>
                    </ul>
                    <p><strong>Signal Conditions:</strong></p>
                    <ul>
                        <li><strong>Buy Signal:</strong> Triggered when a bullish pattern is detected, buy signals are enabled, the current bar is confirmed, within trading hours, under the maximum number of long trades, and a bullish crossover occurs without a bearish crossover.</li>
                        <li><strong>Sell Signal:</strong> Triggered when a bearish pattern is detected, sell signals are enabled, the current bar is confirmed, within trading hours, under the maximum number of short trades, and a bearish crossover occurs without a bullish crossover.</li>
                    </ul>
                </section>

                <!-- Trade Execution -->
                <section id="trade-execution">
                    <h3>Trade Execution</h3>
                    <p>Upon signal detection, the strategy executes trades with the following parameters:</p>
                    <ul>
                        <li><strong>Entry Price:</strong>
                            <ul>
                                <li><strong>Long:</strong> Set above the high of the signal candle by a factor multiplied by the minimum tick size.</li>
                                <li><strong>Short:</strong> Set below the low of the signal candle by a factor multiplied by the minimum tick size.</li>
                            </ul>
                        </li>
                        <li><strong>Stop-Loss (SL):</strong>
                            <ul>
                                <li><strong>Long:</strong> Set below the low of the signal candle by the same factor.</li>
                                <li><strong>Short:</strong> Set above the high of the signal candle by the same factor.</li>
                            </ul>
                        </li>
                        <li><strong>Take-Profit (TP1):</strong>
                            <ul>
                                <li>Calculated as 50% of the distance between the entry price and the SL.</li>
                            </ul>
                        </li>
                    </ul>
                </section>

                <!-- Order Cancellation -->
                <section id="order-cancellation">
                    <h3>Order Cancellation</h3>
                    <p>The strategy incorporates advanced order cancellation logic to manage unfilled orders effectively:</p>
                    <ul>
                        <li><strong>Bar Delay-Based Cancellation:</strong> If enabled, the strategy cancels unfilled orders after a specified number of bars.</li>
                        <li><strong>Close Price Condition-Based Cancellation:</strong> If enabled, the strategy cancels buy orders if the price closes below the signal candle's low and cancels sell orders if the price closes above the signal candle's high.</li>
                        <li><strong>Combined Conditions:</strong> Users can choose to use either or both cancellation conditions.</li>
                    </ul>
                </section>

                <!-- Closing Trades -->
                <section id="closing-trades">
                    <h3>Closing Trades</h3>
                    <p>Trades can be closed based on two user-defined conditions:</p>
                    <ol>
                        <li><strong>Specific Time Closure:</strong> Close all open trades at a user-specified time.</li>
                        <li><strong>Session End Closure:</strong> Close all open trades at the end of the defined trading session.</li>
                    </ol>
                </section>
                <hr>
            </section>

            <!-- Plotting and Visuals -->
            <section id="plotting-and-visuals">
                <h2>Plotting and Visuals</h2>
                <p>To aid in visual analysis and debugging, the strategy plots several key elements on the chart:</p>
                <ul>
                    <li><strong>Entry Price Lines:</strong>
                        <ul>
                            <li><strong>Long Entry:</strong> Green line indicating the entry price for long trades.</li>
                            <li><strong>Short Entry:</strong> Green line indicating the entry price for short trades.</li>
                        </ul>
                    </li>
                    <li><strong>Stop-Loss Lines:</strong>
                        <ul>
                            <li><strong>Long SL:</strong> Red line indicating the stop-loss level for long trades.</li>
                            <li><strong>Short SL:</strong> Red line indicating the stop-loss level for short trades.</li>
                        </ul>
                    </li>
                    <li><strong>Take-Profit Lines:</strong>
                        <ul>
                            <li><strong>Long TP1:</strong> Blue line indicating the first take-profit level for long trades.</li>
                            <li><strong>Short TP1:</strong> Blue line indicating the first take-profit level for short trades.</li>
                        </ul>
                    </li>
                    <li><strong>Signal Markers:</strong>
                        <ul>
                            <li><strong>Long Signals:</strong> Blue triangle pointing upwards below the bar.</li>
                            <li><strong>Short Signals:</strong> Red triangle pointing downwards above the bar.</li>
                        </ul>
                    </li>
                    <li><strong>Moving Averages:</strong>
                        <ul>
                            <li><strong>Faster EMA (5-period):</strong> Red line.</li>
                            <li><strong>Slower EMA (10-period):</strong> Blue line.</li>
                        </ul>
                    </li>
                </ul>
                <p>These visual indicators provide real-time insights into the strategy's operations and help traders make informed decisions.</p>
                <hr>
            </section>

            <!-- Usage Instructions -->
            <section id="usage-instructions">
                <h2>Usage Instructions</h2>
                <ol>
                    <li><strong>Add the Strategy to Your Chart:</strong>
                        <ul>
                            <li>Ensure you've installed the strategy following the <a href="#installation">Installation</a> section.</li>
                            <li>Apply it to your NAS100 chart.</li>
                        </ul>
                    </li>
                    <li><strong>Configure Inputs:</strong>
                        <ul>
                            <li>Open the strategy's settings by clicking on the gear icon next to the strategy's name.</li>
                            <li>Navigate through each input category and adjust the parameters according to your trading preferences and risk tolerance.</li>
                        </ul>
                    </li>
                    <li><strong>Define Trading Hours:</strong>
                        <ul>
                            <li>Set the start and end times for your trading session.</li>
                            <li>The strategy automatically adjusts for DST based on London time.</li>
                        </ul>
                    </li>
                    <li><strong>Set Risk Parameters:</strong>
                        <ul>
                            <li>Determine your risk percentage per trade.</li>
                            <li>Adjust the maximum lot size if compounding is enabled.</li>
                        </ul>
                    </li>
                    <li><strong>Manage Signals:</strong>
                        <ul>
                            <li>Choose whether to use bar delay and/or close price conditions for order cancellations.</li>
                            <li>Set the maximum number of bars to wait before cancelling an unfilled order.</li>
                        </ul>
                    </li>
                    <li><strong>Set Trade Closure Times:</strong>
                        <ul>
                            <li>Enable and specify the exact time to close all open trades if desired.</li>
                            <li>Optionally, enable closing all trades at the end of the trading session.</li>
                        </ul>
                    </li>
                    <li><strong>Monitor the Strategy:</strong>
                        <ul>
                            <li>Observe the plotted indicators and signals on your chart.</li>
                            <li>Use the visual cues to understand trade entries, exits, and the overall strategy performance.</li>
                        </ul>
                    </li>
                    <li><strong>Backtest and Optimize:</strong>
                        <ul>
                            <li>Utilize TradingView's backtesting features to evaluate the strategy's performance over historical data.</li>
                            <li>Adjust input parameters as necessary to optimize results.</li>
                        </ul>
                    </li>
                    <li><strong>Deploy in Live Trading:</strong>
                        <ul>
                            <li>Once satisfied with backtesting results, consider deploying the strategy in a live or simulated trading environment.</li>
                            <li>Continuously monitor and adjust as needed based on market conditions.</li>
                        </ul>
                    </li>
                </ol>
                <hr>
            </section>

            <!-- Recommendations -->
            <section id="recommendations">
                <h2>Recommendations</h2>
                <ul>
                    <li><strong>Backtesting:</strong> Always perform thorough backtesting before deploying the strategy in a live environment to understand its performance and potential drawdowns.</li>
                    <li><strong>Risk Management:</strong> Adjust the <em>Risk Percentage</em> input to align with your overall risk tolerance. Conservative traders might opt for lower percentages, while aggressive traders may choose higher values.</li>
                    <li><strong>Optimize Parameters:</strong> Experiment with different values for <em>Factor</em>, <em>TP1 Multiple</em>, and <em>TP1 Percent</em> to find the optimal settings that suit your trading style.</li>
                    <li><strong>Monitor DST Adjustments:</strong> Ensure that your trading times account for DST changes, especially if trading across different time zones.</li>
                    <li><strong>Regular Reviews:</strong> Periodically review the strategy's performance and make necessary adjustments to adapt to changing market conditions.</li>
                    <li><strong>Diversify:</strong> Consider using the strategy in conjunction with other trading tools or strategies to diversify your trading approach.</li>
                </ul>
                <hr>
            </section>

            <!-- FAQs & Troubleshooting -->
            <section id="faqs--troubleshooting">
                <h2>FAQs & Troubleshooting</h2>

                <h4>1. Why are my orders being canceled too frequently?</h4>
                <p><strong>Possible Reasons:</strong></p>
                <ul>
                    <li><strong>Low <em>Max Signal Bars</em>:</strong> If set too low, the strategy may cancel orders before they get filled.</li>
                    <li><strong>Tight <em>Factor</em> Setting:</strong> A smaller factor increases the proximity of entry and SL, making it harder for orders to be filled.</li>
                    <li><strong>High Market Volatility:</strong> Rapid price movements can trigger cancellation conditions prematurely.</li>
                </ul>
                <p><strong>Solutions:</strong></p>
                <ul>
                    <li>Increase the <em>Max Signal Bars</em> to allow more time for orders to fill.</li>
                    <li>Adjust the <em>Factor</em> to provide more room for entry and SL levels.</li>
                    <li>Review market conditions and adjust settings accordingly.</li>
                </ul>

                <h4>2. How does DST adjustment affect my trading hours?</h4>
                <p>The strategy automatically adjusts the trading hours based on DST for London time. Ensure your chart's time zone aligns with the strategy's DST logic to maintain accurate trading sessions.</p>

                <h4>3. Can I disable the compounding feature?</h4>
                <p><strong>Yes:</strong> Set <em>Enable Compounding</em> to <strong>false</strong> in the Risk Management inputs to disable compounding. This will calculate risk based solely on the starting equity.</p>

                <h4>4. Why are there no trade signals displayed on my chart?</h4>
                <p><strong>Possible Reasons:</strong></p>
                <ul>
                    <li>Trading session is not active.</li>
                    <li>Signal conditions (bull/bear patterns and crossovers) are not being met.</li>
                    <li>Trade limits have been reached for the day.</li>
                </ul>
                <p><strong>Solutions:</strong></p>
                <ul>
                    <li>Verify that the trading session is active based on your defined hours.</li>
                    <li>Review the chart's timeframe and ensure it aligns with the strategy's logic.</li>
                    <li>Reset trade counts or adjust <em>Max Long Trades</em> and <em>Max Short Trades</em>.</li>
                </ul>

                <h4>5. How do I change the time to close all trades?</h4>
                <p>Navigate to the <strong>Close All Trades Management</strong> section in the strategy's settings.</p>
                <ol>
                    <li>Enable the feature by setting <em>Enable Close All Trades at Specific Time</em> to <strong>true</strong>.</li>
                    <li>Specify the desired <em>Close All Trades: Hour</em> and <em>Close All Trades: Minute</em>.</li>
                </ol>
                <hr>
            </section>

            <!-- Contact & Support -->
            <section id="contact--support">
                <h2>Contact & Support</h2>
                <p>For further assistance, customization requests, or feedback, please reach out through the following channels:</p>
                <ul>
                    <li><strong>Email:</strong> <a href="mailto:support@itradeaims.com">support@itradeaims.com</a></li>
                    <li><strong>Website:</strong> <a href="https://www.itradeaims.com" target="_blank">iTradeAIMS</a></li>
                    <li><strong>TradingView Profile:</strong> <a href="https://www.tradingview.com/u/itradeaims" target="_blank">iTradeAIMS on TradingView</a></li>
                </ul>
                <hr>
            </section>

            <!-- Appendix -->
            <section id="appendix">
                <h2>Appendix</h2>
                <h3>Pine Script Code Overview</h3>
                <p>For reference, here is a high-level overview of the key components within the Pine Script code:</p>
                <ul>
                    <li><strong>Strategy Declaration:</strong> Defines the strategy's name, overlay settings, calculation preferences, and initial capital.</li>
                    <li><strong>Input Definitions:</strong> Groups inputs into categories for organized configuration.</li>
                    <li><strong>DST Adjustments:</strong> Automatically adjusts trading hours based on DST periods for London.</li>
                    <li><strong>Trend Detection:</strong> Utilizes EMAs to determine market trends.</li>
                    <li><strong>Signal Patterns:</strong> Identifies bullish and bearish patterns based on candle formations.</li>
                    <li><strong>Risk Calculation:</strong> Determines position size based on risk percentage and equity.</li>
                    <li><strong>Order Management:</strong> Executes and manages buy/sell orders with advanced cancellation logic.</li>
                    <li><strong>Trade Closure:</strong> Implements both session end and specific time-based trade closures.</li>
                    <li><strong>Visual Indicators:</strong> Plots entry, SL, TP levels, and moving averages for easy monitoring.</li>
                </ul>
                <hr>
            </section>

            <!-- Conclusion -->
            <section id="conclusion">
                <h2>Conclusion</h2>
                <p><strong>The Ultimate NAS100 Strategy by iTradeAIMS - DST Version</strong> is a robust and flexible trading strategy designed to navigate the complexities of the NAS100 market. With its comprehensive risk management, dynamic signal filtering, and customizable trade closure options, it offers traders a powerful tool to enhance their trading performance. Always ensure to customize the settings to align with your trading objectives and conduct thorough backtesting to validate its effectiveness under various market conditions.</p>
                <hr>
            </section>
        </div>
    </div>

    <!-- Bootstrap JS (including Popper) -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <!-- Optional: Font Awesome JS for Icons (if needed) -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/js/all.min.js" integrity="sha512-Fo3rlrQd1kY5p1kE/mEjpCJDQKLy8NhvYtN6F/f19LaqX3G1nM/aGm1l+e8Q/S9doMFF3Tn9h/8+9i0wWgr4DA==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
</body>
</html>
