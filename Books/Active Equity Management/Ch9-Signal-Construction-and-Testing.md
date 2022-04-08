# Raw Factor -> Factor Score
trim: remove tails
winsorization: treat tails as shreshold value
smoothed z-score transformation p164
log transformation
generalized box-cox transformation ((x+delta)^lamda - 1)/lambda or ln(x+delta)

rank scores -> reverse cdf to be normal

only tails matter: p167

neutralization: industry de-meaned
for small sub-industry: use parent industry group mean

# Conditional Factors
time series risk ratio tratio = IVOL(1M) / IVOL(12M)
higher tratio: reduce momentum score
1 / (1 + a exp(b * (tratio - 1))) [sigmoid]

Information Discreteness: sign(TOTAL RETURN) * (%neg - %pos)
positive: discrete information, large and fewer upjumps

# Evaluation of Factor
## Information Coefficient
### Pearson correlation
cross sectional, between z-scores and realized future returns
linear to portfolio returns if treat z-scores as weights
E[rp] = sum E[ziri] = N * cov(zi,ri) = N * cor(zi, ri) * sigma_z * sigma_r = N * IC * sigma_r
to increase expected return: more stocks, higher IC, higher cross-sectional volatility

regress stock return against z-score: linear, coefficient on z-score = cov(zi, ri) / var(zi) = sigma_r * IC
### Spearman Correlation
remove outliers, but lose information

### IC over time
r = sigma*N*IC
E[r] = sigma * N * E[IC], assume cross sectional vol and number of stocks stable over time
IR(r) = E[r] / std(r) = E[IC] / std[IC] used to estimate IR

if IC is a true value overtime: std(IC) = sqrt((1-IC^2)/N-2) -> IR = E[IC] * sqrt(N), Fundamental Law of Active Management
in practice: change over time, plot IC against time

correlation of IC and cross-sectional volatility

information decay over time: robustness
smoothing: scores smoothing; rebalance part when information arrives

exit signal: 40th percentile, to reduce turnover

mispricing of high vol stocks tends to last longer, returns <- investors who willing to take idiosyncratic risk
# Long-short portfolio
zero-investment portfolio
- equal weights/market cap weights/sqrt mkt weights
- plot cum returns of all quantiles over time
- z-score weights
# Potential Pitfalls
data inaccuracy: fit missing data, last observation carried forward? can only trade at later price at halt?
data snooping: signal should be based on solid reasoning, should work in different periods/assets/markets, robust to small parameter changes
look-ahead bias: point-in-time database
survivorship bias: delisted stocks, value signals(relative low price stocks more likely to be delisted), CRSP include total return after delisted
return distribution, negative skewness and high kurtosis
low liquidity
market friction and costs: turnover and transaction costs < alpha 

rolling window backtest: underestimate standard error and inflated t-statistic #TODO
regime shift: decimal pricing, electric trading

paper: returns by quantiles, long-short portfolio
practitioners: cum returns over time, contemporary effect