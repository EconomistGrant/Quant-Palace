# Mean-Variance Optimization

## Efficient Frontier and CML
## Pros and Cons
only requires expected return vector and covariance matrix

very sensitive to inputs, estimation error, "error-maximization"
small insignificant changes in inputs -> significant change in weights

assumption: normal distribution (neg skewed, high kurtosis), quadratic utility function

# Risk Forecast
## covariance matrix
exponentially weighted to overweigh recent observation
vol clustering, negative corr between vol and return -> GARCH, JP morgan, Risk Metrics, p198

covariance matrix: high complexity, high cariance, extreme weights, correlation not stable over time
shrink off-diagonal by 20%

## Fundamental Factor Models
residual returns zero correlation, APT
style risk factors, BARRA
explanatory power and stability (autocorr)

factor exposures known (size, mom), but factor returns not known

## Economic Factor Models
factor returns known (GDP, CPI), stock exposure need to be estimated
regression

## Statistical Factor Models
SVD/PCA

## Limitation of Risk Models
estimated from history
linear assumption
multivariate normal assumption
crisis: all vol increases, underestimated factor vol; stock correlations rise
optimizing portfolio using a risk model: small number of risks compared with stocks -> null space, exposures to risk factors tends to be 0 -> other systematic risk not in the model can be very high, use another risk model to evaluate again? p205

normalized return should be N(0,1) -> sse over time should be chi-square -> adjust, tighter risk in modelling, p206

## risk-adjusted Information Coefficient
raw IC: cross sectional linear correlation between z-scores and realized future returns
#TODO

# Return Forecast
## Factor Group
time series of cross sectional correlation is preferred -> reveal patterns
select signal: two-stage regression, subsumes

multicollinearity: non-negative weights? Ridge? assign weights by IR, no estimation of covariance

## Factor Interactions
sequential screnning, decision tree

linear models: combine factor group (prescreen)
very hard to assign weigts: mean-var optimization, noise in covariance
simple weights: benchmark

Long-term investors: use short term signal as timing/execution, or sequential decision making
incorporation can be very hard

## Nonlinear models
logistic, ordinal logistic, less influenced by outliers
tree-based: less susceptible to outliners (even compared with logistic), tree structure; discontinuous around shrehold, overfitting
random forest, genetic programming

Return forecast, in common, does not influence risk forecast (var), 0.2 IC -> 4% R2, 96% of variance not explained

## Risk factors and alpha factors interaction
"optimized" portfolio can have unexpected exposure to unaccounted risk/factor p220
"the optimization step amplifies the problem by pushing the portfolio towards the factors or the fraction of the factors not in the risk model"
redefine covariance matrix with alpha factor?

## Black-Litterman
Bayesian, prior -> posterior
prior: market expected excess return?
view as a linear relation with mean and estimated vol
...

# Portfolio Constraints
## Risk constraints
total asset weights, maximum tracking error
## Diversification constraints
limit exposure
concentration (1/sum square weigts = effective number, quant manager typically > 100)
## liquidity and turnover constraints