Summary:
    There are two files:
        obtain_hourly_data: would download hourly data from binance since Jan 2021
        alphas: would compute the three alphas + implement the following strategy
    


Strategy:
    Create a 24-hour window of each alpha's values and calcualte the mean
    For the following hour, calculate its z-score. (value - rolling-window-mean)/standard deviation of the window
    If the z score is significant (more than 1 standard deviation) then enter, if the z score returns to normal range (less than 0.5) then exit

    Now we will have three signals based on each alpha z-score. I found that taking signal alpha b as a must and either alpha a/c yields best returns.

    I believe the reason why I need to take Alpha B is because it has a much higher disparities when the price changes due to 5 power factor

    There is a performance image that reflect's performance of the strategy

Result:
    Maximum Drawdown: -42.33%
    Daily Sharpe Ratio: 5.239
    CAGR: 104.20%
    Calmar Ratio: 2.461
    Total Return: 1504.79%

Note:
    Even though return is high, the strategy does not account for transactions fees. It would have an impact since there are many transactions.
    Also it has a high max drawdown, investors would be wary of these high mdd.
    A usual quantitative fund would also be leveraged and with this mdd, the fund would be wiped out with current mdd. Assuming a half-kelly leverage ratio






