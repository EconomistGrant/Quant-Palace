# Moving Averages
SMA
EMAt = alpha * Ct + (1-alpha) * EMAt-1
WMA = weights linear to time diff

short-term SMA crosses long-term SMA

variable length: strong trend, more recent weight to capture
VMA = (alpha * VI) * Ct + (1 - alpha*VI) * VMA

Efficiency Ratio: Direction / Volatility
Direction = |Ct - Ct-N|, Volatility = sum |Ct-i - Ct-i-1|
1 to be efficient (same direction over time), 0 to be not efficient 

DEMA = EMA(P) + EMA(P - EMA) = 2 * EMA(P) - EMA(EMA(P))
DEMA forces historical weights to be negative
very responsive and accurate
65页的图很好看

# Channel Breakouts
long when today high is the N day high, and exit when today's low is M day low

volume confirmation; support level confirmation

trend strength (non range-bounded) confirmation: 
True Range = max(Ht - Lt, Ht - Ct-1, Ct-1 - Lt) = max(Ht, Ct-1) - min(Lt, Ct-1)
ATRt = EMA of TR
+DMt = Ht - Ht-1 if Ht - Ht-1 > Lt-1 - Lt (均值变大了？) 0 otherwise
+DIt = EMA of (+DMt / ATRt)

-DMt = Lt - Lt-1 if Lt-1 - Lt > Ht - Ht-1, 0 otherwise
-DIt = EMA of (-DMt / ATRt)

Directional index DXt = (+DIt - -DIt) / (+DIt + -DIt) * 100
ADX = Average Directional Index
<20: range bound, weak trend; >30, strong trend

Reverse Arrangement Test, count % of sign(Ci - Cj) during the interval

ADX and RAT does not help forecast, slow at generating meaningful signals

market regime: if uptrend yesterday, close higher than MA low...

1. there is a trend
2. trend > lag of your formula
fat tails: large winning trade compensate for small losing trades?

# Mean Reversion Signals
## Bollinger Bands
Middle Band: SMA
Upper band: SMA + K * vol, ...
capture oversold / overbought market

Bollinger Z-score
## Relative Strength Index
gain_t = (Ct - Ct-1)+
mean gain = 1/N gain_t + N-1 / N mean gain_t-1
RSI = 100 * mean gain / mean gain + mean loss

## Stochastic Oscillator
%K_t,N Fast =  (C - LL_N) / (HH_N - LL_N) * 100
%D_t,N Fast = n-day SMA (%K_t,N Fast) (n = 3)
too sensitive:
Full %K = m-day SMA(Fast%K)
Full %D = m-day SMA(Full%K)

no signal has consistently outperformed other signals at all times or for all assets!
