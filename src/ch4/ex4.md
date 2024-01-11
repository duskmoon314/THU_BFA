# 习题 4

设 $X$ 为赋范空间，$M$ 为 $X$ 的线性子空间，$x_0 \in X$。求证：$x_0 \in \overline{M}$ 当且仅当任取 $f \in X', f|_M = 0$ 时，$f(x_0) = 0$。

## 解答

### 充分性

$x_0 \in \overline{M}$，故 $\exists x_n \in M, x_n \to x_0$。

$f \in X'$，则 $f$ 连续，故 $f(x_n) \to f(x_0)$。

$f|_M = 0 \implies f(x_n) = 0 \implies f(x_0) = \lim\limits_{n \to \infty} f(x_n) = 0$。

### 必要性

假设 $x_0 \notin \overline{M}$，则 $\rho(x_0, M) > 0$。

由 Hahn-Banach 定理，$\exists f \in X', f|_M = 0, f(x_0) = 1, \|f\| = \rho(x_0, M)$。这与 $f(x_0) = 0$ 矛盾。

> 构造这一泛函可见 [$x_0$ is in the closure of $M$ iff there is no bounded linear functional on $X$](https://math.stackexchange.com/a/4108879/1111443)
