# Trading Costs
Explicit: commissions, fees, bid-ask spread
Implicit: delay costs, alpha decay, market impact, oppurtunity cost

## Bid-ask spread
Bid-ask spread, order processing costs, inventory risk, option effect, adverse selection(compensate liquidity providers for private information traders)
## Delay cost
decision made --- release order
e.g.: close price -> position next open
decision time price - mid-price after the first trade
## Alpha decay
disappearance of alpha as time goes by
## Market Impact
market impact = average trade price - market price before trade
reflects: 1) effective bid-ask spread 2) market vol and price vol 3) impact of other trades 4) alpha decay
if trades typically to be herding or contrarian, these are part of implicit costs

permnent impact = post price - market price before trades (30 min?)
usually modelled as a linear function of trade size

temporary impact = market impact - 1/2 permnent impact (on average, the trade basket only have half permnent impact, so deduct by half)

## Opportunity costs
fail to execute

# Trading Risk
price risk, liquidity risk, signaling risk


# Pre-Trade Analysis
Trading costs models
cost = sigma^k (A + B|X/VT|^beta + C|X/V| + epsilon)
/$cost = cost * |X|P
A =  bid-ask spread
B|X/VT| ^ beta = temporary effect (based on participation rate)
C|X/V| = permnent effect

a quick mind experiment:
T = 1.5 hours, market impact = mean 8bps std 10 bps, anual vol 30 percent = 85bps in 1.5 hour
if model capture 70 percent of variance => 1percent R^2

better model: remove beta drift, group by participation rate / sell&buy / style ...


# Portfolio Optimization
simple model: second order on dollar trade size
quadratic optimization

/$cost/gmv = theta|delta weight| + gmv*phi*|delta weight| ^ 2
total costs: theta * weight change vector + (weight change vector)'(gmv * PHI) (weight change vector)
PHI: diagonal matrix
...

# Volume and Vol Patterns
U shaped intraday valum

# Trading Strategies
balance between: reduce market impact by trading slowly and providing liquidity vs. reduce alpha decay and trading risk by trading fast and consuming liquidity
min (E(x) + lambda V(x))
## Execution Methods
high-touch, low-touch, zero-touch(Direct Market Access)
consider: costs, performance, efficiency

# Orders
immediate or cancel, fill or kill
limit order can outperform in high vol environments; venues often charge fees to remove liquidity and offer rebates to offer liquidity
hidden orders; iceberg orders; stop orders

# Trade Schedule
VWAP: minimizing market impact, expose to price risk; alpha decay
POV: meet pre-specified participation rate
Passive/Aggressive in the money: act based on whether the price moves in trader's favor
order routing

# Post-Trade Analysis
price trajectory, VWAP as benchmark

# Other implementation costs:
cash collateral, interest, 
...

