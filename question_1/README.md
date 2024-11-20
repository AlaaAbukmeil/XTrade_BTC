Summary:
    There are two Jupyter files:
        obtain_data: to get usdt-btc data from both upbit * binance
        back_forward_test: to find best X & Y to optimize exchange arbitrage with training samples and then test them

    Running obtain_data will generate two csv files under directory binance_data & upbit_data. The default range is the last 800 days which is (2022-09-13 -> 2024-11-19). The script cleans the data (removing any na, make sure days are the same between both files, equal in length)

    Running back_forward_test will generate a heat map of daily sharpe ratios of different X & Y combination. X's range is between (0, 2) while Y's range is (-2,0), in every iteration, I increase 0.1 in both paramters. I use the first half of the data to generate the heat map (2022-09-13 -> 2023-10-18)

    After generating the heat map, the best combination is X >=0.0 & Y <=-0.1 which generates a daily Sharpe ratio of 0.05. Note: I put 0 for the benchmark in the sharpe ratio.

    After obtaining the best combination from the training sample, I forward test the combination. The end result is
    Cumulative Return for X >= 0.0 & Y <= -0.1 is 17.27% with daily sharpe ratio: 0.028, max_drawdown: -44.231 %, CAGR: 15.734 %

    I added a plot to verify the max drawdown in back_forward_test




