# stationary

$y_t$ is a stationary time series, then for all s ,  the distribution of $(y_t,\dots y_{t+s})$ does not depend on t

For a stationary time series, the ACF will drop to zero relatively quickly, while the ACF of non-stationary data decreases slowly.

## Differencing

$y_t'=y_t-y_{t-1}$

### second

$y_t''=y_t'-y_{t-1}'=y_t-2y_{t-1}-y_{t-2}$

### seasonal differencing

$y'_t=y_t-y_{t-m}$ lag-m differences

then $y_t=y_{t-m}+\epsilon_t$

# unit root test

*Kwiatkowski-Phillips-Schmidt-Shin (KPSS) test*

In this test, the null hypothesis is that the data are stationary,

In this case, the p-value is shown as 0.01 (and therefore it may be smaller than that), indicating that the null hypothesis is rejected.Then the data is not stationary

# backshift

$By_t=y_{t-1}$

$y'_t=y_t-y_{t-1}=y_t-By_t=(1-B)y_t$

$y''_t=(1-B)^2y_t$

$\begin{aligned}(1-B)(1-B^m)y_t&=(1-B-B^m+B^{m+1})y_t\\&=y_t-y_{t-1}-y_{t-m}+y_{t-m-1},\end{aligned}$

# autoregressive

$y_t=c+\phi_1y_{t-1}+\phi_2y_{t-2}+\dots+\phi_py_{t-p}+\epsilon_t$

AR(p) model 

lagged value of $y_t$

# MA(q)

$y_t=c+\varepsilon_t+\theta_1\varepsilon_{t-1}+\theta_2\varepsilon_{t-2}+\cdots+\theta_q\varepsilon_{t-q}$

It is possible to write any stationary AR(p) model as an MA($\infty$) model. 

Then the MA model is called **invertible**. That is, we can write any invertible MA(q) process as an AR(∞)

so the most recent observations have higher weight than observations from the more distant past. Thus, the process is invertible when $|\theta_1|<1$

# ARIMA

$y_t^{\prime}=c+\phi_1y_{t-1}^{\prime}+\cdots+\phi_py_{t-p}^{\prime}+\theta_1\varepsilon_{t-1}+\cdots+\theta_q\varepsilon_{t-q}+\varepsilon_t,$

p: order of the autoregressive part

d: degree of first differencing involved

q: order of the moving average part

$(1-\phi_1B-\cdots-\phi_pB^p)(1-B)^dy_t\quad=\quad c+(1+\theta_1B+\cdots+\theta_qB^q)\varepsilon_t$

The value of d also has an effect on the prediction intervals — the higher the value of d, the more rapidly the prediction intervals increase in size.

PACF

ARIMA(p,d,0) ACF迅速减小

PACF突然在p之后没有了

ARIMA(0,d,q)

PACF 慢慢减小

ACF在p之后突然减小

1. If necessary, transform the data (using a Box-Cox transformation) to stabilise the variance.

| The number of differences 0≤d≤2 is determined using repeated KPSS tests. |
| ------------------------------------------------------------ |
| The values of p and q are then chosen by minimising the AICc after differencing the data d times. Rather than considering every possible combination of p and q, the algorithm uses a stepwise search to traverse the model space. |
| Four initial models are fitted:ARIMA(0,d,0),ARIMA(2,d,2),ARIMA(1,d,0),ARIMA(0,d,1).A constant is included unless d=2. If d≤1, an additional model is also fitted:ARIMA(0,d,0) without a constant. |
| The best model (with the smallest AICc value) fitted in step (a) is set to be the “current model”. |
| Variations on the current model are considered:vary p and/or q from the current model by ±1;include/exclude c from the current model.The best model considered so far (either the current model or one of these variations) becomes the new current model. |
| Repeat Step 2(c) until no lower AICc can be found.           |

 ℓ−K degrees of freedom in the test

### Portmanteau tests of residuals for ARIMA models

l is number of lags

K is the number of AR and MA parameters

$\begin{aligned}&\text{ivalcnuly as}\\&(1-\phi_1B-\cdots-\phi_pB^p)(1-B)^d(y_t-\mu t^d/d!)=(1+\theta_1B+\cdots+\theta_qB^q)\varepsilon_t,\end{aligned}$

$c=\mu(1-\phi_1-\cdots-\phi_p)\mathrm{~and~}\mu\text{ is the mean of }(1-B)^dy_t.$

Thus, the inclusion of a constant in a non-stationary ARIMA model is equivalent to inducing a polynomial trend of order d in the forecasts.

For d=0 or d=1, a constant will be included if it improves the AICc value. If d>1 the constant is always omitted as a quadratic or higher order trend is particularly dangerous when forecasting.

The stationarity conditions for the model are that the p complex roots of $\phi$(B) lie outside the unit circle, and the invertibility conditions are that the q complex roots of$\theta$(B) lie outside the unit circle. 
