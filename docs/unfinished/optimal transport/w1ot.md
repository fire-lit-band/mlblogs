optimal transport with a linear ground distance is usually more robust to outliers and noise than a quadratic cost.

$\mathrm{Lip}(f)\overset{\mathrm{def.}}{\operatorname*{=}}\sup\left\{\frac{|f(x)-f(y)|}{d(x,y)}:(x,y)\in\mathcal{X}^{2},x\neq y\right\}.$

## proposition

for $\mathcal{X}=\mathcal{Y}$,c(x,y)=d(x,y),then there exist g s.t. $f=g^c$ iff $Lip(f)\leq 1$.If $Lip(f)\leq 1$,then $f^c=-f$

proof:

$\begin{gathered}|f(x)-f(y)|=\begin{vmatrix}\inf_{z\in\mathcal{X}}d(x,z)-g(z)&-&\inf_{z\in\mathcal{X}}d(y,z)-g(z)\end{vmatrix}\\\leq\sup_{z\in\mathcal{X}}|d(x,z)-d(y,z)|\leq d(x,y).\end{gathered}$

for $Lip(f)\leq 1$,define $g=-f$

$f(y)-d(x,y)\leq f(x)\leq f(y)+d(x,y).$

$g^c(y)=\inf_{x\in\mathcal{X}}\left[d(x,y)+f(x)\right]\geq\inf_{x\in\mathcal{X}}\left[d(x,y)+f(y)-d(x,y)\right]=f(y),g^c(y)=\inf_{x\in\mathcal{X}}\left[d(x,y)+f(x)\right]\leq\inf_{x\in\mathcal{X}}\left[d(x,y)+f(y)+d(x,y)\right]=f(y).$

$\mathcal{W}_1(\alpha,\beta)=\max_f\left\{\int_\mathcal{X}f(x)(\mathrm{d}\alpha(x)-\mathrm{d}\beta(x)):\mathrm{Lip}(f)\leq1\right\}$

$\mathcal{W}_{1}(\alpha,\beta)=\max_{f}\left\{\int_{\mathbb{R}^{d}}f(x)(\mathrm{d}\alpha(x)-\mathrm{d}\beta(x)):\left\|\nabla f\right\|_{\infty}\leq1\right\}.$

and $w1$ is actually a norm

for $\alpha-\beta=\sum_k\mathbf{m}_k\delta_{z_k}$

$\sum_k\mathbf{m}_k=0$

$\mathcal{W}_1(\alpha,\beta)=\max_{(\mathbf{f}_k)_k}\left\{\sum_k\mathbf{f}_k\mathbf{m}_k:\forall(k,\ell),|\mathbf{f}_k-\mathbf{f}_\ell|\leq d(z_k,z_\ell),\right\}$

Beckmann formulation$\mathcal{W}_1(\alpha,\beta)=\min_s\left\{\int_{\mathbb{R}^d}\left\|s(x)\right\|_2\mathrm{d}x:\mathrm{div}(s)=\alpha-\beta\right\},$

Outside the support of the two input measures, div(s) = 0, which is the conservation of mass constraint. Once properly discretized using finite elements, Problems (6.3) and (6.4) become nonsmooth convex optimization problems.

a constraint on wavelet coefficients leading to an explicit formula

# $W_p$

$\tilde{d}(x,y)\overset{\mathrm{def.}}{\operatorname*{\operatorname*{=}}}d(x,y)^p$

$\mathrm{Lip}_p(f)\overset{\mathrm{def.}}{\operatorname*{=}}\sup\left\{\frac{|f(x)-f(y)|}{d(x,y)^p}:(x,y)\in\mathcal{X}^2,x\neq y\right\}.$

$\{f:\mathrm{Lip}_p(f)\leq1\}$

# graph

$\forall (i, j) \in \mathcal{E}, \quad (\nabla \mathbf{f})_{i,j} \overset{\mathrm{def.}}{=} \mathbf{f}_i - \mathbf{f}_j.
$
$$
\mathbf{D}_{i,j} \overset{\mathrm{def.}}{=} \min_{K \ge 0, (i_k)_k: i \to j} \left\{ \sum_{k=1}^{K-1} \mathbf{w}_{i_k, i_{k+1}} : \forall k \in [\![1, K-1]\!], (i_k, i_{k+1}) \in \mathcal{E} \right\},
$$

$$
W_1(\mathbf{a}, \mathbf{b}) = \max_{\mathbf{f} \in \mathbb{R}^n} \left\{ \sum_{i=1}^n \mathbf{f}_i(\mathbf{a}_i - \mathbf{b}_i) : \forall(i,j) \in \mathcal{E}, |(\nabla \mathbf{f})_{i,j}| \le \mathbf{w}_{i,j} \right\}.
$$

$$
\forall i \in [\![1, n]\!], \quad \mathrm{div}(\mathbf{s})_i \overset{\mathrm{def.}}{=} \sum_{j:(i,j) \in \mathcal{E}} (\mathbf{s}_{i,j} - \mathbf{s}_{j,i}) \in \mathbb{R}^n.
$$

$$
W_1(\mathbf{a}, \mathbf{b}) = \min_{\mathbf{s} \in \mathbb{R}_+^{\mathcal{E}}} \left\{ \sum_{(i,j) \in \mathcal{E}} \mathbf{w}_{i,j} \mathbf{s}_{i,j} : \mathrm{div}(\mathbf{s}) = \mathbf{a} - \mathbf{b} \right\}.
$$

$J_t\overset{\mathrm{def.}}{\operatorname*{\operatorname*{=}}}\alpha_tv_t,$

$\mathcal{W}_2^2(\alpha_0,\alpha_1)=\min_{(\alpha_t,J_t)_t\in\mathcal{C}(\alpha_0,\alpha_1)}\int_0^1\int_{\mathbb{R}^d}\theta(\alpha_t(x),J_t(x))\mathrm{d}x\mathrm{d}t,$

$\bar{\mathcal{C}}(\alpha_0,\alpha_1)\overset{\mathrm{def.}}{\operatorname*{=}}\left\{(\alpha_t,J_t,s_t):\frac{\partial\alpha_t}{\partial t}+\mathrm{div}(J_t)=s_t,\alpha_{t=0}=\alpha_0,\alpha_{t=1}=\alpha_1\right\}.$