divergence:$D(\alpha,\beta)>0$and $D(\alpha,\alpha)=0$ iff $\alpha=\beta$

and it does not need symmetric and traiangular inequialtiy

# entropic function

1. lower semicontinous,convex
2. dom$\varphi \subset [0,\infty]$ and $dom \varphi \cap [0,\infty]\neq \emptyset$

the speed of grwoth at $\infty$ is defined as

$\varphi_\infty^{\prime}=\lim_{x\to+\infty}\varphi(x)/x\in\mathbb{R}\cup\{\infty\}$

if $\varphi_{\infty}=\infty$,then $\varphi$ grows faster than lienar function and called suplinear

## $\varphi$ divergence

$\varphi$ is entropy function

$\frac{d\alpha}{d\beta}+\alpha^{\perp}$ is Lbebsegue decomposition,then divergence $D_\varphi$ is defined as 

$\mathcal{D}_{\varphi}(\alpha|\beta)\overset{\mathrm{def.}}{\operatorname*{=}}\int_{\mathcal{X}}\varphi\left(\frac{\mathrm{d}\alpha}{\mathrm{d}\beta}\right)\mathrm{d}\beta+\varphi_{\infty}^{\prime}\alpha^{\perp}(\mathcal{X})$

The Lebesgue decomposition theorem asserts that, given $\beta$, $\alpha$ admits a unique decomposition as the sum of two measures$\alpha^s+\alpha^\perp$ such that $\alpha^s$ is absolutely continuous with respect to $\beta$and $\alpha^\perp$ and $\beta$ are singular.

for discreate setting

$\mathbf{D}_\varphi(\mathbf{a}|\mathbf{b})=\sum_{i\in\mathrm{Supp}(\mathbf{b})}\varphi\left(\frac{\mathbf{a}_i}{\mathbf{b}_i}\right)\mathbf{b}_i+\varphi_\infty^{\prime}\sum_{i\notin\mathrm{Supp}(\mathbf{b})}\mathbf{a}_i,$

if $\varphi$ is entorpy function, then $D_\varphi$ is jointyly 1-homogenous, convex and weakly lower semicontinous

$\varphi^*(s)\overset{\mathrm{def.}}{\operatorname*{=}}\sup_{t\in\mathbb{R}}st-\varphi(t)$

$\mathcal{D}_{\varphi}(\alpha|\beta)=\sup_{f:\mathcal{X}\to\mathbb{R}}\int_{\mathcal{X}}f(x)\mathrm{d}\alpha(x)-\int_{\mathcal{X}}\varphi^{*}(f(x))\mathrm{d}\beta(x);$

$\varphi_{\mathrm{KL}}(s)=\begin{cases}s\log(s)-s+1&\mathrm{for}s>0,\\1&\mathrm{for}s=0,\\+\infty&\text{otherwise.}&\end{cases}$

$\mathbf{B}_\psi(\mathbf{a}|\mathbf{b})\overset{\mathrm{def.}}{\operatorname*{=}}\psi(\mathbf{a})-\psi(\mathbf{b})-\langle\nabla\psi(\mathbf{b}),\mathbf{a}-\mathbf{b}\rangle,$

Bregman divergence

it is a convex function for a, and a linear function of $\varphi$

,$\mathbf{B_\psi(a|b)}\geq0\mathrm{~and~}\mathbf{B_\psi(a|b)}=0\text{ if and only if }\mathbf{a}=\mathbf{b}.$

$KL=B_{-H}$

$\mathbf{B}_\psi(\mathbf{a}+\varepsilon|\mathbf{a}+\eta)=\langle\partial^2\psi(\mathbf{a})(\varepsilon-\eta),\varepsilon-\eta\rangle+o(\|\varepsilon-\eta\|^2)$

the set of $\{\mathbf{a}:\mathbf{B}_\psi(\mathbf{a}|\mathbf{b})=\mathbf{B}_\psi(\mathbf{a}|\mathbf{b}^{\prime})\}$ is a hyperplane between b,b'

$\mathrm{KL}(\alpha|\beta)=\frac{1}{2}\left(\frac{\sigma_\alpha^2}{\sigma_\beta^2}+\log\left(\frac{\sigma_\beta^2}{\sigma_\alpha^2}\right)+\frac{|m_\alpha-m_\beta|}{\sigma_\beta^2}-1\right)$

In that sense, one can say that singular Gaussians are infinitely far from all other Gaussians in the KL geometry.

$\mathrm{KL}(\mathcal{N}(m+\delta_m,(\sigma+\delta_\sigma)^2)|\mathcal{N}(m,\sigma^2))=\frac{1}{\sigma^2}\left(\frac{1}{2}\delta_m^2+\delta_\sigma^2\right)+o(\delta_m^2,\delta_\sigma^2).$

The local Riemannian metric so called Fisher metric

they only reach the limit σ = 0 after an infinite time.

if $\sigma_\alpha=\sigma_\beta$,then geodesic between two measure does not have constant deviation

$\mathcal{W}_2^2(\alpha,\beta)=|m_\alpha-m_\beta|^2+|\sigma_\alpha-\sigma_\beta|^2.$

## TV

$\varphi_{\mathrm{TV}}(s)=\begin{cases}|s-1|&\mathrm{for~}s\geq0,\\+\infty&\text{otherwise.}&\end{cases}$

$TV=D_{\varphi_{TV}}$

$\mathrm{TV}(\alpha|\beta)=\|\alpha-\beta\|_{\mathrm{TV}},\quad\mathrm{where}\quad\|\alpha\|_{\mathrm{TV}}=|\alpha|(\mathcal{X})=\int_{\mathcal{X}}\mathrm{d}|\alpha|(x).$

if $\alpha$ has a density $\rho_\alpha$

On a compact domain of Radius R, strong topology

$\mathcal{W}_1(\alpha,\beta)\leq R\|\alpha-\beta\|_{\mathrm{TV}}$

A chief advantage is that $\mathcal{M}_+(\mathcal{X})$ (once again on a compact ground space X ) is compact for the weak topology, so that from any sequence of probability measures (αk)k, one can always extract a converging subsequence, which makes it a suitable space for several optimization problems,

Hellinger

$\mathfrak{h}\overset{\mathrm{def.}}{\operatorname*{=}}\mathcal{D}_{\varphi_H}^{1/2}$

$\varphi_H(s)=\begin{cases}|\sqrt{s}-1|^2&\mathrm{for~}s\geq0,\\+\infty&\text{otherwise.}&\end{cases}$

$\mathfrak{h}(\alpha,\beta)=\|\sqrt{\rho_\alpha}-\sqrt{\rho_\beta}\|_{L^2}$

a distance on M+(X ), which metrizes the strong topology

$\mathrm{JS}(\alpha,\beta)^2\overset{\mathrm{def.}}{\operatorname*{\operatorname*{=}}}\frac{1}{2}\left(\mathrm{KL}(\alpha|\xi)+\mathrm{KL}(\beta|\xi)\right)\quad\mathrm{where}\quad\xi=\frac{\alpha+\beta}{2},$

$\varphi(s)=t\log(t)-(t+1)\log(t+1)$

JS is always bounded, and metric strong convergence(strong topology)

$\mathrm{s}0\leq\mathrm{JS}(\alpha,\beta)^{2}\leq\ln(2)$

$\varphi_{\chi^2}(s)=\begin{cases}|s-1|^2&\mathrm{for}s\geq0,\\+\infty&\text{otherwise.}&\end{cases}$

$\mathrm{The~}\chi^2\text{-divergence }\chi^2\overset{\mathrm{def.}}{\operatorname*{=}}\mathcal{D}_{\varphi_{\chi^2}}$

$\chi^2(\alpha|\beta)=\sum_i\frac{(\mathbf{a}_i-\mathbf{b}_i)^2}{\mathbf{b}_i}.$

# integral probability metric

$\left\|\alpha\right\|_{B}\overset{\mathrm{def.}}{\operatorname*{=}}\max_{f}\left\{\int_{\mathcal{X}}f(x)\mathrm{d}\alpha(x):f\in B\right\}.$

total variation:

$B=\left\{f\in\mathcal{C}(\mathcal{X}):\left\|f\right\|_\infty\leq1\right\}.$

By using smaller “balls” B, which typically only contain continuous (and sometimes regular) functions, one defines weaker dual norms. In order for ‖·‖B to metrize the weak convergence ,it is sufficient for the space spanned by B to be dense in the set of continuous functions for the sup-norm ‖·‖∞ 

不能让B，bounded，否则会使得 $\int_{\mathcal{X}}d\alpha=0$

$\mathcal{W}_1$ norm  $B=\{f:\mathrm{Lip}(f)\leq1\}$

the flat norm $B=\{f:\left\|\nabla f\right\|_{\infty}\leq1\quad\mathrm{and}\quad\left\|f\right\|_{\infty}\leq1\}.$ s the weak convergence on the whole space

The flat norm is sometimes called the “Kantorovich–Rubinstein” norm

Dudley metric $B=\left\{f:\left\|\nabla f\right\|_\infty+\left\|f\right\|_\infty\leq1\right\}.$

# RKHS

Definition 8.3. A symmetric function $k$ (resp., $\varphi)$ defined on a set $\mathcal{X}\times\mathcal{X}$ is said to be positive (resp., negative) definite if for any $n\geq0$, family $x_1,\ldots,x_n\in\mathcal{Z}$, and vector $r\in\mathbb{R}^n$ the following inequality holds:

(8.12)

$$\sum_{i,j=1}^nr_ir_jk(x_i,x_j)\geq0,\quad\left(\text{resp.}\quad\sum_{i,j=1}^nr_ir_j\varphi(x_i,x_j)\leq0\right).$$

be conditionally positive if positivity only holds in (8.12) for zero mean vectors r (i.e. such that 〈r, 1n〉 = 0).

for k is conditionally positive 

$\|\alpha\|_k^2\overset{\mathrm{def.}}{\operatorname*{=}}\int_{\mathcal{X}\times\mathcal{X}}k(x,y)\mathrm{d}\alpha(x)\mathrm{d}\alpha(y).=\mathbb{E}_{X,X^{\prime}}(k(X,X^{\prime})).$

“maximum mean discrepancy” (MMD)

One can show that $\|\|_k^2$ is the dual norm in the sense of (8.10) associated to the unit ball B of the RKHS associated to k.

the weak convergence

For translation-invariant kernels over X = Rd, $k(x,y)=k_0(x-y)$, this is equivalent to having a nonvanishing Fourier transform

for discreate

$\|\alpha\|_k^2=\sum_{i=1}^n\sum_{i^{\prime}=1}^n\mathbf{a}_i\mathbf{a}_{i^{\prime}}\mathbf{k}_{i,i^{\prime}}=\langle\mathbf{k}\mathbf{a},\mathbf{a}\rangle\quad\mathrm{where}\quad\mathbf{k}_{i,i^{\prime}}\overset{\mathrm{def.}}{\operatorname*{=}}k(x_i,x_{i^{\prime}}).$

guassian kernel $k(x,y)=e^{-\frac{\|x-y\|^2}{2\sigma^2}}$

If the measures have multiscale features (some regions may be very dense, others very sparsely populated), a Gaussian kernel is thus not well adapted, and one should consider a “scale-free” kernel as we detail next. An issue with such scale-free kernels is that they are globa

$H^{-1}(R^d)$ dual norm

the dual of Sobolev space 

it is defined using the primal RKHS norm $\|\nabla f\|^2_L$

$\|\alpha-\beta\|_{H^{-1}(\mathbb{R}^d)}^2=\min_s\left\{\int_{\mathbb{R}^d}\|s(x)\|_2^2\mathrm{d}x:\mathrm{div}(s)=\alpha-\beta\right\}$

the weighted version of Sobolev dual norm

$\left\|\rho\right\|_{H^{-1}(\alpha)}^2=\min_{\mathrm{div}(s)=\rho}\int_{\mathbb{R}^d}\left\|s(x)\right\|_2^2\mathrm{d}\alpha(x),$ is not a norm

if $\alpha,\beta$ have density on the same support bounded (a,b)

$b^{-1/2}\left\|\alpha-\beta\right\|_{H^{-1}(\mathbb{R}^{d})}\leq W_{2}(\alpha,\beta)\leq a^{-1/2}\left\|\alpha-\beta\right\|_{H^{-1}(\mathbb{R}^{d})};$

$H^{-r}(R^d)$ is the dual of the functional Sobolev space $H^r(R^d)$ of functions having r derivatives

$\|\alpha\|_{H^{-r}(\mathbb{R}^d)}^2\overset{\mathrm{def.}}{\operatorname*{=}}\int_{\mathbb{R}^d}\|\omega\|^{-2r}|\hat{\alpha}(\omega)|^2\mathrm{d}\omega.$

$\forall x\in\mathbb{R}^d,\quad k_0(x)=\left\{\begin{array}{ll}\frac{1}{\|x\|^{d-2r}}\quad\mathrm{if}\quad r<d/2,\\-\|x\|^{2r-d}\quad\mathrm{if}\quad r>d/2.\end{array}\right.$

The energy distance$\left\|\alpha-\beta\right\|_{\mathrm{ED}(\mathcal{X},d^p)}\overset{\mathrm{def.}}{\operatorname*{=}}\left\|\alpha-\beta\right\|_{k_{\mathrm{ED}}}\quad\mathrm{where}\quad k_{\mathrm{ED}}(x,y)=-d(x,y)^p$

$\left\|\cdot\right\|_{\mathrm{ED}(\mathbb{R}^d,\|\cdot\|^p)}=\left\|\cdot\right\|_{H^{-\frac{d+p}{2}}(\mathbb{R}^d)}.$

$\left\|f_{s\sharp}(\alpha-\beta)\right\|_{\mathrm{ED}(\mathbb{R}^d,\|\cdot\|^p)}=s^{\frac{p}{2}}\left\|\alpha-\beta\right\|_{\mathrm{ED}(\mathbb{R}^d,\|\cdot\|^p)}$

$f_s(x)=sx$

$\mathcal{W}_p(f_{s\sharp}\alpha,f_{s\sharp}\beta))=s\mathcal{W}_p(\alpha,\beta))$

$\|\alpha-\beta\|_{\mathrm{ED}(\mathbb{R}^d,\|\cdot\|^2)}=\left\|\int_{\mathbb{R}^d}x(\mathrm{d}\alpha(x)-\mathrm{d}\beta(x))\right\|$

$\left\|\alpha-\beta\right\|_{\mathrm{ED}(\mathbb{R}^d,\left\|\cdot\right\|^2)}=\left\|\int_{\mathbb{R}^d}x(\mathrm{d}\alpha(x)-\mathrm{d}\beta(x))\right\|$

# hilbertian

Definition 8.4. A distance $d$ defined on a set $z\times z$ is said to be Hilbertian if there exists a Hilbert space $\mathcal{H}$ and a mapping $\phi:\mathcal{Z}\to\mathcal{H}$ such that for any pair $z,z^\prime$ in $\mathcal{Z}$ we have that $d(z,z^\prime)=\|\phi(z)-\phi(z^{\prime})\|_{\mathcal{H}}.$

(1)$e^{-d^p/t}$ is positive definite kernel

mbedded in lower dimensions with low distortion factor

Wasserstein distance do not retain its Hilbertian nature in higher dimensional

A distance d is Hilbertian if and only if $d^2$ is negative definite.

$\|x-y\|_2$,then p=1,2,p-wassertein distance is not Hilbertian,$d\geq 2$

把w2 embedding到l2 space，会造成严重的扭曲distortion

embed quasi-isometrically p-Wasserstein spaces for l1,but the equivalence constant between the distances grows fast with the dimension d. Note also that for p = 1 the embedding is true only for discrete measures

Note also that for p = 1 the embedding is true only for discrete measures

l over the wavelets coefficients

this embedding can be computed approximately in linear time when the input measures are discretized on uniform grids.

Negative/Positive Definite Variants of Optimal Transport

# Empirical Estimators for OT

sample $(x_i)$ from $\alpha$,and sample $y_j$ from $\beta$

$\left.D(\alpha,\beta)\approx D(\hat{\alpha}_n,\hat{\beta}_m)\quad\mathrm{where}\quad\left\{\begin{array}{l}\hat{\alpha}_n\overset{\mathrm{def.}}{\operatorname*{=}}\frac{1}{n}\sum_i\delta_{x_i},\\\hat{\beta}_m\overset{\mathrm{def.}}{\operatorname*{=}}\frac{1}{m}\sum_j\delta_{y_j}.\end{array}\right.\right.$

Assume $\mathcal{X}$ is compact

$\mathbb{E}(|\mathcal{W}_p(\hat{\alpha}_n,\hat{\beta}_n)-\mathcal{W}_p(\alpha,\beta)|)=O(n^{-\frac{1}{d}}),$

This rate can be refined when the measures are supported on low-dimensional subdomains: Weed and Bach [2017] show that, indeed, the rate depends on the intrinsic dimensionality of the support.

MMD

and contrary to Wasserstein distances, the sample complexity does not depend on the ambient dimension

$\mathbb{E}(\|\hat{\alpha}_n-\hat{\beta}_n\|_k-\|\alpha-\beta\|_k|)=O(n^{-\frac{1}{2}})$

$\mathrm{MMD}_{k}(\hat{\alpha}_{n},\hat{\beta}_{n})^{2}\overset{\mathrm{def.}}{\operatorname*{=}}\frac{1}{n(n-1)}\sum_{i,i^{\prime}}k(x_{i},x_{i^{\prime}})+\frac{1}{n(n-1)}\sum_{j,j^{\prime}}k(y_{j},y_{j^{\prime}})-2\frac{1}{n^2}\sum_{i,j}k(x_i,y_j),$

# empirical estimator for $\varphi$

Instead, it is required to use a density estimator to somehow smooth the discrete empirical measures and replace them by densities;

$h_{\sigma}=h(\cdot/\sigma)$

$\hat{\alpha}_n\star h_\sigma=\frac{1}{n}\sum_ih_\sigma(\cdot-x_i)$

$\mathcal{D}_\varphi^\sigma(\hat{\alpha}_n|\hat{\beta}_n)\overset{\mathrm{def.}}{\operatorname*{=}}\frac{1}{n}\sum_{j=1}^n\varphi\left(\frac{\sum_ih_\sigma(y_j-x_i)}{\sum_{j^{\prime}}h_\sigma(y_j-y_{j^{\prime}}),}\right)$

It is also possible to devise nonparametric estimators, bypassing the choice of a fixed bandwidth σ to select instead a number k of nearest neighbors. These methods typically make use of the distance between nearest neighbors

which is similar to locally adapting the bandwidth σ to the local sampling density.

$\Delta_k(x)$ the distance between $x\in\mathbb{R}^d$ and its $k$th nearest neighbor among the $(x_i)_i=1^n$, a density estimator is defined as

$$\rho_{\hat{\alpha}_n}^k(x)\stackrel{\mathrm{def.}}{=}\frac{k/n}{|B_d|\Delta_k(x)^r},$$

where $|B_d|$ is the volume of the unit ball in $\mathbb{R}^d.$ 

## Entropic Regularization: Between OT and MMD

$\tilde{\mathcal{W}}_{p,\varepsilon}(\alpha,\beta)^p\overset{\mathrm{def.}}{\operatorname*{=}}2\mathcal{W}_{p,\varepsilon}(\alpha,\beta)^p-\mathcal{W}_{p,\varepsilon}(\alpha,\alpha)^p-\mathcal{W}_{p,\varepsilon}(\beta,\beta)^p.$

$\tilde{\mathcal{W}}_{p,\varepsilon}(\alpha,\beta)\overset{\varepsilon\to0}{\operatorname*{\longrightarrow}}2\mathcal{W}_{p}(\alpha,\beta)\quad\mathrm{and}\quad\tilde{\mathcal{W}}_{p,\varepsilon}(\alpha,\beta)^{p}\overset{\varepsilon\to+\infty}{\operatorname*{\longrightarrow}}\left\|\alpha-\beta\right\|_{\mathrm{ED}(\mathcal{X},d)}^{2},$

It is proved in Genevay et al. [2019], in the case of c(x, y) = ‖x − y‖2 on X = Rd, that these rates interpolate between the ones of OT and MMD