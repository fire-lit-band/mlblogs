$\mathbf{H}(\mathbf{P})\overset{\mathrm{def.}}{\operatorname*{=}}-\sum_{i,j}\mathbf{P}_{i,j}(\log(\mathbf{P}_{i,j})-1)$

$\mathrm{L}_{\mathbf{C}}^{\varepsilon}(\mathbf{a},\mathbf{b})\overset{\mathrm{def.}}{\operatorname*{=}}\min_{\mathbf{P}\in\mathbf{U}(\mathbf{a},\mathbf{b})}\langle\mathbf{P},\mathbf{C}\rangle-\varepsilon\mathbf{H}(\mathbf{P}).$

H is 1-strongly concave

L is $\epsilon$ strongly convex

$\mathbf{P}_\varepsilon\xrightarrow{\varepsilon\to0}\underset{\mathbf{P}}{\operatorname*{\operatorname*{argmin}}}\{-\mathbf{H}(\mathbf{P}):\mathbf{P}\in\mathbf{U}(\mathbf{a},\mathbf{b}),\langle\mathbf{P},\mathbf{C}\rangle=\mathcal{L}_\mathbf{C}(\mathbf{a},\mathbf{b}),\}$

$\mathrm{L}_{\mathbf{C}}^{\varepsilon}(\mathbf{a},\mathbf{b})\xrightarrow{\varepsilon\to0}\mathrm{L}_{\mathbf{C}}(\mathbf{a},\mathbf{b}).\mathbf{P}_{\varepsilon}\overset{\varepsilon\to\infty}{\operatorname*{\longrightarrow}}\mathbf{a}\otimes\mathbf{b}=\mathbf{a}\mathbf{b}^{\mathrm{T}}=(\mathbf{a}_{i}\mathbf{b}_{j})_{i,j}.$

proof:

for $\epsilon_l$,denote $P_l$the solution for $\epsilon=\epsilon_l$,$P^*$ is the limit

$\langle\mathbf{C},\mathbf{P}\rangle=\mathrm{L}_\mathbf{C}(\mathbf{a},\mathbf{b})$

$0\leq\langle\mathbf{C},\mathbf{P}_{\ell}\rangle-\langle\mathbf{C},\mathbf{P}\rangle\leq\varepsilon_{\ell}(\mathbf{H}(\mathbf{P}_{\ell})-\mathbf{H}(\mathbf{P}))$

taking the limit

$\langle\mathbf{C},\mathbf{P}^\star\rangle=\langle C,P\rangle$

$H(P^*)\leq H(P)$

since P is abitary ,so $P^*$ is the optimal for minimization of entropy

for a small regularization $\epsilon$, the solution converges to the maximum entropy optimal transport coupling

$\epsilon$ increase ,the optimal coupling become less sparse

large $\epsilon$ showthe solution converge two describe two independent variable

$\mathbf{KL}(\mathbf{P}|\mathbf{K})\overset{\mathrm{def.}}{\operatorname*{=}}\sum_{i,j}\mathbf{P}_{i,j}\log\left(\frac{\mathbf{P}_{i,j}}{\mathbf{K}_{i,j}}\right)-\mathbf{P}_{i,j}+\mathbf{K}_{i,j},$

kernel $\mathbf{K}_{i,j}\overset{\mathrm{def.}}{\operatorname*{\operatorname*{=}}}e^{-\frac{\mathrm{C}_{i,j}}{\varepsilon}}.$

$\mathbf{P}_\varepsilon=\mathrm{Proj}_{\mathbf{U}(\mathbf{a},\mathbf{b})}^{\mathbf{KL}}(\mathbf{K})\overset{\mathrm{def.}}{\operatorname*{=}}\underset{\mathbf{P}\in\mathbf{U}(\mathbf{a},\mathbf{b})}{\operatorname*{\operatorname*{\mathrm{argmin}}}}\mathbf{KL}(\mathbf{P}|\mathbf{K}).$

$\mathcal{L}_c^\varepsilon(\alpha,\beta)\overset{\mathrm{def.}}{\operatorname*{=}}\mathcal{L}_\mathbf{C}^\varepsilon(\mathbf{a},\mathbf{b}),$

# general formula

$\mathcal{L}_c^\varepsilon(\alpha,\beta)\overset{\mathrm{def.}}{\operatorname*{=}}\min_{\pi\in\mathcal{U}(\alpha,\beta)}\int_{\mathcal{X}\times\mathcal{Y}}c(x,y)\mathrm{d}\pi(x,y)+\varepsilon\operatorname{KL}(\pi|\alpha\otimes\beta),$

$\begin{aligned}\mathrm{KL}(\pi|\xi)&\overset{\mathrm{def.}}{\operatorname*{=}}\int_{\mathcal{X}\times\mathcal{Y}}\log\left(\frac{\mathrm{d}\pi}{\mathrm{d}\xi}(x,y)\right)\mathrm{d}\pi(x,y)\\&+\int_{\mathcal{X}\times\mathcal{Y}}(\mathrm{d}\xi(x,y)-\mathrm{d}\pi(x,y)),\end{aligned}$

$\mathrm{KL}(\pi|\alpha\otimes\beta)=\mathrm{KL}(\pi|\alpha^{\prime}\otimes\beta^{\prime})-\mathrm{KL}(\alpha\otimes\beta|\alpha^{\prime}\otimes\beta^{\prime}).$ if$(\alpha',\beta')$haveing the same 0 measure sets as $(\alpha,\beta)$ 

$\min_{\pi\in\mathcal{U}(\alpha,\beta)}\mathrm{KL}(\pi|\mathcal{K})$

can be refactored as projection problem

$\mathrm{d}\mathcal{K}(x,y)\overset{\mathrm{def.}}{\operatorname*{=}}e^{-\frac{c(x,y)}{\varepsilon}}\mathrm{d}\alpha(x)\mathrm{d}\beta(y)$

$\mathcal{L}_c^\varepsilon(\alpha,\beta)=\min_{(X,Y)}\left\{\mathbb{E}_{(X,Y)}(c(X,Y))+\varepsilon\mathbb{I}(X,Y):X\sim\alpha,Y\sim\beta\right\},$

$\mathrm{I}(X,Y)\overset{\mathrm{def.}}{\operatorname*{=}}\mathrm{KL}(\pi|\alpha\otimes\beta)$

# solution and convergence

$\forall\left(i,j\right)\in\left[n\right]\times\left[m\right],\quad\mathbf{P}_{i,j}=\mathbf{u}_i\mathbf{K}_{i,j}\mathbf{v}_j$

$\mathrm{e}(\mathbf{u},\mathbf{v})\in\mathbb{R}_+^n\times\mathbb{R}_+^m$

proof:consider dual f,g

$\begin{aligned}&\text{an or (12) roado}\\&\mathcal{E}(\mathbf{P},\mathbf{f},\mathbf{g})=\langle\mathbf{P},\mathbf{~C}\rangle-\varepsilon\mathbf{H}(\mathbf{P})-\langle\mathbf{f},\mathbf{~P}\mathbb{1}_m-\mathbf{a}\rangle-\langle\mathbf{g},\mathbf{~P}^\mathrm{T}\mathbb{1}_n-\mathbf{b}\rangle.\end{aligned}$

$\frac{\partial\mathcal{E}(\mathbf{P},\mathbf{f},\mathbf{g})}{\partial\mathbf{P}_{i,j}}=\mathbf{C}_{i,j}+\varepsilon\log(\mathbf{P}_{i,j})-\mathbf{f}_i-\mathbf{g}_j=0,$

$\mathbf{P}_{i,j}=e^{\mathbf{f}_i/\varepsilon}e^{-\mathbf{C}_{i,j}/\varepsilon}e^{\mathbf{g}_j/\varepsilon}$

## matrix

P=diag(u)Kdiag(v)

$\operatorname{diag}(\mathbf{u})\mathbf{K}\operatorname{diag}(\mathbf{v})\mathbb{1}_m=\mathbf{a},\quad\operatorname{and}\quad\operatorname{diag}(\mathbf{v})\mathbf{K}^\top\operatorname{diag}(\mathbf{u})\mathbb{1}_n=\mathbf{b}.$

$\mathbf{u}\odot(\mathbf{K}\mathbf{v})=\mathbf{a}\quad\mathrm{and}\quad\mathbf{v}\odot(\mathbf{K}^\mathrm{T}\mathbf{u})=\mathbf{b},$

$\mathbf{u}^{(\ell+1)}\overset{\mathrm{def.}}{\operatorname*{=}}\frac{\mathbf{a}}{\mathbf{K}\mathbf{v}^{(\ell)}}\quad\mathrm{and}\quad\mathbf{v}^{(\ell+1)}\overset{\mathrm{def.}}{\operatorname*{=}}\frac{\mathbf{b}}{\mathbf{K}^{\mathrm{T}}\mathbf{u}^{(\ell+1)}}$

the inital  lead to differnt u,v,but iteration can converge

## complexity

setting$\varepsilon=\frac{4\operatorname{log}(n)}{\tau}$

Altschuler et al. [2017]

$O(\|\mathbf{C}\|_{\infty}^{3}\operatorname{log}(n)\tau^{-3})$ ieration are enough to ensure that

$\langle\hat{\mathbf{P}},\overset{\circ}{\operatorname*{\mathbf{C}}}\rangle\leq\overset{\circ}{\operatorname*{\operatorname*{L_C}(\mathbf{a},\mathbf{b})+\tau}}.$

$O(n^2\log(n)\tau^{-3})$ operations

### the rounding schem

$\begin{aligned}&\mathbf{u}^{\prime}\overset{\mathrm{def.}}{\operatorname*{=}}\mathbf{u}\odot\min\left(\frac{\mathbf{a}}{\mathbf{u}\odot(\mathbf{K}\mathbf{v})},\mathbf{1}_{n}\right),\mathbf{v}^{\prime}\overset{\mathrm{def.}}{\operatorname*{=}}\mathbf{v}\odot\min\left(\frac{\mathbf{b}}{\mathbf{v}\odot(\mathbf{K}^{\mathrm{T}}\mathbf{u}^{\prime})},\mathbf{1}_{n}\right),\\&\Delta_{\mathbf{a}}\overset{\mathrm{def.}}{\operatorname*{=}}\mathbf{a}-\mathbf{u}^{\prime}\odot(\mathbf{K}\mathbf{v}^{\prime}),\Delta_{\mathbf{b}}\overset{\mathrm{def.}}{\operatorname*{=}}\mathbf{b}-\mathbf{v}^{\prime}\odot(\mathbf{K}^{\mathrm{T}}\mathbf{u}),\\&\hat{\mathbf{P}}\overset{\mathrm{def.}}{\operatorname*{=}}\operatorname{diag}(\mathbf{u}^{\prime})\mathbf{K}\operatorname{diag}(\mathbf{v}^{\prime})+\Delta_{\mathbf{a}}(\Delta_{\mathbf{b}})^{\mathrm{T}}/\left\|\Delta_{\mathbf{a}}\right\|_{1}.\end{aligned}$

$\left\|\hat{\mathbf{P}}-\operatorname{diag}(\mathbf{u})\mathbf{K}\operatorname{diag}(\mathbf{v})\right\|_1\leq\left\|\mathbf{a}-\mathbf{u}\odot(\mathbf{K}\mathbf{v})\right\|_1+\left\|\mathbf{b}-\mathbf{v}\odot(\mathbf{K}^\mathrm{T}\mathbf{u})\right\|_1.$

# stability

for $\epsilon$,K may become too small to stored in memeory

cay out in log space

# proximal point algorithm for the KL metric

$F(\mathbf{P})\overset{\mathrm{def.}}{\operatorname*{=}}\langle\mathbf{P},\pi\rangle+\iota_{\mathbf{U}(\mathbf{a},\mathbf{b})}(\mathbf{P})$

$\iota_{\mathbf{U}(\mathbf{a},\mathbf{b})}(\mathbf{P})$ is the indicator function

$\mathbf{P}^{(\ell+1)}\overset{\mathrm{def.}}{\operatorname*{=}}\mathrm{Prox}_{\frac{1}{\varepsilon}F}^{\mathbf{KL}}(\mathbf{P}^{(\ell)})\overset{\mathrm{def.}}{\operatorname*{=}}\underset{\mathbf{P}\in\mathbb{R}_+^{n\times m}}{\operatorname*{\operatorname*{argmin}}}\mathbf{KL}(\mathbf{P}|\mathbf{P}^{(\ell)})+\frac{1}{\varepsilon}F(\mathbf{P})$

$\begin{aligned}P^{(\ell+1)}&\begin{aligned}=\operatorname{diag}(\mathbf{u}^{(\ell)})(e^{-\frac{\mathbf{C}}{\varepsilon}}\odot\mathbf{P}^{(\ell)})\operatorname{diag}(\mathbf{v}^{(\ell)})\end{aligned}\\&=\mathrm{diag}(\mathbf{u}^{(\ell)}\odot\cdots\odot\mathbf{u}^{(0)})e^{-\frac{(\ell+1)\mathbf{C}}{\varepsilon}}\odot\mathbf{P}^{(\ell)})\mathrm{diag}(\mathbf{v}^{(\ell)}\odot\cdots\odot\mathbf{v}^{(0)}).\end{aligned}$

This method is thus tightly connected to a series of works which combine Sinkhorn with some decaying schedule on the regularization

# other regularzation

replace entropic term by strictly convex penalty R(P)

$R(\mathbf{P})=\sum_{i,j}\mathbf{P}_{i,j}^2+\iota_{\mathbb{R}_+}(\mathbf{P}_{i,j});$

the constraint must add P>=0

The main advantage of the quadratic regularization over entropy is that it produces **sparse approximation** of the optimal coupling, yet this comes at the expense of a **slower algorithm that cannot be parallelized as efficiently** as Sinkhorn...

## Barycentric projection

$T:x_i\in\mathcal{X}\longmapsto\frac{1}{\mathbf{a}_i}\sum_j\mathbf{P}_{i,j}y_j\in\mathcal{Y},$

$T:x\in\mathcal{X}\longmapsto\int_{\mathcal{Y}}y\frac{\mathrm{d}\pi(x,y)}{\mathrm{d}\alpha(x)\mathrm{d}\beta(y)}\mathrm{d}\beta(y).$

### hilbert metric

hilbert projective metric

$\forall(\mathbf{u},\mathbf{u}^{\prime})\in(\mathbb{R}_{+,*}^n)^2,\quad d_{\mathcal{H}}(\mathbf{u},\mathbf{u}^{\prime})\overset{\mathrm{def.}}{\operatorname*{=}}\log\max_{i,j}\frac{\mathbf{u}_i\mathbf{u}_j^{\prime}}{\mathbf{u}_j\mathbf{u}_i^{\prime}}.$

$\begin{aligned}&d_{\mathcal{H}}(\mathbf{u},\mathbf{u}^{\prime})=\left\|\log(\mathbf{u})-\log(\mathbf{u}^{\prime})\right\|_{\mathrm{var}}\\&\mathrm{where}\quad\left\|\mathbf{f}\right\|_{\mathrm{var}}\overset{\mathrm{def.}}{\operatorname*{=}}(\max_{i}\mathbf{f}_{i})-(\min_{i}\mathbf{f}_{i}).\end{aligned}$

$\|f\|_{\infty}\leq\|f\|_{var}\leq 2\|f\|_{\infty}$

$\left.\begin{aligned}&d_{\mathcal{H}}(\mathbf{K}\mathbf{v},\mathbf{K}\mathbf{v}^{\prime})\leq\lambda(\mathbf{K})d_{\mathcal{H}}(\mathbf{v},\mathbf{v}^{\prime}),\mathrm{where}\left\{\begin{array}{l}{\lambda(\mathbf{K})\overset{\mathrm{def.}}{\operatorname*{=}}\frac{\sqrt{\eta(\mathbf{K})}-1}{\sqrt{\eta(\mathbf{K})}+1}<1,}\\{\eta(\mathbf{K})\overset{\mathrm{def.}}{\operatorname*{=}}\max_{i,j,k,\ell}\frac{\mathbf{K}_{i,k}\mathbf{K}_{j,\ell}}{\mathbf{K}_{j,k}\mathbf{K}_{i,\ell}}.}\end{array}\right.\\&d_{\mathcal{H}}(\mathbf{K}\mathbf{v},\mathbf{K}\mathbf{v}^{\prime})\leq\lambda(\mathbf{K})d_{\mathcal{H}}(\mathbf{v},\mathbf{v}^{\prime}),\mathrm{where}\left\{\begin{array}{l}{\lambda(\mathbf{K})\overset{\mathrm{def.}}{\operatorname*{=}}\frac{\sqrt{\eta(\mathbf{K})}-1}{\sqrt{\eta(\mathbf{K})}+1}<1,}\\{\eta(\mathbf{K})\overset{\mathrm{def.}}{\operatorname*{=}}\max_{i,j,k,\ell}\frac{\mathbf{K}_{i,k}\mathbf{K}_{j,\ell}}{\mathbf{K}_{j,k}\mathbf{K}_{i,\ell}}.}\end{array}\right.\end{aligned}\right.$

K is positive matrix

A matrix K,$K^T1_n=1_n$and K>0

then exit distirbution $p^*$,$Kp^*=p^*$

$,d_{\mathcal{H}}(\mathbf{K}^\ell p_0,p^\star)\leq\lambda(\mathbf{K})^\ell d_{\mathcal{H}}(p_0,p^\star),$

one has linear convergence of the iterates of the matrix toward $p^*$

## global convergence

$$d_\mathcal{H}(\mathbf{u}^{(\ell)},\mathbf{u}^\star)=O(\lambda(\mathbf{K})^{2\ell}),\quad d_\mathcal{H}(\mathbf{v}^{(\ell)},\mathbf{v}^\star)=O(\lambda(\mathbf{K})^{2\ell}).$$

$$d_{\mathcal{H}}(\mathbf{u}^{(\ell)},\mathbf{u}^{\star})\leq\frac{d_{\mathcal{H}}(\mathbf{P}^{(\ell)}\mathbb{1}_m,\mathbf{a})}{1-\lambda(\mathbf{K})^2},\\d_{\mathcal{H}}(\mathbf{v}^{(\ell)},\mathbf{v}^{\star})\leq\frac{d_{\mathcal{H}}(\mathbf{P}^{(\ell),\top}\mathbb{1}_n,\mathbf{b})}{1-\lambda(\mathbf{K})^2},$$

where we denoted $\mathbf{P}^(\ell)\overset{\mathrm{def.}}{\operatorname*{=}}$diag$(\mathbf{u}^(\ell))\mathbf{K}$ diag$(\mathbf{v}^(\ell)).$ Last, one has
$$\|\log(\mathbf{P}^{(\ell)})-\log(\mathbf{P}^\star)\|_\infty\leq d_\mathcal{H}(\mathbf{u}^{(\ell)},\mathbf{u}^\star)+d_\mathcal{H}(\mathbf{v}^{(\ell)},\mathbf{v}^\star),$$

$1-\lambda(\mathbf{K})\sim e^{-1/\varepsilon}.$

# local convergence

$\mathbf{f}^{(\ell+1)}=\Phi(\mathbf{f}^{(\ell)})$

$\|\mathbf{f}^{(\ell)}-\mathbf{f}\|=O((1-\kappa)^\ell).$

the second eigenvalue $1-\kappa<1$

# speeding

$a_1,\dots a_N$ histograms in $\Sigma_n$

 $b_1,\dots b_N$ histograms in $\Sigma_m$

$A=[a_1,\dots,a_n],B=[b_1,\dots,b_n]$

# separable kernel

$i=(i_k)_{k=1}^d,j=(j_k)_{k=1}^d\in[[n_1]]\times\cdots\times[[n_d]].$

$\mathbf{C}_{ij}=\sum_{k=1}^d\mathbf{C}_{i_k,j_k}^k,$

$\mathbf{K}_{i,j}=\prod_{k=1}^d\mathbf{K}_{i_k,j_k}^k.$

reduce the complexity to O($n^{1+1/d}$)  in place of $O(n^2)$

$c(x,y)=\|x-y\|_q^q=\sum_{i=1}^d|x_i-y_i|^q,q>0;$

$\mathbf{K}^k=\left[\exp(-\left|\frac{r-s}{n_k}\right|^q/\varepsilon)\right]_{1\leq r,s\leq n_k}$

$x_i=(i_1/n_1,\ldots,i_d/n_d)$

$(\mathbf{K}^2(\mathbf{K}^1\mathbf{U})^T)^T=\mathbf{K}^1\mathbf{U}\mathbf{K}^2$

exponent (1 + 1/d)

$(\mathbf{K}^{2}(\mathbf{K}^{1}\mathbf{U})^{T})^{T}=\mathbf{K}^{1}\mathbf{UK}^{2},$

With larger d, one needs to apply these very same 1-D convolutions to each slice of u (reshaped as a tensor of suitable size)

用列**自回归滤波器 (autoregressive filters)** 或者**傅里叶变换 (Fourier transform**近似卷积(linear time)

但epsilon比较小的时候，后者不稳定

## geodesic in heat apporixmation

$\mathbf{K}=e^{-\frac{d_{\mathcal{M}}}{\varepsilon}}$

this kernel is close to the Laplacian kernel (for p = 1) and the heat kernel (for p = 2).

$-\frac{\sqrt{t}}{2}\log(\mathcal{P}_t(x,y))=d_{\mathcal{M}}(x,y)+o(t)\quad\mathrm{where}\quad\mathcal{P}_t\overset{\mathrm{def.}}{\operatorname*{=}}(\mathrm{Id}-t\Delta_{\mathcal{M}})^{-1},$

# **extrapolation schemes**

**extrapolation schemes** for local linear convergence accerlate

from

$O((1-\kappa)^\ell)\mathrm{~to~}O((1-\sqrt{\kappa})^\ell)$

# stability

for $\mathbf{P}_{i,j}=e^{\mathbf{f}_{i}/\varepsilon}e^{-\mathbf{C}_{i,j}/\varepsilon}e^{\mathbf{g}_{j}/\varepsilon}.$

the minimum problem become

$\langle e^{\mathbf{f}/\varepsilon},\left(\mathbf{K}\odot\mathbf{C}\right)e^{\mathbf{g}/\varepsilon}\rangle-\varepsilon\mathbf{H}(\operatorname{diag}(e^{\mathbf{f}/\varepsilon})\mathbf{K}\operatorname{diag}(e^{\mathbf{g}/\varepsilon})).$

$\begin{aligned}&\langle\operatorname{diag}(e^{\mathbf{f}/\varepsilon})\mathbf{K}\operatorname{diag}(e^{\mathbf{g}/\varepsilon}),\mathbf{f}\mathbb{1}_m^\mathrm{T}+\mathbb{1}_n\mathbf{g}^\mathrm{T}-\mathbf{C}-\varepsilon\mathbb{1}_{n\times m}\rangle\\&=-\langle e^{\mathbf{f}/\varepsilon},(\mathbf{K}\odot\mathbf{C})e^{\mathbf{g}/\varepsilon}\rangle+\langle\mathbf{f},\mathbf{a}\rangle+\langle\mathbf{g},\mathbf{b}\rangle-\varepsilon\langle e^{\mathbf{f}/\varepsilon},\mathbf{K}e^{\mathbf{g}/\varepsilon}\rangle\end{aligned}$

we apply block coordinate for maximum the dual problem

$\nabla|_\mathbf{f}Q(\mathbf{f},\mathbf{g})=\mathbf{a}-e^{\mathbf{f}/\varepsilon}\odot\left(\mathbf{K}e^{\mathbf{g}/\varepsilon}\right),\nabla|_\mathbf{g}Q(\mathbf{f},\mathbf{g})=\mathbf{b}-e^{\mathbf{g}/\varepsilon}\odot\left(\mathbf{K}^\mathrm{T}e^{\mathbf{f}/\varepsilon}\right).$

$Q=\max_{\mathbf{f}\in\mathbb{R}^{n},\mathbf{g}\in\mathbb{R}^{m}}\langle\mathbf{f},\mathbf{a}\rangle+\langle\mathbf{g},\mathbf{b}\rangle-\varepsilon\langle e^{\mathbf{f}/\varepsilon},\mathbf{K}e^{\mathbf{g}/\varepsilon}\rangle.$

let the gradient=0 we obtain the dual ascent

## soft-min rewriting

$\min_{\varepsilon}\mathbf{z}=-\varepsilon\log\sum_{i}e^{-\mathbf{z}_{i}/\varepsilon}.$

$(\mathbf{f}^{(\ell+1)})_i=\min_\varepsilon(\mathbf{C}_{ij}-\mathbf{g}_j^{(\ell)})_j+\varepsilon\log\mathbf{a}_i,(\mathbf{g}^{(\ell+1)})_j=\min_\varepsilon(\mathbf{C}_{ij}-\mathbf{f}_i^{(\ell)})_i+\varepsilon\log\mathbf{b}_j.$

$\mathrm{Min}_{\varepsilon}^{\mathrm{row}}\left(\mathbf{A}\right)\overset{\mathrm{def.}}{\operatorname*{=}}\left(\min_{\varepsilon}\left(\mathbf{A}_{i,j}\right)_{j}\right)_{i}\in\mathbb{R}^{n},\mathrm{Min}_{\varepsilon}^{\mathrm{col}}\left(\mathbf{A}\right)\overset{\mathrm{def.}}{\operatorname*{=}}\left(\min_{\varepsilon}\left(\mathbf{A}_{i,j}\right)_{i}\right)_{j}\in\mathbb{R}^{m}.$

$\min_{\varepsilon}\mathbf{z}=\underline{\mathrm{z}}-\varepsilon\log\sum_{i}e^{-(\mathbf{z}_{i}-\underline{\mathrm{z}})/\varepsilon}.$

$\mathbf{f}^{(\ell+1)}=\mathrm{Min}_\varepsilon^\mathrm{row}\left(\mathbf{S}(\mathbf{f}^{(\ell)},\mathbf{g}^{(\ell)})\right)+\mathbf{f}^{(\ell)}+\varepsilon\log(\mathbf{a}),\mathbf{g}^{(\ell+1)}=\mathrm{Min}_\varepsilon^\mathrm{col}\left(\mathbf{S}(\mathbf{f}^{(\ell+1)},\mathbf{g}^{(\ell)})\right)+\mathbf{g}^{(\ell)}+\varepsilon\log(\mathbf{b}),$

$\mathbf{S}(\mathbf{f},\mathbf{g})=\left(\mathbf{C}_{i,j}-\mathbf{f}_i-\mathbf{g}_j\right)_{i,j}.$

it requires nm computations of exp at each step

# dual generic

$\sup_{(f,g)\in\mathcal{C}(\mathcal{X})\times\mathcal{C}(\mathcal{Y})}\int_{\mathcal{X}}f\mathrm{d}\alpha+\int_{\mathcal{Y}}g\mathrm{d}\beta-\varepsilon\int_{\mathcal{X}\times\mathcal{Y}}e^{\frac{-c(x,y)+f(x)+g(y)}{\varepsilon}}\mathrm{d}\alpha(x)\mathrm{d}\beta(y).$

unconstrained entropic dual

$\sup_{(f,g)\in\mathcal{C}(\mathcal{X})\times\mathcal{C}(\mathcal{Y})}\int_{\mathcal{X}}f\mathrm{d}\alpha+\int_{\mathcal{Y}}g\mathrm{d}\beta+\min_{\varepsilon}(c-f\oplus g),$

$\forall S\in\mathcal{C}(\mathcal{X}\times\mathcal{Y}),\quad\min_\varepsilon S\overset{\mathrm{def.}}{\operatorname*{=}}-\varepsilon\int_{\mathcal{X}\times\mathcal{Y}}e^{\frac{-S(x,y)}{\varepsilon}}\mathrm{d}\alpha(x)\mathrm{d}\beta(y)$

A disadvantage of this alternative dual formulation is that the presence of a log prevents the use of stochastic optimization methods

## optimal trasnport

$\langle\mathbf{f}^{\star},\mathbf{a}\rangle+\langle\mathbf{g}^{\star},\mathbf{b}\rangle\leq\mathcal{L}_{\mathbf{C}}(\mathbf{a},\mathbf{b}).$

Proposition $4. 6. \mathrm{~L}_{\mathbb{C} }^{\varepsilon }( \mathbf{a} , \mathbf{b} )$ is a jointly convex function of a and b for $\varepsilon\geq0.$ When
$\varepsilon>0$, its gradient is equal to

$$\nabla\mathrm{L}_\mathbf{C}^\varepsilon(\mathbf{a},\mathbf{b})=\begin{bmatrix}\mathbf{f}^\star\\\mathbf{g}^\star\end{bmatrix},$$

## sinkhorn divergence

$\begin{aligned}&\mathfrak{P}_{\mathbf{C}}^{\varepsilon}(\mathbf{a},\mathbf{b})\overset{\mathrm{def.}}{\operatorname*{=}}\langle\mathbf{C},\mathbf{P}^{\star}\rangle=\langle e^{\frac{\mathbf{f}^{\star}}{\varepsilon}},(\mathbf{K}\odot\mathbf{C})e^{\frac{\mathbf{g}^{\star}}{\varepsilon}}\rangle,\\&\mathfrak{D}_{\mathbf{C}}^{\varepsilon}(\mathbf{a},\mathbf{b})\overset{\mathrm{def.}}{\operatorname*{=}}\langle\mathbf{f}^{\star},\mathbf{a}\rangle+\langle\mathbf{g}^{\star},\mathbf{b}\rangle,\end{aligned}$

$\mathfrak{D}_\mathbf{C}^\varepsilon(\mathbf{a},\mathbf{b})\leq\mathrm{L}_\mathbf{C}^\varepsilon(\mathbf{a},\mathbf{b})\leq\mathfrak{P}_\mathbf{C}^\varepsilon(\mathbf{a},\mathbf{b}).\mathfrak{P}_\mathbf{C}^\varepsilon(\mathbf{a},\mathbf{b})-\mathfrak{D}_\mathbf{C}^\varepsilon(\mathbf{a},\mathbf{b})=\varepsilon(\mathbf{H}(\mathbf{P}^\star)+1).$

proof:

$\mathcal{L}_{\mathbf{C}}^{\varepsilon}(\mathbf{a},\mathbf{b})=\mathfrak{P}_{\mathbf{C}}^{\varepsilon}(\mathbf{a},\mathbf{b})-\varepsilon\mathbf{H}(\mathbf{P}^{\star})=\mathfrak{D}_{\mathbf{C}}^{\varepsilon}(\mathbf{a},\mathbf{b})-\varepsilon\langle e^{\mathbf{f}^{\star}/\varepsilon},\mathbf{K}e^{\mathbf{g}^{\star}/\varepsilon}\rangle$

$\mathrm{t}\langle e^{\mathbf{f}^{\star}/\varepsilon},\mathbf{K}e^{\mathbf{g}^{\star}/\varepsilon}\rangle=1$

$\mathfrak{D}_\mathbf{C}^{(L)}(\mathbf{a},\mathbf{b})\overset{\mathrm{def.}}{\operatorname*{=}}\langle\mathbf{f}^{(L)},\mathbf{a}\rangle+\langle\mathbf{g}^{(L)},\mathbf{b}\rangle.$

Sinkhorn functional lower bounds the regularized cost function

$\mathfrak{D}_\mathbf{C}^{(L)}(\mathbf{a},\mathbf{b})\leq\mathfrak{L}_\mathbf{C}^\varepsilon(\mathbf{a},\mathbf{b}).$

the rounding scheme is the upper bound on $L_c^\epsilon(a,b)$ and do not satisfy primal feasible

the sinkhorn divergence $\mathfrak{D}_\mathbf{C}^{(L)}(\mathbf{a},\mathbf{b})$ is not convexhowever, a differentiable function which can be differentiated using automatic differentiation techniques

# general

$\min_{\mathbf{P}}\sum_{i,j}\mathbf{C}_{i,j}\mathbf{P}_{i,j}-\varepsilon\mathbf{H}(\mathbf{P})+F(\mathbf{P}\mathbb{1}_m)+G(\mathbf{P}^\mathrm{T}\mathbb{1}_n).$

$\mathbf{u}\leftarrow\frac{\mathrm{Prox}_{F}^{\mathbf{KL}}(\mathbf{K}\mathbf{v})}{\mathrm{K}\mathbf{v}}\quad\mathrm{and}\quad\mathbf{v}\leftarrow\frac{\mathrm{Prox}_{G}^{\mathbf{KL}}(\mathbf{K}^{\mathrm{T}}\mathbf{u})}{\mathbf{K}^{\mathrm{T}}\mathbf{u}},$

$\forall\mathbf{u}\in\mathbb{R}_+^N,\quad\mathrm{Prox}_F^{\mathbf{KL}}(\mathbf{u})=\underset{\mathbf{u}^{\prime}\in\mathbb{R}_+^N}{\operatorname*{\operatorname*{\operatorname*{argmin}}}}\mathbf{KL}(\mathbf{u}^{\prime}|\mathbf{u})+F(\mathbf{u}^{\prime}).$

F is the indicator function，也可以被general成其他形式

$\mathrm{Prox}_F^{\mathbf{KL}}(\mathbf{u})=\left(\mathrm{Prox}_{F_i}^{\mathbf{KL}}(\mathbf{u}_i)\right)_i.$ $F(\mathbf{u})=\sum_iF_i(\mathbf{u}_i)$

the dual is 

$\max_{\mathbf{f},\mathbf{g}}-F^*(\mathbf{f})-G^*(\mathbf{g})-\varepsilon\sum_{i,j}e^{\frac{\mathbf{f}_i+\mathbf{g}_j-\mathbf{C}_{i,j}}{\varepsilon}}$

$\forall\mathbf{f}\in\mathbb{R}^n,\quad F^*(\mathbf{f})\overset{\mathrm{def.}}{\operatorname*{=}}\max_{\mathbf{a}\in\mathbb{R}^n}\langle\mathbf{f},\mathbf{a}\rangle-F(\mathbf{a}).$