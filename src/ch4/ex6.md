# 习题 6

设 $X$ 为赋范空间，$f \in X^*$。求证：$f \in X'$ 当且仅当 $N(f)$ 为 $X$ 的闭线性子空间。

## 解答

### 充分性

$\forall x_1, x_2 \in N(f), \alpha, \beta \in \mathbb{K}, f(\alpha x_1 + \beta x_2) = \alpha f(x_1) + \beta f(x_2) = \alpha 0 + \beta 0 = 0$，故 $\alpha x_1 + \beta x_2 \in N(f)$，故 $N(f)$ 为 $X$ 的线性子空间。

$\forall x_n \in N(f), x_n \to x$，由 $f \in X'$ 知 $f$ 连续，故 $f(x) = \lim\limits_{n \to \infty} f(x_n) = \lim\limits_{n \to \infty} 0 = 0$，故 $x \in N(f)$，故 $N(f)$ 为 $X$ 的闭线性子空间。

### 必要性

$N(f)$ 为 $X$ 的闭线性子空间，故 $N(f) = \overline{N(f)}$。

若 $N(f) = X$，则 $f = 0 \in X'$。

若 $N(f) \subsetneq X$，则 $N(f)$ 不稠密，故 $\exists x_0 \in X \setminus N(f), r > 0, B(x_0, r) \subset X \setminus N(f)$。

假设 $f \in X^* \setminus X'$，则 $f(B(x_0), r)$ 不是有界集，进而 $f(x_0) + rB(0, 1)$ 不是有界集。

$\forall k \in \mathbb{K}, \exists x_1 \in B(x_0, r), |f(x_1)| > |k|$。取 $x_2 = x_0 - \frac{f(x_0)}{f(x_1)} x_1$，则 $\|x_2 - x_0\| = \|\frac{x_0}{x_1} x_1\| = |\frac{f(x_0)}{f(x_1)}| \|x_1\|$，由 $|f(x_1)|$ 可任意大，故 $\|x_2 - x_0\|$ 可任意小，故 $x_2 \in B(x_0, r)$。

又 $|f(x_2)| = |f(x_0) - f(x_0)| = 0$，即 $x_2 \in N(f)$，与 $x_2 \in B(x_0, r) \subset X \setminus N(f)$ 矛盾。

故 $f \in X'$。
