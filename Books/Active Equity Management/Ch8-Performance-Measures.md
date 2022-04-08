# Trade Level
P/L: average win / average loss
hit rate: wining trades percentage
# Portfolio Level
turnover: 1/2 * sum(weight change) for fully invested portfolio
short position cumulative return: 1 - long cum return

# Sharpe Ratio and Information Ratio
SR = E[alpha] / sigma_alpha
IR = E[r-rb] / sqrt(var(r-rb))
tracking error

dimension: assume no autocorr, alpha and variance both grow linearly with time
t = alpha / s.e. of alpha = IR * sqrt(T-1)

asymptotic distribution of IR: p155
consider skewness and kurtosis: p156

# VAR
sample size issue when estimate tail risk: 10 years weekly return, 1% only 5 data point
does not depend on the shape of tail, does not describe the loss on the left tail
not sub-additive and not a coherent measure of risk

conditional value at risk: average loss when the loss is at least as large as value at the risk
CVAR(A+B) <= CVAR(A) + CVAR(B)
conditional sharpe ratio: E[alpha] / CVAR of alpha

Sortino Ratio = E[alpha] - MAR / Downside Deviation
Downside Deviation = sqrt(1/N(a < MAR) * sum[min(a - MAR, 0)^2] )

Calmar ratio = E[alpha]/maximum drawdown

# Leverage
Kelly criterion, optimal fraction of the current capital to bet 
alpha / sigma^2

sigma estimation is poor
half kelly
EV = vol + 2*s.e.(vol)

consider maximum drawdown: 20%
rule of thumb: below 3

