$\sup_{(f,g)}\mathcal{E}(f,g)\overset{\mathrm{def.}}{\operatorname*{=}}\int_{\mathcal{X}}f(x)\mathrm{d}\alpha(x)+\int_{\mathcal{Y}}g(y)\mathrm{d}\beta(y)+\iota_{\mathcal{R}(c)}(f,g),$

$$\forall\:y\in\mathcal{Y},\quad f^{c}(y)\stackrel{\mathrm{def.}}{=}\inf_{x\in\mathcal{X}}c(x,y)-f(x),\\\forall\:x\in\mathcal{X},\quad g^{\bar{c}}(x)\stackrel{\mathrm{def.}}{=}\inf_{y\in\mathcal{Y}}c(x,y)-g(y),$$

$f^c\in\underset{g}{\operatorname*{\operatorname*{argmax}}}\mathcal{E}(f,g)\quad\mathrm{and}\quad g^{\bar{c}}\in\underset{f}{\operatorname*{\operatorname*{argmax}}}\mathcal{E}(f,g).$

$\mathcal{X}=R^d,c(x,y)=\|x-y\|^p_2=(\sum_{i=1}^d|x_i-y_i|)^{p/2}$

then the ctransform (5.1) f c is the so-called inf-convolution between $-f$ and $\|\|^p$.

$f^c$is also often referred to as a “Hopf–Lax formula.”

then $(g^{\bar{c}},f^c)$ replace the dual potentials

and $f^c,g^{\bar{c}}$ are called c-concave and $\bar{c}$-concave

if $c(x,y)=<x,y>$,then the c convex is convex

# semidiscrete formulation

Assume $\beta=\sum_jb_j\delta_{y_j}$,$\alpha$ is continou

$\forall\mathbf{g}\in\mathbb{R}^m,\forall x\in\mathcal{X},\quad\mathbf{g}^{\bar{c}}(x)\overset{\mathrm{def.}}{\operatorname*{=}}\min_{j\in[[m]]}c(x,y_j)-\mathbf{g}_j$

$\mathcal{L}_c(\alpha,\beta)=\max_{\mathbf{g}\in\mathbb{R}^m}\mathcal{E}(\mathbf{g})\overset{\mathrm{def.}}{\operatorname*{=}}\int_{\mathcal{X}}\mathbf{g}^{\bar{c}}(x)\mathrm{d}\alpha(x)+\sum\mathbf{g}_y\mathbf{b}_j.$

Laguerre cells $\mathbb{L}_j(\mathbf{g})\overset{\mathrm{def.}}{\operatorname*{=}}\left\{x\in\mathcal{X}:\forall j^{\prime}\neq j,c(x,y_j)-\mathbf{g}_j\leq c(x,y_{j^{\prime}})-\mathbf{g}_{j^{\prime}}\right\}$

is the disjoint set $\mathcal{X}=\cup _jL_j(g)$

When g is constant, the Laguerre cells decomposition corresponds to the Voronoi diagram partition of the space.

$\mathcal{E}(\mathbf{g})=\sum_{j=1}^m\int_{\mathbb{L}_j(\mathbf{g})}\left(c(x,y_j)-\mathbf{g}_j\right)\mathrm{d}\alpha(x)+\langle\mathbf{g},\mathbf{b}\rangle.$

$\forall j\in[[m]],\quad\nabla\mathcal{E}(\mathbf{g})_j=-\int_{\mathbb{L}_j(\mathbf{g})}\mathrm{d}\alpha(x)+\mathbf{b}_j.$

 Once the optimal g is computed, then the optimal transport map $T$ from $\alpha$ to $\beta$ is mapping any $x\in\mathbb{L}_j(\mathbf{g})$ toward $y_j$, so it is piecewise constant.

for $c(x,y)=\|x-y\|^2$,the decomposition is power diagram

The most widely used algorithm relies on the fact that the power diagram of points in $\mathbb{R}^d$ is equal to the projection on$\mathbb{R}^d$of the convex hull of the set of points $(y_j,\|y_j\|^2-\mathbf{g}_j)_{j=1}^m\subset\mathbb{R}^{d+1}$

An important area of application of the semidiscrete method is for the resolution of the incompressible fluid dynamic (Euler’s equations) using Lagrangian methods

# entropic formulation

$\forall y\in\mathcal{Y},\quad f^{c,\varepsilon}(y)\overset{\mathrm{def.}}{\operatorname*{=}}-\varepsilon\log\left(\int_{\mathcal{X}}e^{\frac{-c(x,y)+f(x)}{\varepsilon}}\mathrm{d}\alpha(x)\right),\forall x\in\mathcal{X},\quad g^{\bar{c},\varepsilon}(x)\overset{\mathrm{def.}}{\operatorname*{=}}-\varepsilon\log\left(\int_{\mathcal{Y}}e^{\frac{-c(x,y)+g(y)}{\varepsilon}}\mathrm{d}\beta(y)\right).$

$\mathcal{L}_c^\varepsilon(\alpha,\beta)=\sup_{(f,g)\in\mathcal{C}(\mathcal{X})\times\mathcal{C}(\mathcal{Y})}\int_\mathcal{X}f\mathrm{d}\alpha+\int_\mathcal{Y}g\mathrm{d}\beta-\varepsilon\int_{\mathcal{X}\times\mathcal{Y}}e^{\frac{-c+f\oplus g}{\varepsilon}}\mathrm{d}\alpha\mathrm{d}\beta,$

$\forall x\in\mathcal{X},\quad\mathbf{g}^{\bar{c},\varepsilon}(x)\overset{\mathrm{def.}}{\operatorname*{=}}-\varepsilon\log\left(\sum_{j=1}^me^{\frac{-c(x,y_j)+\mathbf{g}_j}{\varepsilon}}\mathbf{b}_j\right)$

$\mathbf{f}_i^{(\ell+1)}=\mathbf{g}^{\bar{c},\varepsilon}(x_i)\quad\mathrm{and}\quad\mathbf{g}_j^{(\ell+1)}=\mathbf{f}^{c,\varepsilon}(y_j)$

$\max_{\mathbf{g}\in\mathbb{R}^n}\mathcal{E}^\varepsilon(\mathbf{g})\overset{\mathrm{def.}}{\operatorname*{=}}\int_\mathcal{X}\mathbf{g}^{\bar{c},\varepsilon}(x)\mathrm{d}\alpha(x)+\langle\mathbf{g},\mathbf{~b}\rangle.$

$\forall j\in[[m]],\quad\nabla\mathcal{E}^\varepsilon(\mathbf{g})_j=-\int_{\mathcal{X}}\chi_j^\varepsilon(x)\mathrm{d}\alpha(x)+\mathbf{b}_j$

$\chi_j^\varepsilon(x)=\frac{e^{\frac{-c(x,y_j)+\mathbf{g}_j}{\varepsilon}}}{\sum_\ell e^{\frac{-c(x,y_\ell)+\mathbf{g}_\ell}{\varepsilon}}}.$

the optimal transport can be viewd as muticlass logistirc regression problem

The intuition is that, while the conditioning of the entropic regularized problem scales like 1/ε, when ε = 0, this conditioning is rather driven by m, the number of samples of the discrete distribution

## legendre-renchel transoform

$F_\mathbf{a}(\mathbf{b})=\mathrm{L}_\mathbf{C}^\varepsilon(\mathbf{a},\mathbf{b})$

$F_\mathbf{a}^*(\mathbf{g})=-\varepsilon H(\mathbf{a})+\sum_i\mathbf{a}_i\mathbf{g}^{\bar{c},\varepsilon}(x_i).$

$G(\mathbf{a},\mathbf{b})\overset{\mathrm{def.}}{\operatorname*{=}}\mathrm{L}_{\mathbf{C}}^{\varepsilon}(\mathbf{a},\mathbf{b})$

$\forall\left(\mathbf{f},\mathbf{g}\right)\in\mathbb{R}^n\times\mathbb{R}^m,\quad G^*(\mathbf{f},\mathbf{g})=-\varepsilon\log\sum_{i,j}e^{\frac{-\mathbf{C}_{i,j}+\mathbf{f}_i+\mathbf{g}_j}{\varepsilon}}$

$\begin{aligned}\mathcal{L}_c(\alpha,\beta),\\&\forall(f,g)\in\mathcal{C}(\mathcal{X})\times\mathcal{C}(\mathcal{Y}),\quad\mathcal{G}^*(f,g)=\inf_{(x,y)\in\mathcal{X}\times\mathcal{Y}}c(x,y)-f(x)-g(y).\end{aligned}$

# stochatis optimization

$\mathcal{E}^{\varepsilon}(\mathbf{g})=\int_{\mathcal{X}}E^{\varepsilon}(\mathbf{g},x)\mathrm{d}\alpha(x)=\mathbb{E}_{X}(E^{\varepsilon}(\mathbf{g},X))\mathrm{where}\quad E^{\varepsilon}(\mathbf{g},x)\overset{\mathrm{def.}}{\operatorname*{=}}\mathbf{g}^{\bar{c},\varepsilon}(x)-\langle\mathbf{g},\mathbf{b}\rangle,$

$\nabla_\mathbf{g}E^\varepsilon(x,\mathbf{g})=(\chi_j^\varepsilon(x)-\mathbf{b}_j)_{j=1}^m\in\mathbb{R}^m.$

$\tau_\ell\overset{\mathrm{def.}}{\operatorname*{\operatorname*{=}}}\frac{\tau_0}{1+\ell/\ell_0},$

$l_0$ use for warm start

$\mathcal{E}^\varepsilon(\mathbf{g}^\star)-\mathbb{E}(\mathcal{E}^\varepsilon(\mathbf{g}^{(\ell)}))=O\left(\frac{1}{\sqrt{\ell}}\right),$