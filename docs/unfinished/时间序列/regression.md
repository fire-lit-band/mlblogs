# linear regression

$y_t=\beta_0+\beta_1x_t+\epsilon_t$

$R^2 = \frac{\sum(\hat{y}_t - \bar{y})^2}{\sum(y_t - \bar{y})^2},$

$\hat{\sigma}_e = \sqrt{\frac{1}{T - k - 1} \sum_{t=1}^{T} e_t^2},$

$\sum_{t=1}^{T} e_t = 0 \quad \text{and} \quad \sum_{t=1}^{T} x_{k,t} e_t = 0$

ACF plot for residuals

Residual plots against predictors

against fitted value

A plot of the residuals against the fitted values should also show no pattern. If a pattern is observed, there may be “heteroscedasticity” in the errors which means that the variance of the residuals may not be constant.

Observations that take extreme values compared to the majority of the data are called **outliers**. Observations that have a large influence on the estimated coefficients of a regression model are called **influential observations**.(outliers in the x direction)

### Spurious regression

二者并无关系，但regression却效果很好

# userful predictors

1. trend :t
2. dummy:1 yes 0 no

A dummy variable can also be used to account for an outlier in the data. Rather than omit the outlier, a dummy variable removes its effect. In this case, the dummy variable takes value 1 for that observation and 0 everywhere els

# Intervention variables

spike varialbe:take value in one period

step varible:take value zero before the intervention（永久改变）

# fourier series

m is seasonal period ,then 

maximum K=m/2

A regression model containing Fourier terms is often called a **harmonic regression**

$$\begin{align*}
x_{1,t} &= \sin\left(\frac{2\pi t}{m}\right), x_{2,t} = \cos\left(\frac{2\pi t}{m}\right), x_{3,t} = \sin\left(\frac{4\pi t}{m}\right), \\
x_{4,t} &= \cos\left(\frac{4\pi t}{m}\right), x_{5,t} = \sin\left(\frac{6\pi t}{m}\right), x_{6,t} = \cos\left(\frac{6\pi t}{m}\right),
\end{align*}$$

We describe a variable that is not included in our forecasting model as a **confounder** when it influences both the response variable and at least one predictor variable.