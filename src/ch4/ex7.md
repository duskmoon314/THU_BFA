# 习题 7

设 $X$ 为赋范空间，$M$ 为 $X'$ 的非空子集，求证：若 $\overline{\operatorname{span}(M)} = X'$，则 $\bigcap\limits_{f \in M} N(f) = \{0\}$。

## 解答

设 $x_0 \ne 0, x_0 \in \bigcap\limits_{f \in M} N(f)$，则 $\forall f \in M, f(x_0) = 0$。

由 Hahn-Banach 定理，$\exists f \in X', \|f\| = 1, f(x_0) = \|x_0\|$。

由 $\overline{\operatorname{span}(M)} = X'$，$\exists f_n = \sum\limits_{i \ge 1} a_{ni} f_i \to f$，其中 $f_i \in M, a_{ni} \in \mathbb{K}$。则有

$$
\begin{aligned}
|f_n(x_0) - f(x_0)| &= |\sum_{i \ge 1} a_{ni} f_i(x_0) - f(x_0)| \\
&= |\sum_{i \ge 1} a_{ni} \cdot 0 - \|x_0\|| \\
&= \|x_0\|
\end{aligned}
$$

由 $f_n \to f$，则 $\forall \varepsilon > 0, \exists N, \forall n > N, |f_n(x_0) - f(x_0)| < \varepsilon$。进而 $\|x_0\| < \varepsilon$，由 $\varepsilon$ 的任意性，$\|x_0\| = 0$，故 $x_0 = 0$。这与假设矛盾，故 $\bigcap\limits_{f \in M} N(f) = \{0\}$。
