# 赋范空间

## 线性空间和维数

**线性空间** $X$ 为 $\mathbb{K}$ 上的线性空间，若

1. $\forall x,y \in X, x + y = y + x$
2. $\forall x,y,z \in X, (x + y) + z = x + (y + z)$
3. $\exists 0 \in X, \forall x \in X, x + 0 = 0 + x$
4. $\forall x \in X, \exists -x \in X, x + (-x) = 0$
5. $\forall x \in X, \forall \alpha, \beta \in \mathbb{K}, \alpha(\beta x) = (\alpha \beta)x$
6. $\forall x \in X, 1 x = x$
7. $\forall x, y \in X, \alpha \in \mathbb{K}, \alpha(x + y) = \alpha x + \alpha y$
8. $\forall x,y \in X, \alpha, \beta \in \mathbb{K}, (\alpha + \beta)x = \alpha x + \beta x$

**线性无关** $x_1, x_2, \cdots, x_n \in X$ 线性无关，若 $\exists \alpha_1, \alpha_2, \cdots, \alpha_n \in \mathbb{K}, \alpha_1 x_1 + \alpha_2 x_2 + \cdots + \alpha_n x_n = 0$，则 $\alpha_1 = \alpha_2 = \cdots = \alpha_n = 0$

**Hamel 基** $M$ 为 $X$ 的 Hamel 基，若 $M$ 为 $X$ 线性无关子集且 $\operatorname{span}(M) = X$

设 $X$ 为线性空间，$X \ne \{0\}$，$M_0$ 为线性无关子集，则一定存在 Hamel 基 $N$ 使得 $M_0 \subset N$

## 赋范空间和 Banach 空间

**范数** $\|\cdot\|: X \to \mathbb{R}$，若

1. 非负性：$\forall x \in X, \|x\| \ge 0$
2. 非退化性：$\forall x \in X, \|x\| = 0 \iff x = 0$
3. 齐次性：$\forall x \in X, \forall \alpha \in \mathbb{K}, \|\alpha x\| = |\alpha| \|x\|$
4. 三角不等式：$\forall x, y \in X, \|x + y\| \le \|x\| + \|y\|$

**赋范空间** 序对 $(X, \|\cdot\|)$ 为赋范空间，其中 $X$ 为线性空间，$\|\cdot\|$ 为范数

**诱导度量** $d(x, y) = \|x - y\|$

1. 平移不变性：$\forall x, y, z \in X, d(x + z, y + z) = d(x, y)$
2. 齐次性：$\forall x, y \in X, \forall \alpha \in \mathbb{K}, d(\alpha x, \alpha y) = |\alpha| d(x, y)$

**Banach 空间** $X$ 为 Banach 空间，若诱导度量使之成为完备空间

**线性算子** $T: X \to Y$ 为线性算子，若

1. $\forall x, y \in X, T(x + y) = T(x) + T(y)$
2. $\forall x \in X, \forall \alpha \in \mathbb{K}, T(\alpha x) = \alpha T(x)$

**等距同构** $T: X \to Y$ 为等距同构，若

1. $T$ 为线性算子，且 $T$ 为双射
2. $\forall x \in X, \|T(x)\|_Y = \|x\|_X$

**Schauder 基** $\{e_n\}$ 为 $X$ 的 Schauder 基，若 $\forall x \in X, \exists! \alpha_n \in \mathbb{K}, x = \sum\limits_{n = 1}^\infty \alpha_n e_n$

## 有限维赋范空间

**等价范数** $\|\cdot\|_1, \|\cdot\|_2$ 为等价范数，若 $\exists c_1, c_2 > 0, \forall x \in X, c_1 \|x\|_1 \le \|x\|_2 \le c_2 \|x\|_1$

设 $X$ 为赋范空间，$x_1, x_2, \cdots, x_n \in X$ 线性无关，则存在常数 $c > 0$，使得 $\forall \alpha_1, \alpha_2, \cdots, \alpha_n \in \mathbb{K}, \| \alpha_1 x_1 + \alpha_2 x_2 + \cdots + \alpha_n x_n \| \ge c(|\alpha_1| + |\alpha_2| + \cdots + |\alpha_n|)$

设 $X$ 为有限维赋范空间，则 $X$ 上的任意两个范数等价，且 $X$ 赋予任意范数均是 Banach 空间

设 $X$ 为赋范空间，$Y$ 为有限维线性子空间，则 $Y$ 必为 Banach 空间，因此总为闭线性子空间

设 $X$ 为有限维赋范空间，则 $M \subset X$ 为紧集 $\iff M$ 为有界闭集

## 有界线性算子

**有界线性算子** $T: X \to Y$ 为有界线性算子，若 $\exist C \ge 0, \forall x \in X, \|T(x)\|_Y \le C \|x\|_X$

**算子范数** $\|T\| = \sup\limits_{x \ne 0} \frac{\|T(x)\|}{\|x\|}$

设 $X, Y$ 为赋范空间，$T: X \to Y$ 为有界线性算子，则 $\|T\| = \sup\limits_{\|x\| \le 1} \|T(x)\| = \sup\limits_{\|x\| = 1} \|T(x)\|$

**有界线性算子空间** 记 $B(X, Y)$ 为有界线性算子空间

设 $X, Y$ 为赋范空间，$T: X \to Y$ 为线性算子，则下述命题相互等价

1. $T$ 在 $x = 0$ 连续
2. $T$ 在某点连续
3. $T$ 为连续映射
4. $T$ 为有界线性算子

设 $X, Y$ 为赋范空间，$T: X \to Y$ 为有界线性算子，则 $T$ 的零空间 $N(T) = \{x \in X: T(x) = 0\}$ 为闭线性子空间

设 $X$ 为赋范空间，$Y$ 为 Banach 空间，则 $B(X, Y)$ 为 Banach 空间

**延拓** $X_0 \subset X, T: X \to Y, S: X_0 \to Y$，若 $\forall x \in X_0, S(x) = T(x)$，则 $T$ 为 $S$ 的延拓，$S$ 为 $T$ 的限制，记 $S = T \mid_{X_0}$

设 $X$ 赋范空间，$Y$ Banach 空间，$X_0 \subset X$ 为稠密线性子空间，又设 $T_0 \in B(X_0, Y)$，则存在唯一的 $T \in B(X, Y)$ 使得 $T \mid_{X_0} = T_0$ 且 $\|T\| = \|T_0\|$

## 有界线性泛函及其表示

**线性泛函** 线性算子 $f: X \to \mathbb{K}$

**代数对偶空间** $X^* = \{\text{全体线性泛函}\}$

**拓扑对偶空间（对偶空间、共轭空间）** $X' = B(X, \mathbb{K})$

常见赋范空间的对偶空间：

- $(\mathbb{K}^n, \|\cdot\|_2)' = (\mathbb{K}^n, \|\cdot\|_2)$
- $(\mathbb{K}^n, \|\cdot\|_p)' = (\mathbb{K}^n, \|\cdot\|_q)$
- $c_0' = \ell^1$，其中 $c_0 = (\{\{x_n\} \in \ell^\infty: \lim\limits_{n \to \infty} x_n = 0\}, \|\cdot\|_\infty)$
- $(\ell^1)' = \ell^\infty$
- $(\ell^p)' = \ell^q$，其中 $1 < p < \infty, \frac{1}{p} + \frac{1}{q} = 1$
