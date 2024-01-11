# 习题 1

设 $p$ 为赋范空间 $X$ 上的次线性泛函，满足 $p(0) = 0$，且在 $0$ 处连续，求证：$p$ 为连续映射

## 解答

$p$ 为次线性泛函，即 $p(x + y) \le p(x) + p(y)$ 且 $p(\alpha x) = \alpha p(x)$，其中 $\alpha \ge 0$。

已知 $p$ 在 $0$ 处连续，即 $\forall \varepsilon > 0, \exists \delta > 0$，使得 $\forall x \in X$，$\|x\| < \delta$ 时，$|p(x)| < \varepsilon$。

对于任意 $x_0, x \in X, \|x\| < \delta$，有

$$
\begin{aligned}
p(x_0) = p(x_0 + x - x) &\le p(x_0 + x) + p(-x) \\
-\varepsilon < -p(-x) &\le p(x_0 + x) - p(x_0) \le p(x) + p(x_0) - p(x_0) \\
-\varepsilon &< p(x_0 + x) - p(x_0) \le p(x) < \varepsilon \\
|p(x_0 + x) - p(x_0)| &< \varepsilon
\end{aligned}
$$

故 $p$ 在 $x_0$ 处连续，故 $p$ 为连续映射。
