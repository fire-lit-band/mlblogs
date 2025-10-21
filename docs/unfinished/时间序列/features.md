# ACF feature

 the sum of the first ten squared autocorrelation coefficients is a useful summary of how much autocorrelation there is in a series

- the first autocorrelation coefficient from the original data;
- the sum of squares of the first ten autocorrelation coefficients from the original data;
- the first autocorrelation coefficient from the differenced data;
- the sum of squares of the first ten autocorrelation coefficients from the differenced data;
- the first autocorrelation coefficient from the twice differenced data;
- the sum of squares of the first ten autocorrelation coefficients from the twice differenced data;
- For seasonal data, the autocorrelation coefficient at the first seasonal lag is also returned.

# STL feature

 For strongly trended data, the seasonally adjusted data should have much more 
variation than the remainder component. Therefore $\operatorname{Var}(R_t)/\operatorname{Var}(T_t + R_t)$ should be relatively 
small. 

But for data with little or no trend, the two variances should be approximately the same. So 
we define the strength of trend as:
$$F_T = \max \left( 0, 1 - \frac{\operatorname{Var}(R_t)}{\operatorname{Var}(T_t + R_t)} \right).$$

e strength of seasonality

$$F_S = \max \left( 0, 1 - \frac{\operatorname{Var}(R_t)}{\operatorname{Var}(S_t + R_t)} \right).$$