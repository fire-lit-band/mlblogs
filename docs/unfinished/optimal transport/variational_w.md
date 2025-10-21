has a unique ability, not shared with other information divergences, to leverage physical ideas (mass displacement) and geometry (a ground cost between observations or bins) to compare measures.

compare distribution $\beta$ with $\{\alpha_\theta,\theta\in\Theta\}$

$\min_{\theta\in\Theta}\mathcal{E}(\theta)\overset{\mathrm{def.}}{\operatorname*{\operatorname*{=}}}\mathcal{L}_c(\alpha_\theta,\beta).$

when the parameter $\theta$ is itself a histogram, namely $\Theta=\Sigma_n$ and $\alpha_\theta=\theta$, or more generally when $\theta$ describes $K$ weights in the simplex, $\Theta=\Sigma_K$, and $\alpha_\theta=\sum_{i=1}^K\theta_i\alpha_i$ is a convex combination of known atoms $\alpha_1,\ldots,\alpha_K$ in $\Sigma_N$, Problem (9.1) remains convex

(the first case corresponds to the barycenter problem, the second to one iteration of the dictionary learning problem with a Wasserstein loss [Rolet et al., 2016])

1. 转化成特殊分布的w2 distance

Eulerian or Lagrangian.

a Eulerian discretization is the most suitable when measures are supported on a lowdimensional space (as when dealing with shapes or color spaces), or for intrinsically discrete problems (such as those arising from string or text analysis)

take continuous values in high-dimensional spaces, a Lagrangian perspective

# Eulerian Discretization

A first way to discretize the problem is to suppose that both distributions $\beta=\sum_{j=1}^m\mathrm{b}_j\delta_{y_j}$

$\alpha_\theta=\sum_{i=1}^n\mathbf{a}(\theta)_i\delta_{x_i}$

Such locations might stand for cells dividing the entire space of observations in a grid, or a finite subset of points of interest in a continuous space

$\alpha_\theta$ can be represented as $\mathbf{a}:\theta\mapsto\mathbf{a}(\theta)\in\Sigma_n$ might be sprase in high dimension

9.1 is not differntiable ,so in order to obtain smooth minimization,use entropic regularized OT

$\min_{\theta\in\Theta}\mathcal{E}_E(\theta)\overset{\mathrm{def.}}{\operatorname*{=}}\mathcal{L}_\mathbf{C}^\varepsilon(\mathbf{a}(\theta),\mathbf{b})\quad\mathrm{where}\quad\mathbf{C}_{i,j}\overset{\mathrm{def.}}{\operatorname*{=}}c(x_i,y_j).$

$(\mathbf{a},\mathbf{b})\mapsto\mathcal{L}_{\mathbf{C}}^{\varepsilon}(\mathbf{a},\mathbf{b})$is convex and differentiable.

$\nabla\mathrm{L}_\mathbf{C}^\varepsilon(\mathbf{a},\mathbf{b})=(\mathbf{f},\mathbf{g})$ and $\sum_if_i=\sum_ig_i=0$

the function is differentiable if they are unique.

$\nabla\mathcal{E}_E(\theta)=[\partial\mathbf{a}(\theta)]^\top(\mathbf{f})$

where $\partial \mathbf{a} ( \theta ) \in \mathbb{R} ^{n\times \mathrm{dim}( \Theta ) }$ is the Jacobian (differential) of the map $\mathbf{a}(\theta)$, and where $\mathbf{f}\in\mathbb{R}^n$ is the dual potential vector associated to the dual entropic OT (4.30) between

# lagrangian 

$$\alpha_\theta\:=\:\frac1n\sum_i\delta_{x(\theta)_i}$$

$\min_\theta\mathcal{E}_L(\theta)\overset{\mathrm{def.}}{\operatorname*{=}}\mathcal{L}_{\mathbf{C}(x(\theta))}^\varepsilon(1_n/n,\mathbf{b})\quad\mathrm{where}\quad\mathbf{C}(x)_{i,j}\overset{\mathrm{def.}}{\operatorname*{=}}c(x(\theta)_i,y_j).$

entropic OT loss is a smooth function of the cost matrix and gives the expression of its gradient.

$$\mathbf{C}\mapsto\mathcal{R}(\mathbf{C})\stackrel{\mathrm{def.}}{=}\mathcal{L}_{\mathbf{C}}^{\varepsilon}(\mathbf{a},\mathbf{b})$$ is concave and smooth and

$\nabla\mathcal{R}(\mathbf{C})=\mathbf{P}$

$x= ( x_i) _i= 1^n\in \mathcal{X} ^n\mapsto \mathcal{F} ( x) \overset {\mathrm{def. }}{\operatorname* { \operatorname* { = } } }$ $\mathcal{L}_{\mathbf{C}(x)}(1_n/n,\mathbf{b})$ is smooth and that

$$\nabla\mathcal{F}(x)=\left(\sum_{j=1}^m\mathrm{P}_{i,j}\nabla_1c(x_i,y_j)\right)_{i=1}^n\in\mathcal{X}^n,$$

$\nabla_1 c$is the gradient with respect to the first variable

this gradient is Id − T , where T is the barycentric projection

it is usually better to differentiate directly the output of Sinkhorn’s algorithm, using reverse mode automatic differentiation

Sinkhorn divergences as introduced in (4.48), rather than the quantity $L_C^\epsilon$ in (4.2) and differentiating it directly as a composition of simple maps using the inputs

The only downside is that reverse mode automatic differentation is memory intensive (the memory grows proportionally with the number of iterations). There exist, however, subsampling strategies that mitigate this problem

# Wasserstein Barycenters, Clustering and Dictionary Learning

$$\min_{x\in\mathcal{X}}\sum_{s=1}^S\lambda_sd(x,x_s)^p$$

One can retrieve various notions of means (e.g. harmonic or geometric means over X = R+) using this formalism. This process is often referred to as the “Fréchet” or “Karcher” mean

is usually a difficult nonconvex optimization problem. Fortunately,

Fréchet means over the Wasserstein space

$$\min_{\mathbf{a}\in\Sigma_n}\sum_{s=1}^S\lambda_s\mathrm{L}_{\mathbf{C}_s}(\mathbf{a},\mathbf{b}_s)$$

$$\min_{\alpha\in\mathcal{M}_+^1(\mathcal{X})}\sum_{s=1}^S\lambda_s\mathcal{L}_c(\alpha,\beta_s)$$

if $\mathcal{X}=R^d,c(x,y)=\|x-y\|^2$this barycenter is unique.

$\int_\mathcal{X}x\mathrm{d}\alpha^\star(x)=\sum_s\lambda_s\int_\mathcal{X}x\mathrm{d}\alpha_s(x)$

approximating Lc using entropic regularization results in smoothed out assignments that appear in soft-clustering variants of k-means, such as mixtures of Gaussians

## barycenter

$$\min_{\alpha\in\mathcal{M}_+^1(\mathcal{X})}\mathbb{E}_M(\mathcal{L}_c(\alpha,\beta))=\int_{\mathcal{M}_+^1(\mathcal{X})}\mathcal{L}_c(\alpha,\beta)\mathrm{d}M(\beta)$$

where $\beta$ is a random measure distributed according to $M.$ Drawing uniformly at random a finite number $S$ of input measures $(\beta_s)_s=1^S$ according to $M$, one can then define $\hat{\beta}_S$ as being a solution of (9.11) for uniform weights $\lambda_s=1/S$ (note that

as S increase,then $\beta_S$ convergence to the barycenter of $\beta$

For $\mathcal{X}=R^d$,with ground cost $c(x,y)=\|x-y\|^2$,

we define optimal transportation maps between $T_s$ between $\alpha,\alpha _s$,$T_{s,\sharp}\alpha=\alpha_s$

$T^{(\alpha)}\overset{\mathrm{def.}}{\operatorname*{=}}\sum_{s=1}^S\lambda_sT_s$

vrono, vquor vo viro brwaront or o vum

$v$ омит опи конихо олодир очивон омомо орозамон

As shown in , first order optimality conditions of the barycenter problem  actually read $T^(\alpha^*)=\mathbb{l}_{\mathbb{R}^d}$ (the identity map) at the optimal measure $\alpha^\star$ (the barycenter), and it is shown inthat the barycenter $\alpha^\star$ is the unique  to the fixed-point

equation

$$G(\alpha)=\alpha\quad\mathrm{where}\quad G(\alpha)\stackrel{\mathrm{def.}}{=}T_\sharp^{(\alpha)}\alpha,$$

Under mild conditions on the input measures, Álvarez-Esteban et al.[2016] and Zemel and Panaretos [2018] have shown that $\alpha\mapsto G(\alpha)$ strictly decreases the objective function of (9.13) if $\alpha$ is not the barycenter and that the fixed-point iterations $\alpha^(\ell+1)\overset{\mathrm{def.}}{\operatorname*{=}}G(\alpha^{(\ell)})$ converge to the barycenter $\alpha^\star.$ This fixed point algorithm can be used in cases where the optimal transportation maps are known in closed form $(e.g.$ for Gaussians). Adapting this algorithm for empirical mea-

$$\alpha^{(\ell+1)}\stackrel{\mathrm{def.}}{=}G(\alpha^{(\ell)})$$

也就是optimal在重心，算最优解约等于算最优的重心

$$T_{r,u}:x\mapsto rx+u$$

$$\alpha_s=T_{r_s,u_s,\sharp}\alpha_0$$

$\left.\alpha_{\lambda}=T_{r^{\star},u^{\star},\sharp}\alpha_{0}\quad\mathrm{where}\quad\left\{\begin{array}{l}r^{\star}=(\sum_{s}\lambda_{s}/r_{s})^{-1},\\u^{\star}=\sum_{s}\lambda_{s}u_{s}.\end{array}\right.\right.$

$$\text{s }T_\sharp\alpha_0=\alpha_1$$

$a_\lambda=\begin{array}{c}(\lambda_1\mathrm{Id}+\lambda_2T)_\sharp\alpha_0.\end{array}$

## Entropic approximation of barycenters

$$\min_{{\mathbf{a}\in\Sigma_{n}}}\sum_{s=1}^{S}\lambda_{s}\mathcal{L}_{{\mathbf{C}_{s}}}^{\varepsilon}(\mathbf{a},\mathbf{b}_{s})$$

$$\min_{(\mathbf{P}_s)_s}\:\left\{\sum_s\lambda_s\varepsilon\mathbf{KL}(\mathbf{P}_s|\mathbf{K}_s)\::\:\forall s,\mathbf{P}_s^\mathrm{T}\mathbf{1}_m=\mathbf{b}_s,\:\mathbf{P}_1\mathbf{1}_1=\cdots=\mathbf{P}_S\mathbf{1}_S,\right\}$$

$$\mathbf{P}_s=\operatorname{diag}(\mathbf{u}_s)\mathbf{K}\operatorname{diag}(\mathbf{v}_s),$$

$$\forall\:s\in[[1,S]],\quad\mathbf{v}_s^{(\ell+1)}\stackrel{\mathrm{def.}}{=}\frac{\mathbf{b}_s}{\mathbf{K}_s^{\mathrm{T}}\mathbf{u}_s^{(\ell)}},$$



$$\forall\:s\in[[1,S]],\quad\mathbf{u}_s^{(\ell+1)}\stackrel{\mathrm{def.}}{=}\frac{\mathbf{a}^{(\ell+1)}}{\mathbf{K}_s\mathbf{v}_s^{(\ell+1)}},$$


where $\mathbf{a} ^{( \ell + 1) }\overset {\mathrm{def. }}{\operatorname* { \operatorname* { = } } }\prod ( \mathbf{K} _s\mathbf{v} _s^{( \ell + 1) }) ^{\lambda _s}.$

$(u_s,v_s)=(e^{f_s/\epsilon},e^{g_s/\epsilon})$,where $(f_s,g_s)$ are the solution of the following program

$$\max_{(\mathbf{f}_s,\mathbf{g}_s)_s}\:\left\{\sum_s\lambda_s\left(\langle\mathbf{g}_s,\:\mathbf{b}_s\rangle-\varepsilon\langle\mathbf{K}_se^{\mathbf{g}_s/\varepsilon},\:e^{\mathbf{f}_s/\varepsilon}\rangle\right)\::\:\sum_s\lambda_s\mathbf{f}_s=0\right\}$$

# gradient flow

$$\mathbf{a}^{(\ell+1)}\stackrel{\mathrm{def.}}{=}\underset{\mathbf{a}}{\operatorname*{argmin}}\:\mathrm{W}_{p}(\mathbf{a},\mathbf{a}^{(\ell)})^{p}+\tau F(\mathbf{a}).$$

$$\frac{\partial\alpha_t}{\partial t}=\mathrm{div}(\alpha_t\nabla(F'(\alpha_t))),$$

$t=\tau l$

$$F(\alpha+\varepsilon\xi)=F(\alpha)+\varepsilon\int_{\mathcal{X}}F'(\alpha)\mathrm{d}\xi(x)+o(\varepsilon).$$

F=-H

$$H(\alpha)=-\int_{\mathbb{R}^d}\rho_\alpha(x)(\log(\rho_\alpha(x))-1)\mathrm{d}x$$

then  

$$\frac{\partial\alpha_t}{\partial t}=\Delta\alpha_t,$$

$x^{(\ell+1)}=\underset{x\in\mathcal{X}}{\operatorname*{\operatorname*{argmin}}}d(x^{(\ell)},x)^2+\tau\langle\nabla F(x^{(\ell)}),x\rangle.$ and is unstable

$$\alpha_t\:=\:\frac1n\sum_{i=1}^n\delta_{x_i(t)}$$

$$X(t)\:=\:(x_i(t))_i$$

$\mathcal{F}(X)=F(\frac{1}{n}\sum_{i=1}^n\delta_{x_i})$

$F(\alpha)=\int_{\mathcal{X}}V(x)$d$\alpha(x)$ and quadratic interactions $F(\alpha)=\int_{\mathcal{X}^2}W(x,y)$d$\alpha(x)$d$\alpha(y)$,
in which case one can use respectively


$$\mathcal{F}(X)=\frac1n\sum_iV(x_i)\quad\mathrm{and}\quad\mathcal{F}(X)=\frac1{n^2}\sum_{i,j}W(x_i,x_j).$$

density estimator$\mathcal{F}(X)=\frac{1}{n}\sum_{i}\log(d_{X}(x_{i}))\quad\mathrm{where}\quad d_{X}(x)=\min_{x^{\prime}\in X,x^{\prime}\neq x}\left\|x-x^{\prime}\right\|;$

for small enough step sizes,W2 mathces the Euclidean distance on the points,.i.e.|t-t'|small$\mathcal{W}_2(\alpha_t,\alpha_{t^{\prime}})=\|X(t)-X(t^{\prime})\|.$

The gradient flow is thus equivalent to the Euclidean flow on positions

$$X'(t)=-\nabla\mathcal{F}(X(t))$$

$X^{(\ell+1)}\overset{\mathrm{def.}}{\operatorname*{=}}X^{(\ell)}-\tau\nabla\mathcal{F}(X^{(\ell)}).$

Note that for this particular case of linear Fokker–Planck equation, it is possible also to resort to stochastic PDEs methods, and it can be approximated numerically by evolving a single random particle with a Gaussian drift. The convergence of these schemes (so-called Langevin Monte Carlo) to the stationary distribution can in turn be quantified in terms of Wasserstein distanc

for F nonsmooth

$X^{(\ell+1)}\overset{\mathrm{def.}}{\operatorname*{=}}\mathrm{Prox}_{\tau\mathcal{F}}^{\|\cdot\|}(X^{(\ell)})\overset{\mathrm{def.}}{\operatorname*{=}}\mathrm{argmin}_{Z\in\mathcal{X}^{n}}\frac{1}{2}\left\|Z-X^{(\ell)}\right\|^{2}+\tau\mathcal{F}(Z).$

F is the convexity of the functional F with respect to the Wasserstein-2 geometry

,and is limit of the euler step,

it converge to a fixed stationary distribution as $t\rightarrow \infty$

The entropy is a typical example of geodesically convex function,

quadratic interaction functions might fail to be.

form $F(\alpha)=\int_{\mathbb{R}^d}\varphi(\rho_\alpha(x))$d$x$ on $\mathcal{X}=\mathbb{R}^d$ are geodesically convex if $\varphi$ is convex, with $\varphi(0)=0,\varphi(t)/t\to+\infty$ as $t\to+\infty$ and such that $s\mapsto s^d\varphi(s^-d)$ is convex $\operatorname{decaying}.$

# Minimum Kantorovich Estimators

$$\min_{\theta\in\Theta}\mathcal{L}(\alpha_\theta,\beta)\quad\mathrm{where}\quad\beta=\frac1n\sum_i\delta_{x_i},$$

the goal is to fit a parametric model $\theta \rightarrow \alpha_{\theta}$

$$\min_{\theta}\mathcal{L}_{\mathrm{MLE}}(\alpha_{\theta},\beta)\stackrel{\mathrm{def.}}{=}-\sum_{i}\log(\rho_{\theta}(x_{i})).$$

$$\mathcal{L}_{\mathrm{MLE}}(\alpha,\beta)\overset{n\to+\infty}{\operatorname*{\longrightarrow}}\mathrm{KL}(\alpha|\bar{\beta}).$$

However, it fails to work when estimating singular distributions, typically when the αθ does not have a density

However, it fails to work when estimating singular distributions, typically when the $\alpha_{\theta}$ does not have a density or when $x_i$ are sample from some singular $\beta$

KL should share the same support of 

a fixed reference measure $\alpha_\theta=h_{\theta,\sharp}\zeta$

The space Z is usually low-dimensional, so that the support of αθ is localized along a low-dimensional “manifold” and the resulting density is highly singular

$$\mathcal{L}(\alpha,\beta)\stackrel{\mathrm{def.}}{=}\max_{(f,g)\in\mathcal{C}(\mathcal{X})^{2}}\:\left\{\int_{\mathcal{X}}f(x)\mathrm{d}\alpha(x)+\int_{\mathcal{X}}g(x)\mathrm{d}\beta(x)\::\:(f,g)\in\mathcal{R}\right\}.$$

$$\mathcal{R}=\left\{(f,-f)\::\:f\in B\right\},$$

$$\min_{(\gamma_i)_{i=1}^n}\sum_{i=1}^n\int_{\mathcal{Z}}c(h_\theta(z),x_i)\mathrm{d}\gamma_i(z)\quad\mathrm{where}\quad\sum_{i=1}^n\gamma_i=\zeta,\quad\int_{\mathcal{Z}}\mathrm{d}\gamma_i(z)=\frac1n,$$

the use of Sinkhorn divergences for parametric model fitting is used routinely for shape matching and registration

Metric learning for supervised tasks is a classical problem