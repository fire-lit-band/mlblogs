$$
\frac{\partial \alpha_t}{\partial t} + \mathrm{div}(\alpha_t v_t) = 0 \quad \text{and} \quad \alpha_{t=0} = \alpha_0, \alpha_{t=1} = \alpha_1,
$$

$\|v_t\|_{L^2(\alpha_t)}=\left(\int_{\mathbb{R}^d}\|v_t(x)\|^2\mathrm{d}\alpha_t(x)\right)^{1/2}$

$\mathcal{W}_2^2(\alpha_0,\alpha_1)=\min_{(\alpha_t,v_t)_t\mathrm{~sat.~}(7.1)}\int_0^1\int_{\mathbb{R}^d}\|v_t(x)\|^2\mathrm{d}\alpha_t(x)\mathrm{d}t$

Benamou and Brenier [2000]:

$\alpha_t$ is scalaer valued measure, $v_t$ is vector valued measure

$\mathcal{C}(\alpha_{0},\alpha_{1})\overset{\mathrm{def.}}{\operatorname*{=}}\left\{(\alpha_{t},J_{t}):\frac{\partial\alpha_{t}}{\partial t}+\mathrm{div}(J_{t})=0,\alpha_{t=0}=\alpha_{0},\alpha_{t=1}=\alpha_{1}\right\},$

$\forall\left(a,b\right)\in\mathbb{R}_{+}\times\mathbb{R}^{d},\quad\theta(a,b)=\left\{\begin{array}{ll}\frac{\left\|o\right\|}{a}\quad\mathrm{if}\quad a>0,\\0\quad\mathrm{if}\quad(a,b)=0,\\+\infty\quad\text{otherwise.}\end{array}\right.$

Then there exists optimal monge map $T_\sharp\alpha_0=\alpha_1$

$\alpha_t=((1-t)\mathrm{Id}+tT)_\sharp\alpha_0.$

In other case(differnt cost function),不一定有monge map

$\alpha_t=P_{t\sharp}\pi\quad\mathrm{where}\quad P_t:(x,y)\in\mathbb{R}^d\times\mathbb{R}^d\mapsto(1-t)x+ty.$



discretized dynamic OT is convex but nonsmooth

$\Theta(\tilde{\mathbf{a}},\tilde{\mathbf{J}})=\min_{\tilde{\mathbf{z}}}\left\{\sum_{k,i}\tilde{\mathbf{z}}_{k,i}:\forall(k,i),(\mathbf{z}_{k,i},\tilde{\mathbf{a}}_{k,i},\tilde{\mathbf{J}}_{i,j})\in\mathcal{L}\right\},$

$\mathcal{L}=\{(z,a,J)\in R\times R^+\times R^d:\|J\|\leq za\}$

With this extra variable, it is thus possible to solve the discretized problem using standard interior point solvers for quadratic-cone programs

## low precision(DR)

$\min_{x\in\mathcal{H}}F(x)+G(x),$

F,G are convex function

$\forall x\in\mathcal{H},\quad\mathrm{Prox}_{\tau F}(x)\overset{\mathrm{def.}}{\operatorname*{=}}\mathrm{argmin}_{x^{\prime}\in\mathcal{H}}\frac{1}{2}\left\|x-x^{\prime}\right\|^{2}+\tau F(x)$

$\begin{aligned}&w^{(\ell+1)}\overset{\mathrm{def.}}{\operatorname*{=}}w^{(\ell)}+\alpha(\mathrm{Prox}_{\gamma F}(2x^{(\ell)}-w^{(\ell)})-x^{(\ell)}),\\&x^{(\ell+1)}\overset{\mathrm{def.}}{\operatorname*{=}}\mathrm{Prox}_{\gamma G}(w^{(\ell+1)}).\end{aligned}$

$F(x)\overset{\mathrm{def.}}{\operatorname*{=}}\Theta(\tilde{\mathbf{a}},\tilde{\mathbf{J}})+\iota_{\mathbf{C}(\mathbf{a}_0,\mathbf{a}_1)}(\mathbf{a},\mathbf{J})\quad\mathrm{and}\quad G(x)=\iota_{\mathcal{D}}(\mathbf{a},\mathbf{J},\tilde{\mathbf{a}},\tilde{\mathbf{J}}),\mathrm{where}\quad\mathcal{D}\overset{\mathrm{def.}}{\operatorname*{=}}\left\{(\mathbf{a},\mathbf{J},\tilde{\mathbf{a}},\tilde{\mathbf{J}}):\tilde{\mathbf{a}}=\mathcal{I}_{a}(\mathbf{a}),\tilde{\mathbf{J}}=\mathcal{I}_{J}(\mathbf{J})\right\}.$

# dynamic unbalanced OT

$\alpha_0(\mathcal{X})\neq\alpha_1(\mathcal{X})$

$\bar{\mathcal{C}}(\alpha_0,\alpha_1)\overset{\mathrm{def.}}{\operatorname*{=}}\left\{(\alpha_t,J_t,s_t):\frac{\partial\alpha_t}{\partial t}+\mathrm{div}(J_t)=s_t,\alpha_{t=0}=\alpha_0,\alpha_{t=1}=\alpha_1\right\}.$

$\mathrm{WFR}^{2}(\alpha_{0},\alpha_{1})=\min_{(\alpha_{t},J_{t},s_{t})_{t}\in\bar{C}(\alpha_{0},\alpha_{1})}\Theta(\alpha,J,s),\mathrm{(7.15)}\mathrm{where}\quad\Theta(\alpha,J,s)\overset{\mathrm{def.}}{\operatorname*{=}}\int_{0}^{1}\int_{\mathbb{R}^{d}}\left(\theta(\alpha_{t}(x),J_{t}(x))+\tau\theta(\alpha_{t}(x),s_{t}(x))\right)\mathrm{d}x\mathrm{d}t,$

$\begin{aligned}\frac{1}{\tau}\operatorname{WFR}(\alpha_{0},\alpha_{1})^{2}&\overset{\tau\to+\infty}{\operatorname*{\operatorname*{\longrightarrow}}}\int_{\mathcal{X}}|\sqrt{\rho_{\alpha_{0}}(x)}-\sqrt{\rho_{\alpha_{1}}(x)}|^{2}\mathrm{d}x\\&=\int_{\mathcal{X}}|1-\sqrt{\frac{\mathrm{d}\alpha_{1}}{\mathrm{d}\alpha_{0}}(x)}|^{2}\mathrm{d}\alpha_{0}(x).\end{aligned}$

## general mobility functional

$\forall\left(a,b\right)\in\mathbb{R}_+\times\mathbb{R}^d,\quad\theta(a,b)=a^{s-p}\left\|b\right\|^p,$

$p\geq 1.1\leq s\leq p$

s=1 classical OT

s>1 does not have linear growth as infintiy

s=p

$\|\alpha-\beta\|_{W^{-1,p}(\mathbb{R}^d)}^p=\min_f\left\{\int_{\mathbb{R}^d}f\mathrm{d}(\alpha-\beta):\int_{\mathbb{R}^d}\|\nabla f(x)\|^q\mathrm{d}x\leq1\right\}$

# path space

$\bar{\mathcal{U}}(\alpha_0,\alpha_1)\overset{\mathrm{def.}}{\operatorname*{=}}\left\{\bar{\pi}\in\mathcal{M}_+^1(\bar{\mathcal{X}}):\bar{P}_{0\sharp}\bar{\pi}=\alpha_0,\bar{P}_{1\sharp}\bar{\pi}=\alpha_1\right\},\text{where, for any path }\gamma\in\bar{\mathcal{X}},P_0(\gamma)=\gamma(0),P_1(\gamma)=\gamma(1).$

$\bar{\mathcal{X}}$ is the path space

$\mathcal{W}_2(\alpha_0,\alpha_1)^2=\min_{\bar{\pi}\in\bar{\mathcal{U}}(\alpha_0,\alpha_1)}\int_{\bar{\mathcal{X}}}\mathcal{L}(\gamma)^2\mathrm{d}\bar{\pi}(\gamma),$

$\mathcal{L}(\gamma)=\int_{0}^{1}|\gamma^{\prime}(s)|^{2}\mathrm{d}s$ is the kinetic energy of a path $\gamma(s)$

is that $\bar{\pi}$only gives mass to geodesics joining pairs of points in prop by $\pi$

$\pi^{\star}=\sum_{i,j}\mathbf{P}_{i,j}\delta_{(x_{i},y_{j})}\quad\mathrm{and}\quad\bar{\pi}^{\star}=\sum_{i,j}\mathbf{P}_{i,j}\delta_{\gamma_{x_{i},y_{j}}},$

$t\in[0,1]\mapsto\alpha_t\overset{\mathrm{def.}}{\operatorname*{=}}P_{t\sharp}\bar{\pi}^\star\quad\mathrm{where}\quad P_t(\gamma)=\gamma(t)\in\mathcal{X},$ is solution to dynamical formulation

### entropic OT over space of paths

$\min_{\bar{\pi}\in\bar{\mathcal{U}}(\alpha_0,\alpha_1)}\mathrm{KL}(\bar{\pi}|\bar{\mathcal{K}}).$

$\mathcal{\bar{K}}$ si the distribution of reversible brownian motion

$\epsilon \rightarrow 0$ as solution converge

$\bar{\gamma}_{x,y}^{\varepsilon}\in\bar{\mathcal{X}}$ is brownion bridge

$\pi_\varepsilon^\star=\sum_{i,j}\mathbf{P}_{\varepsilon,i,j}^\star\delta_{(x_i,y_j)}\quad\mathrm{and}\quad\bar{\pi}_\varepsilon^\star=\sum_{i,j}\mathbf{P}_{\varepsilon,i,j}^\star\bar{\gamma}_{x_i,y_j}^\varepsilon,$

$\alpha_{\varepsilon,t}\overset{\mathrm{def.}}{\operatorname*{=}}\mathrm{P}_{t\sharp}\bar{\pi}_\varepsilon^\star.$


Since the law $\mathbf{P}_{t\sharp}\bar{\gamma}_{x,y}^{\varepsilon}$ of the position at time $t$ along a Brownian bridge is a Gaussian $\mathcal{G}_{t(1-t)\varepsilon^2}(\cdot-\gamma_{x,y}(t))$ of variance $t(1-t)\varepsilon^2$ centered at $\gamma_x,y(t)$, one can deduce that $\alpha_\varepsilon,t$ is a Gaussian blurring of a set of traveling Diracs

$$\alpha_{\varepsilon,t}=\sum_{i,j}\mathbf{P}_{\varepsilon,i,j}^{\star}\mathcal{G}_{t(1-t)\varepsilon^2}(\cdot-\gamma_{x_i,y_j}(t)).$$

$\min_{(\alpha_t,v_t)_t\mathrm{~sat.~}(7.1)}\int_0^1\int_{\mathbb{R}^d}\left(\left\|v_t(x)\right\|^2+\frac{\varepsilon}{4}\left\|\nabla\log(\alpha_t)(x)\right\|^2\right)\mathrm{d}\alpha_t(x)\mathrm{d}t;$