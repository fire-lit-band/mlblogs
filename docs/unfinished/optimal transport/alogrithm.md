# Kronecker

$\mathbf{A}=\begin{bmatrix}\mathbb{1_n}^{\mathrm{T}}\otimes\mathbb{1_m}\\\mathbb{1_n}\otimes\mathbb{1_m}^{\mathrm{T}}\end{bmatrix}\in\mathbb{R}^{(n+m)\times nm}$

$\mathbf{P}\in\mathbb{R}^{n\times m}\in\mathbf{U}(\mathbf{a},\mathbf{b})\Leftrightarrow\mathbf{p}\in\mathbb{R}_+^{nm},\mathbf{A}\mathbf{p}=[\begin{array}{l}\mathbf{a}\\\mathbf{b}\end{array}].$

$\mathcal{L}_{\mathbf{C}}(\mathbf{a},\mathbf{b})=\min_{\mathbf{p}\in\mathbb{R}_{+}^{nm}}\mathbf{c}^{\mathrm{T}}\mathbf{p},\\\mathbf{A}\mathbf{p}=\left[{\begin{array}{c}\mathbf{a}\\\mathbf{b}\end{array}}\right]$

the dual problem is 

$\mathcal{L}_{\mathbf{C}}(\mathbf{a},\mathbf{b})=\max_{\begin{array}{c}\mathbf{h}\in\mathbb{R}^{n+m}\\A^{\mathrm{T}}\mathbf{h}\leq\mathbf{c}\end{array}}\left[\mathbf{\begin{array}{c}\mathbf{a}\\\mathbf{b}\end{array}}\right]^{\mathrm{T}}\mathbf{h}.$

and has strong duality

# c-transform

fix f,then the optimal for g is $f^C$ denoted as

$(\mathbf{f}^\mathbf{C})_j=\min_{i\in[n]}\mathbf{C}_{ij}-\mathbf{f}_i,$

$\langle\mathrm{f,~a\rangle+\langle g,~b\rangle\leq\langle f,~a\rangle+\langle f^{C},~b\rangle.}$

similar for g,the $$(\mathbf{g}^{\bar{\mathbf{C}}})_i=\min_{j\in[m]]}\mathbf{C}_{ij}-\mathbf{g}_j,$$

$\langle\mathbf{f},\mathbf{a}\rangle+\langle\mathbf{f}^\mathbf{C},\mathbf{b}\rangle\leq\langle\mathbf{f}^\mathbf{C}\bar{\mathbf{C}},\mathbf{a}\rangle+\langle\mathbf{f}^\mathbf{C},\mathbf{b}\rangle\leq\langle\mathbf{f}^{\mathbf{C}\bar{\mathbf{C}}},\mathbf{a}\rangle+\langle\mathbf{f}^{\mathbf{C}\bar{\mathbf{C}}\mathbf{C}},\mathbf{b}\rangle\leq\ldots$

and have three properties

(1)$f\leq f'$, then $f^C\geq f'^C$

(2)$f^{C\bar{C}}\geq f,g^{\bar{C}C}\geq g$

(3)$f^{C\bar{C}C}=f^C$

## complementray slackness

$\mathbf{P}_{i,j}^\star(\mathbf{C}_{i,j}-\mathbf{f}_i^\star+\mathbf{g}_j^\star)=0$

*means optimal here

note strong duality $\langle\mathbf{P}^\star,\mathbf{C}\rangle=\langle\mathbf{f}^\star,\mathbf{a}\rangle+\langle\mathbf{g}^\star,\mathbf{b}\rangle.$

# verticy

a vertex or an extremal point of a convex set is formally a point x in that set such that, if there exiss y and z in that set with x = (y + z)/2, then necessarily x = y = z.

P is extremal point,$$

$\{(i,j^{\prime}),i\in[[n]],j\in[m]\text{ such that }\mathbf{P}_{ij}>0$

$G(\mathbf{P})\overset{\mathrm{def.}}{\operatorname*{=}}(V\cup V^{\prime},S(\mathbf{P}))$have no cycle

P cannot have more than n+m-1 nonzero entries

proof:

$H=\left\{(i_1,j_1^{\prime}),(i_2,j_1^{\prime}),(i_2,j_2^{\prime}),\ldots,(i_k,j_k^{\prime}),(i_1,j_k^{\prime})\right\}.$

$\varepsilon<\min_{(i,j^{\prime})\subseteq F}\mathbf{P}_{ij}.$,F=S(P)

Consider a perturbation matrix E

(i,j) entry is equal to$\varepsilon\mathrm{if~}i\to j^{\prime}\in\bar{H}$$,-\varepsilon\mathrm{~if~}j\to i^{\prime}\in\bar{H}$and zero otherwise

Q = P + E and R = P−E contradtiion

n+m node, so

## North western

Formally, the algorithm works as follows: $i$ and $j$ are initialized to $1,r\leftarrow\mathbf{a}_1,c\leftarrow\mathbf{b}_1.$ While $i\leq n$ and $j\leq m$, set $t\leftarrow\min(r,c),\textbf{ P}_{i,j}\leftarrow t,r\leftarrow r-t,c\leftarrow s-t;$ if $r=0$ then increment $i$, and update $r\leftarrow\mathbf{a}_i$ if $i\leq n;$ if $c=0$ then increment $j$, and update $c\leftarrow\mathbf{b}_j$ if $j\leq n;$ repeat. 

we can also permute a,b

$\mathcal{N}(\mathbf{a},\mathbf{b})\overset{\mathrm{def.}}{\operatorname*{=}}\{\mathbf{N}\mathbf{W}_{\sigma^{-1}\sigma^{\prime}-1}(r_\sigma,c_{\sigma^{\prime}}),\sigma,\sigma^{\prime}\in S_d\}.$

## Obtaining a Dual Pair Complementary to P

选一个点作为root,f=0，然后往下计算下去

Network Simplex Update

如果有$f_i+g_j\leq C_{i,j}$

加入(i,j)到G

如果G变成forest，连上，并选取他为root，算dual

如果G有circle

$\theta=\min_k\mathbf{P}_{i_{k+1},j_k}$$

$\forall k\leq l,\quad\tilde{\mathbf{P}}_{i_{k},j_{k}}:=\mathbb{P}_{i_{k},j_{k}}+\theta;\quad\tilde{\mathbf{P}}_{i_{k+1},j_{k}}:=\mathbb{P}_{i_{k+1},j_{k}}-\theta.$

$(i_1,j_1^{\prime}),(j_1^{\prime},i_2),(i_2,j_2^{\prime}),\ldots,(i_l,j_l^{\prime}),(j_l^{\prime},i_{l+1})$

increase input flow,decrease output flow

$\langle\tilde{\mathbf{P}},\mathbf{C}\rangle=\langle\mathbf{P},\mathbf{C}\rangle+\theta\left(\mathbf{C}_{i,j}-(\mathbf{f}_{i}-\mathbf{f}_{g})\right)<\langle\mathbf{P},\mathbf{C}\rangle.$

$O\begin{pmatrix}(n+m)nm\log(n+m)\log\left((n+m)\|\mathbf{C}\|_\infty\right)\end{pmatrix}$

# dual ascent

$1_S$ for the vector of zeros except ones index in S

balanced pair (i,j') if $f_i+g_j=C_{ij}$

inactive if $f_i+g_j<C_{ij}$

$(\tilde{\mathbf{f}},\tilde{\mathbf{g}})\overset{\mathrm{def.}}{\operatorname*{=}}(\mathbf{f},\mathbf{g})+\varepsilon(1_S,-1_{S^{\prime}})$

if $\forall i \in S$,(i,j')is balanced,then $j' \in S'$

then  $(\tilde{\mathbf{f}},\tilde{\mathbf{g}})$is dual feasible form small $\epsilon$

proof:

$I_i$is the set that (i,j') is inactive

$\varepsilon_i\overset{\mathrm{def.}}{\operatorname*{\operatorname*{=}}}\min_{j\in I_i}{\operatorname*{\operatorname*{C}_{i,j}}}-\mathrm{f}_i-\mathrm{g}_j$

then $\tilde{\mathbf{f}}_i+\tilde{\mathbf{g}}_j<{{C}}_{i,j}$ for $i\in I_i$

then for $j'\in B_i=[m]/I_i$ $B_i$ is balanced

$j^{\prime}\in\mathcal{B}_i,\tilde{\mathbf{f}}_i+\tilde{\mathbf{g}}_j=\mathbf{f}_i+\mathbf{g}_j=\mathbf{C}_{i,j}.$

## auction

consider assignment problem

$\mathrm{f}_i^\star+\mathrm{g}_{\sigma_i^\star}^\star=\mathrm{C}_{i,\sigma_i^\star}.$

$\mathrm{C}_{i,\sigma_{i}^{\star}}-\mathrm{g}_{\sigma_{i}}^{\star}=f^*=\mathbf{g}^{\bar{\mathbf{C}}}=\min_{j}\mathrm{C}_{i,j}-\mathrm{g}_{j}^{\star}.$

if exits g,$\sigma$ let the equation hold, then they both optimal

the number of step at most $n\|\mathbb{C}\|_{\infty}/\varepsilon.$

The auction algorithm finds an assignment whose cost is $n\epsilon$ suboptimal.