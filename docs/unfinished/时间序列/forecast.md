1. data preration
2. visualise
3. define model and train

# simple

## mean method

$\hat{y}_{T+h|T} = \bar{y} = (y_1 + \dots + y_T)/T.$

## naive

$\hat{y}_{T+h|T} = y_T$

## seansonal naive

$\hat{y}_{T+h|T} = y_{T+h-m(k+1)},$

where m= the seasonal period, and k is the integer part of (h−1)/m (i.e., the number of complete years in the forecast period prior to time T+h).

# drift method

$\hat{y}_{T+h|T} = y_T + \frac{h}{T-1} \sum_{t=2}^{T} (y_t - y_{t-1}) = y_T + h \left( \frac{y_T - y_1}{T-1} \right).$

# fitted value and residual

Each observation in a time series can be forecast using all previous observations. We call these **fitted values** and they are denoted by $\hat{y}_{t|t-1}$, meaning the forecast of $y_t$ based on observations $y_1,…,y_{t−1}$

and somtimes we write $\hat{y}_t$

## residual

$e_t=y_t-\hat{y_t}$

**innovation residuals**:the residual on the trasnformed scale

## good forecast

residual uncorrelated

innovation residual zero



it is useful (but not necessary) for the residuals to also have the following two properties.

1. The innovation residuals have constant variance. This is known as “homoscedasticity”.
2. The innovation residuals are normally distributed.

 **portmanteau test**

s the **Box-Pierce test**, 

e **Ljung-Box test**

# prediction interval

## one step

When forecasting one step ahead, the standard deviation of the forecast distribution can be estimated using the standard deviation of the residuals given by

$$\hat{\sigma} = \sqrt{\frac{1}{T-K-M} \sum_{t=1}^{T} e_t^2}$$

where \(K\) is the number of parameters estimated in the forecasting method, and \(M\) is the number of missing values in the residuals. (For example, \(M = 1\) for a naive forecast, because we can't forecast the first observation.)

## mutistep

mean:$\hat{\sigma}_h = \hat{\sigma}\sqrt{1 + 1/T}$

naive:$\hat{\sigma}_h = \hat{\sigma}\sqrt{h}$

seasonal naive:$\hat{\sigma}_h = \hat{\sigma}\sqrt{k+1}$

drift:$\hat{\sigma}_h = \hat{\sigma}\sqrt{h(1 + h/(T-1))}$

#  bootstrapped residuals

use the residual from the past to simulate the future

compute prediction intervals by calculating percentiles of the future sample paths

## bias adjustment

he difference between the simple back-transformed forecast given by [(5.2)](https://otexts.com/fpp3/ftransformations.html#eq:backtransform) and the mean given by [(5.3)](https://otexts.com/fpp3/ftransformations.html#eq:backtransformmean) is called the **bias**. When we use the mean, rather than the median, we say the point forecasts have been **bias-adjusted**.

$$\hat{y}_{T+h|T} = 
\begin{cases}
    \exp(\hat{w}_{T+h|T}) \left[ 1 + \frac{\sigma_h^2}{2} \right] & \text{if } \lambda = 0; \\
    (\lambda \hat{w}_{T+h|T} + 1)^{1/\lambda} \left[ 1 + \frac{\sigma_h^2(1-\lambda)}{2(\lambda \hat{w}_{T+h|T}+1)^2} \right] & \text{otherwise;}
\end{cases}$$

we use the mean, the point have been bias-adjusted

# decomposition

forecast the seasonal compoent and seasonally adjustment compent

# evaluate

When comparing forecast methods applied to a single time series, or to several time series with the same units, the MAE is popular as it is easy to both understand and compute. 

A forecast method that minimises the MAE will lead to forecasts of the median, while minimising the RMSE will lead to forecasts of the mean. 

Consequently, the RMSE is also widely used, despite being more difficult to interpret.

$p_t=100e_t/y_t$

MAPE=mean($|p_t|$)=

Measures based on percentage errors have the disadvantage of being infinite or undefined if yt=0 for any t in the period of interest, and having extreme values if any yt is close to zero. Another problem with percentage errors that is often overlooked is that they assume the unit of measurement has a meaningful zero

$\text{sMAPE} = \text{mean}(200|y_t - \hat{y}_t|/(y_t + \hat{y}_t)).$

For a non-seasonal time series

$q_j = \frac{e_j}{\frac{1}{T-1} \sum_{t=2}^{T} |y_t - y_{t-1}|}.$

if error>1 then, the forecast worse than naive forecast

seasonal

$q_j = \frac{e_j}{\frac{1}{T-m} \sum_{t=m+1}^{T} |y_t - y_{t-m}|}.$

*mean absolute scaled error* MASE=mean($|q_j|$)

root mean squares scales error 

$RMSSE=\sqrt{mean(q_j^2)}$

$q^2_j = \frac{e^2_j}{\frac{1}{T-m} \sum_{t=m+1}^{T} |y_t - y_{t-m}|^2}.$

# evaluate distributional forecast

quantile score

### Winkler Score

### Continuous Ranked Probability Score

### Scale-free comparisons using skill scores