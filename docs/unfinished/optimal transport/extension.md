# Multimarginal Problems

$$\min_{\mathbf{P}\in\mathbf{U}(\mathbf{a}_s)_s}\left\langle\mathbf{C},\mathbf{P}\right\rangle\overset{\mathrm{def.}}{\operatorname*{=}}\sum_s\sum_{i_s=1}^{n_s}\mathbf{C}_{i_1,...,i_S}\mathbf{P}_{i_1,...,i_S},$$

$$\mathbf{U}(\mathbf{a}_s)_s=\left\{\mathbf{P}\in\mathbb{R}^{n_1\times...\times n_S}\::\:\forall\:s,\forall\:i_s,\sum_{\ell\neq s}\sum_{i_\ell=1}^{n_\ell}\mathbf{P}_{i_1,...,i_S}=\mathbf{a}_{s,i_s}\right\}.$$

entropy regularzation

$$\min_{\mathbf{P}\in\mathbf{U}(\mathbf{a}_s)_s}\langle\mathbf{P},\mathbf{C}\rangle-\varepsilon\mathbf{H}(\mathbf{P})$$

$\mathbf{P}_i=\mathbf{K}_i\prod_{s=1}^S\mathbf{u}_{s,i_s}\quad\mathrm{where}\quad\mathbf{K}\overset{\mathrm{def.}}{\operatorname*{=}}e^{-\frac{\mathbf{C}}{\varepsilon}},$

$$\mathbf{u}_{s,i_s}\leftarrow\frac{\mathbf{a}_{s,i_s}}{\sum_{\ell\neq s}\sum_{i_\ell=1}^{n_\ell}\mathbf{K}_i\prod_{r\neq s}\mathbf{u}_{\ell,i_r}}$$

## general measure

$\min_{\pi\in\mathcal{U}(\alpha_s)_s}\int_{\mathcal{X}_1\times...\times\mathcal{X}_S}c(x_1,\ldots,x_S)\mathrm{d}\pi(x_1,\ldots,x_S)$

$\mathcal{U}(\alpha_s)_s\overset{\mathrm{def.}}{\operatorname*{=}}\left\{\pi\in\mathcal{M}_+^1(\mathcal{X}_1\times\ldots\times\mathcal{X}_S):\forall s=1,\ldots,S,P_{s,\sharp}\pi=\alpha_s,\right\}$

## barycenter

$$\min_{\bar{\pi}\in\mathcal{M}_+^1(X^{S+1})}\:\int_{\mathcal{X}^{S+1}}\sum_{s=1}^S\lambda_sc(x,x_s)\mathrm{d}\bar{\pi}(x_1,\ldots,x_s,x)$$

subject to $\forall s= 1, \ldots , S$, $P_{s, \sharp }\bar{\pi } = \alpha _s.$

# unbalanced ot

$$\begin{aligned}\mathcal{L}_{\mathbf{C}}^{\tau}(\mathbf{a},\mathbf{b})&=\min_{\tilde{\mathbf{a}},\tilde{\mathbf{b}}}\mathcal{L}_{\mathbf{C}}(\mathbf{a},\mathbf{b})+\tau_{1}\mathbf{D}_{\varphi}(\mathbf{a},\tilde{\mathbf{a}})+\tau_{2}\mathbf{D}_{\varphi}(\mathbf{b},\tilde{\mathbf{b}})\\&=\min_{\mathbf{P}\in\mathbb{R}_{+}^{n\times m}}\langle\mathbf{C},\mathbf{P}\rangle+\tau_{1}\mathbf{D}_{\varphi}(\mathbf{P}\mathbb{1}_{m}|\mathbf{a})+\tau_{2}\mathbf{D}_{\varphi}(\mathbf{P}^{\top}\mathbb{1}_{m}|\mathbf{b}),\end{aligned}$$

$$\mathcal{L}_\mathbf{C}^\tau(\mathbf{a},\mathbf{b})\xrightarrow{\tau\to0}\mathfrak{h}^2(\mathbf{a},\mathbf{b})=\sum_i(\sqrt{\mathbf{a}_i}-\sqrt{\mathbf{b}_i})^2$$

$$\mathbf{u}\leftarrow\left(\frac{\mathbf{a}}{\mathbf{K}\mathbf{v}}\right)^{\frac{\tau_1}{\tau_1+\varepsilon}}\quad\mathrm{and}\quad\mathbf{v}\leftarrow\left(\frac{\mathbf{b}}{\mathbf{K}^\mathrm{T}\mathbf{u}}\right)^{\frac{\tau_2}{\tau_2+\varepsilon}}.$$

## wasserstein fisher rao

$c(x,y)=-\log\cos(\min(d(x,y)/\kappa,\pi/2)),$

 $\mathcal{D}_\varphi=$KL
$$\mathrm{WFR}(\alpha,\beta)\stackrel{\mathrm{def.}}{=}\mathcal{L}_c^\tau(\alpha,\beta)^{\frac12}$$

outperform classical OT for applications (such as in imaging or machine learning) where the input data is noisy or not perfectly known.

# extra constraint

$$\min_{\pi\in\mathcal{U}(\alpha,\beta)}\:\left\{\int_{\mathcal{X}\times\mathcal{Y}}c(x,y)\mathrm{d}\pi(x,y)\::\:\pi\in\mathcal{C}\right\}$$

martingale constraint

$$\mathcal{C}=\left\{\pi\::\:\forall\:x\in\mathbb{R}^d,\int_{\mathbb{R}^d}y\frac{\mathrm{d}\pi(x,y)}{\mathrm{d}\alpha(x)\mathrm{d}\beta(y)}\mathrm{d}\beta(y)=x\right\}.$$

use generalize sinkhorn, the method can be solved

# sliced w distnace

$$\mathrm{SW}(\alpha,\beta)^2\overset{\mathrm{def.}}{\operatorname*{=}}\int_{\mathbf{S}^d}\mathcal{W}_2(P_{\theta,\sharp}\alpha,P_{\theta,\sharp}\beta)^2\mathrm{d}\theta,$$

 $\mathbf{S}^d=\{\theta\in\mathbb{R}^d:\|\theta\|=1\}$ is the $d$-dimensional sphere, and $P_\theta:x\in\mathbb{R}^d\to\mathbb{R}$ is the projection.

Project measure onto the sphere

# randon trasnform

$$\mathcal{R}(\alpha)\stackrel{\mathrm{def.}}{=}\left(P_{\theta,\sharp}\alpha\right)_{\theta\in\mathbf{S}^d}.$$

$$\mathcal{R}^+(\rho)=C_d\Delta^{\frac{d-1}2}\mathcal{B}(\rho),$$

and $\xi=\mathcal{B}(\rho)$is defined through

$$\forall\:g\in\mathcal{C}(\mathbb{R}^d),\quad\int_{\mathbb{R}^d}g(x)\mathrm{d}\xi(x)=\int_{\mathbf{S}^d}\int_{\mathbb{R}^{d-1}}\int_{\mathbb{R}}g(r\theta+U_\theta z)\mathrm{d}\rho_\theta(r)\mathrm{d}z\mathrm{d}\theta,$$

## Sliced Wasserstein kernels.

$1\leq p \leq 2$,$$k(\alpha,\beta)=e^{-\frac{\mathrm{SW}(\alpha,\beta)^p}{2\sigma^p}}$$

$0<p<2$$\quad\mathrm{and}\quad k(\alpha,\beta)=-\mathrm{SW}(\alpha,\beta)^p$

extend KL on matrix

$$\mathbf{KL}(A|B)\stackrel{\mathrm{def.}}{=}\mathrm{tr}\left(P\log(P)-P\log(Q)-P+Q,\right)$$

# hausdorff

$$\mathcal{H}_{\mathcal{Z}}(A,B)\stackrel{\mathrm{def.}}{=}\max\left(\sup_{a\in A}\inf_{b\in B}d_{\mathcal{Z}}(a,b),\sup_{b\in B}\inf_{a\in A}d_{\mathcal{Z}}(a,b)\right)$$

$$\mathcal{R}(A,B)\stackrel{\mathrm{def.}}{=}\left\{R\in\mathcal{X}\times\mathcal{Y}:\begin{array}{c}\forall a\in A,\exists b\in B,(a,b)\in R\\\forall b\in B,\exists a\in A,(a,b)\in R\end{array}\right\}.$$

$$\mathcal{H}_{\mathcal{Z}}(A,B)=\inf_{R\in\mathcal{R}(A,B)}\sup_{(a,b)\in R}d(a,b).$$

# Gromov hausdorff

by quantifying how far they are from being isometric to each other,

$$\left.\mathcal{GH}(d_{\mathcal{X}},d_{\mathcal{Y}})\stackrel{\mathrm{def.}}{=}\inf_{\mathcal{Z},f,g}\left\{\mathcal{H}_{\mathcal{Z}}(f(\mathcal{X}),g(\mathcal{Y}))\right.:\begin{array}{c}f:\mathcal{X}\stackrel{\mathrm{isom}}{\longrightarrow}\mathcal{Z}\\g:\mathcal{Y}\stackrel{\mathrm{isom}}{\longrightarrow}\mathcal{Z}\end{array}\right\}.$$

## gromov wassertein distance

$$\mathrm{GW}((\mathbf{a},\mathbf{D}),(\mathbf{b},\mathbf{D}^{\prime}))^2\stackrel{\mathrm{def.}}{=}\min_{\mathbf{P}\in\mathbf{U}(\mathbf{a},\mathbf{b})}\mathcal{E}_{\mathbf{D},\mathbf{D}^{\prime}}(\mathbf{P})$$

$$\mathrm{where}\quad\mathcal{E}_{\mathbf{D},\mathbf{D}'}(\mathbf{P})\stackrel{\mathrm{def.}}{=}\sum_{i,j,i',j'}|\mathbf{D}_{i,i'}-\mathbf{D}_{j,j'}^{\prime}|^2\mathbf{P}_{i,j}\mathbf{P}_{i',j'},$$

One can show that GW satisfies the triangular inequality, and in fact it defines a distance between metric spaces equipped with a probability distribution, here assumed to be discrete in definition