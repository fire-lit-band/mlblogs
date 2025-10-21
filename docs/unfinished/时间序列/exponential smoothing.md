# simple exponential smoothing

suitable for forecast data with no clear trend or seasonal pattern

$\hat{y}_{T+1|T} = \alpha y_{T} + \alpha(1-\alpha)y_{T-1} + \alpha(1-\alpha)^2 y_{T-2} + \dots$

## component form

forecast eqaution $\hat{y}_{t+h|t} = l_t$

Smoothing equation$ \ell_t = \alpha y_t + (1-\alpha)\ell_{t-1}$

a “flat” forecast function:

$\hat{y}_{t+h|t}=\hat{y}_{t+1|t} = l_t$

Choose parameter

$\text{SSE} = \sum_{t=1}^{T} (y_t - \hat{y}_{t|t-1})^2 = \sum_{t=1}^{T} e_t^2.$

# hots

$\begin{aligned}\text{Forecast equation}&&\hat{y}_{t+h|t}&=\ell_t+hb_t\\\text{Level equation}&&\ell_{t}&=\alpha y_t+(1-\alpha)(\ell_{t-1}+b_{t-1})\\\text{Trend equation}&&b_{t}&=\beta^*(\ell_t-\ell_{t-1})+(1-\beta^*)b_{t-1},\end{aligned}$

# dampeed trend method

Empirical evidence indicates that these methods tend to over-forecast, especially for longer forecast horizons. 

$\begin{aligned}\hat{y}_{t+h|t}&=\ell_t+(\phi+\phi^2+\cdots+\phi^h)b_t\\\ell_{t}&=\alpha y_t+(1-\alpha)(\ell_{t-1}+\phi b_{t-1})\\b_{t}&=\beta^*(\ell_t-\ell_{t-1})+(1-\beta^*)\phi b_{t-1}.\end{aligned}$

# seasonality

$\begin{aligned}\hat{y}_{t+h|t}&=\ell_t+hb_t+s_{t+h-m(k+1)}\\\ell_{t}&=\alpha(y_t-s_{t-m})+(1-\alpha)(\ell_{t-1}+b_{t-1})\\b_{t}&=\beta^*(\ell_t-\ell_{t-1})+(1-\beta^*)b_{t-1}\\s_{t}&=\gamma(y_t-\ell_{t-1}-b_{t-1})+(1-\gamma)s_{t-m},\end{aligned}$

k is the integet part of (h-1)/m

m is number of season

$\begin{aligned}\hat{y}_{t+h|t}&=(\ell_t+hb_t)s_{t+h-m(k+1)}\\\ell_{t}&=\alpha\frac{y_t}{s_{t-m}}+(1-\alpha)(\ell_{t-1}+b_{t-1})\\b_{t}&=\beta^*(\ell_t-\ell_{t-1})+(1-\beta^*)b_{t-1}\\s_{t}&=\gamma\frac{y_t}{(\ell_{t-1}+h_{t-1})}+(1-\gamma)s_{t-m}.\end{aligned}$

trend:additive or dampen

seasonal: additive and mutiplicative

## ETS

 We label each state space model as ETS(⋅,⋅,⋅) for (Error, Trend, Seasonal). This label can also be thought of as ExponenTial Smoothing. Using the same notation as in Table [8.5](https://otexts.com/fpp3/taxonomy.html#tab:taxonomy), the possibilities for each component (or state) are: Error ={A,M}, Trend ={N,A,Ad} and Seasonal ={N,A,M}.

for simple expontential smoothing

$l_t=l_{t-1}+\alpha(y_t-l_{t-1})=l_t+\alpha e_t$

$y_t=l_t+\epsilon_t$refer as the measurement(observation eqution)

$l_t=l_{t-1}+\alpha\epsilon_t$as the state equation

$0<\beta<\alpha,0<\gamma<1-\alpha,0<\alpha<1,0.8<\phi<0.98$

AIC=-2log(L)+2k

$AIC_c=AIC+\frac{2k(k+1)}{T-k-1}$

$BIC=AIC+k(log(T)-2)$

Point forecasts can be obtained from the models by iterating the equations for t=T+1,…,T+h and setting all $\epsilon_t=0$ for t>T.
