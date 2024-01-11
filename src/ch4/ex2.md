# 习题 2

设 $X$ 为线性空间，$p: X \to \mathbb{R}$，使得任取 $x, y \in X, \lambda \in \mathbb{K}$，有 $p(x + y) \le p(x) + p(y), p(\lambda x) = |\lambda| p(x)$。求证：$p$ 为 $X$ 上的半范数。

## 解答

回顾半范数定义：$p: X \to \mathbb{R}$ 满足

1. $\forall x \in X, p(x) \ge 0$
2. $\forall x, y \in X, p(x + y) \le p(x) + p(y)$
3. $\forall x \in X, \forall \lambda \in \mathbb{K}, p(\lambda x) = |\lambda| p(x)$

对比题设，只须证明 1 也成立

取 $\lambda = 0$，易得 $p(0) = 0$。再取 $y = -x$，则 $p(x + y) = p(0) \le p(x) + p(-x)$，因此任一对 $p(x), p(-x)$ 中至少有一个非负。

又 $p(-x) = |-1| p(x) = p(x)$，故 $p(x) = p(-x) \ge 0$，故 $p$ 为 $X$ 上的半范数。
