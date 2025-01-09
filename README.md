Exchange Arbitrage Algo

Under each folder lays an algo strategy with its backtest performance and detailed explanation

exchange_arb

  When BTC future goes up by x% on Binance, go long BTC by y% on upbit and vice versa. To determine the best x% and y%, I generate a
  heat map with the best performers.

exchange_arb_correlated

  When BTC future goes up by x% on Binance, go long ETH by y% on upbit and vice versa.
  The idea here is less liquid exchanges reflect market sentiment slower than more liquid exchanges. However, the spread might be
  too small, so we can trade on a correlated instrument with higher volatility to make it profitable.

z_score_arb

  Define three alpha parameters and create a 24-hour window. If a value is -+2 standard deviation away from the 24-hour mean, then
  go long/short accordingly. 

