# 习题 5

设 $X$ 为可分赋范空间，求证：存在 $X'$ 单位球面的可数子集 $N$，使得任取 $x \in X$，有 $\|x\| = \sup\limits_{f \in N} |f(x)|$。

## 解答

记 $S$ 为 $X'$ 的单位球面。

$X$ 可分，即 $\exists M$ 为可数集，且 $\overline{M} = X$

由 Hahn-Banach 定理，$\forall x \in X, x \ne 0, \exists f_x \in X', \|f_x\| = 1, f_x(x) = \|x\|$。

构造集合 $N = \{f_x: x \in M\}$，则 $M$ 为可数集 $\implies N$ 为可数集，且 $\|f_x\| = 1 \implies N \subset S$。故 $N$ 为 $S$ 的可数子集。

$\forall f \in N, |f(x)| \le \|f\| \|x\| = \|x\| \implies \sup\limits_{f \in N} |f(x)| \le \|x\|$。

$\forall x \in X, \exists x_n \in M, x_n \to x$，即 $\forall \varepsilon > 0, \exists K, \forall k > K, \|x_k - x\| < \varepsilon$。

$$
\begin{aligned}
|f_{x_k}(x)| &= |f_{x_k}(x_k + (x - x_k))| \\
&= |f_{x_k}(x_k) + f_{x_k}(x - x_k)| \\
&\le |f_{x_k}(x_k)| + |f_{x_k}(x - x_k)| \\
&= \|x_k\| + |f_{x_k}(x - x_k)| \\
&\le \|x_k\| + \|f_{x_k}\| \|x - x_k\| \\
&= \|x_k\| + \|x - x_k\| \\
&< \|x_k\| + \varepsilon
\end{aligned}
$$

由 $\varepsilon$ 的任意性，$\sup\limits_{f \in N} |f(x)| = \|x\|$。
