Defintion:

A stochastic process in discrete time is a sequence $(X_t)_{t=0}^{\infty}$ of random variables. We think of $t$ as "time".

stochastic process $X_t(\omega)$ is a function of both time $t$ and event $\omega$
Fix $t$: $X_t(\omega)$ is a random variable
Fix $\omega$: $X_t(\omega)$ is a function of time

When $\omega$ is fixed, i.e., the event has been realized, we have a particular sample path, which is a function of time only.

Each set {$t_1,\dots t_n$} is called a partition

Expectation function: $\mu_t = \mathbb{E}[X_t]$ and this is a function of time $t$
Covariance function: $\text{Cov}(X_t, X_s) = \mathbb{E}[(X_t - \mu_t)(X_s - \mu_s)]$ and this is a function of times $t$ and $s$
Auto correlation: the correlation between $X$ at different times
$$
\text{Corr}(X\_t, X\_s) = \frac{\text{Cov}(X\_t, X\_s)}{\sqrt{\\text{Var}(X\_t)}\sqrt{\text{Var}(X_s)}}
$$
A stochastic process $X_t(\omega)$ is stationary if for each (and all) partitions $\{t_1, \dots, t_n\}$, the distribution is invariant under a shift in time. That is, the random vectors $(X_{t_1}, \dots, X_{t_n})$ and $(X_{t_1+k}, \dots, X_{t_n+k})$ have the same distribution.

► **Properties of stationary process**
*   $\mathbb{E}[X_t] = \mathbb{E}[X_{t+k}] \Rightarrow \mu = \mu_t = \mu_{t+k}$
*   $Cov(X_t, X_s) = Cov(X_{t+k}, X_{s+k})$, which is some function of $s-t$ only

For any stochastic process $(X_t)$, the natural or generated filtration of $(X_t)$ is the filtration given by
$ \mathcal{F}_t = \sigma(X_0, X_1, \dots, X\_t) $
A random variable is $\mathcal{F}_m$-measurable if it depends onlyon the behavior of the stochastic process up until time $m$
We adopt the convention that whenever we do not specify a filtration explicitly, we mean to use the generated filtration

Recall that a sequence of $\sigma$-algebras $(\mathcal{F}_t)$ is known as a filtration if $\mathcal{F}_0 \subseteq \mathcal{F}_1 \subseteq \dots \subseteq \mathcal{F}$

A stochastic process $X = (X_t)$ is **adapted** to the filtration $(\mathcal{F}_t)$ if, for all $t$, $X_t$ is $\mathcal{F}_t$-measurable.

We can think of an adapted process is one that “cannot see
into the future”

A process is adapted if and only if for every realization and
every t, the value Xt is known at time t

That is, at any time t, the information in Ft is sufficient to
determine the value of Xs for all s ≤ t

### _Definition (Martingale)_
A process $M = (M_t)_{t=0}^\infty$ is a martingale if
(i) $(M_t)$ is adapted
(ii) $\mathbb{E}[|M_t|] < \infty$ for all t
(iii) $\mathbb{E}[M_{t+1} | \mathcal{F}_t] = M_t$ almost surely for all t.

We say that $M$ is a **submartingale** if, instead of (iii), we have
$\mathbb{E}[M_{t+1} | \mathcal{F}_t] \ge M_t$ almost surely

We say that $M$ is a **supermartingale** if, instead of (iii), we have
$\mathbb{E}[M_{t+1} | \mathcal{F}_t] \le M_t$ almost surely. <span style="color:red;">downward trend</span>

### _Corollary_
$M = (M_t)$ is a martingale if and only if it is both a submartingale and a supermartingale.