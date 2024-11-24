Strategy:
    Check if BTC-USDT went up by X % on Binance, then go long on ETH by Y % on OKX. Exit is either Y% profit or Z% loss


    The logic here is less liquid exchange will reflect market sentiment slower than a higher liquid exchange. However,
    I believe the spread to make would be small and would be consumed by transaction fees. Therefore, we can use cointegerated/correlated instruments with BTC that have higher volitality to have a profitable spread.

    To choose the optimal X, Y I use the same approuch introduced in question 1, to generate a heat map with the best total return.

    The optimal X is 0.2 & Y is 0.9

Summary:

    obtain_hourly_data: downloads hourly btc/eth data from binance and okx
    strategy: tries to find the optimal x & y, then backtests the x & y


Result:
    Total Return: 278.217 %
    CAGR: 15.414 %
    Daily Sharpe Ratio: 116.879
    Maximum Drawdown: -45.516%
    Calmar Ratio: 0.339





