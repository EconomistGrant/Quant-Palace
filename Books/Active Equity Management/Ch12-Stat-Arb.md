# Dual Class Shares
after voting premium and liquidity premium: ratio should be stationary
equal dollar should be used instead of equal shares

# Correlation-based (short term) pairs trading
entry signal: daily return deviation, not a reversal of existing gap

# Cointegration-based (long term) pairs trading
P250: daily correlated pairs can be very different in the long run, consider rebalancing
cointegration: linear combination of price series is stationary

simple diff in cum return, sum of squares;
Dickey-Fuller, regression, residual, u = c + b*u_{-1} + eps, test null that b = 1

standardized deviation, optimize shreshold, or wait until convergence starts

cointegration can break
stop loss (does deviation exceeds historical high?) and time stop

exploits earnings announcement: another company can release negative earning surprise as well, the market has not fully incorporated

## filter candidates
residual needs to have sufficient vol over time
pairs with lower idiosyncratic risk, driven by macro events (fin/utility)
paris within same industry
speed of convergence: autoregressive process, delta u = theta (u bar - u) delta t + eps
1/theta = time scale

# benchmark (replicating portfolio based)
50 highest correlation stocks -> equal weights -> beta -> sort quantile by diff -> long short portfolio

quant meltdown
extremely skewed: majority small gains, small percent huge loss
