# 赋范空间中的基本定理

## Hahn-Banach 定理

**次线性泛函** $p: X \to \mathbb{R}$，若

1. $\forall x, y \in X, p(x + y) \le p(x) + p(y)$
2. $\forall x \in X, \alpha \ge 0, p(\alpha x) = \alpha p(x)$

**Hahn-Banach 定理（1）** 设 $X$ 为实线性空间，$p$ 为次线性泛函，$Z$ 为线性子空间，$f \in Z^*$，设 $f(x) \le p(x)$，则 $\exists g \in X^*, g\mid_Z = f, g(x) \le p(x)$

**半范数** $p: X \to \mathbb{R}$，若

1. $\forall x \in X, p(x) \ge 0$
2. $\forall x, y \in X, p(x + y) \le p(x) + p(y)$
3. $\forall x \in X, \alpha \in \mathbb{K}, p(\alpha x) = |\alpha| p(x)$

**Hahn-Banach 定理（2）** 设 $X$ 为线性空间，$p$ 为半范数，$Z$ 为线性子空间，$f \in Z^*$，设 $f(x) \le p(x)$，则 $\exists g \in X^*, g\mid_Z = f, g(x) \le p(x)$

**Hahn-Banach 定理（3）** 设 $X$ 为赋范空间，$Z$ 为线性子空间，$f \in Z'$，则 $\exists g \in X', g\mid_Z = f, \|g\| = \|f\|$

**Hahn-Banach 定理（4）** 设 $X$ 为赋范空间，$x_0 \in X, x_0 \ne 0$，则 $\exists f \in X', \|f\| = 1, f(x_0) = \|x_0\|$

$x_0 = 0 \implies f(x_0) = 0, \forall f \in X'$

设 $X$ 为非零赋范空间，$x_0 \in X$，则 $\|x_0\| = \max\limits_{f \ne 0} \frac{|f(x_0)|}{\|f\|} = \max\limits_{\|f\| \le 1} |f(x_0)|$

**共轭算子** $T^*: Y' \to X'$，$T^*(f) = f \circ T$

**共轭算子的性质** 设 $X, Y$ 为赋范空间，$T \in B(X, Y)$，则 $T^* \in B(Y', X')$，且 $\|T^*\| = \|T\|$

**典范映射** $J: X \to X'', J(x) = g_x$，$g_x(f) = f(x)$

**自反空间** $X$ 为自反空间，若 $J$ 为满射

设 $X$ 为赋范空间，$X'$ 为可分空间，则 $X$ 为可分空间

## 一致有界性定理

**一致有界性定理** 设 $X$ 为 Banach 空间，$Y$ 为赋范空间，$(T_i)_{i \in I} \subset B(X, Y)$，若 $\forall x \in X, \sup\limits_{i \in I} \|T_i(x)\| < \infty$，则 $\sup\limits_{i \in I} \|T_i\| < \infty$

## 强收敛与弱收敛

## 开映射定理和闭图像定理

**开映射** $T: X \to Y$ 为开映射，若 $\forall G \subset X$ 为开集，$T(G) = \{T(x): x \in G\}$ 为 $Y$ 的开集

**开映射定理** 设 $X, Y$ 为 Banach 空间，$T \in B(X, Y)$，若 $T$ 为满射，则 $T$ 为开映射。若 $T$ 为双射，则 $T^{-1} \in B(Y, X)$

设 $X$ 为线性空间，$\|\cdot\|_1, \|\cdot\|_2$ 为 $X$ 上的两个范数，且和 $X$ 构成 Banach 空间。若 $\exists \alpha > 0, \|x\|_1 \le \alpha \|x\|_2, \forall x \in X$，则 $\exists \beta > 0, \|x\|_2 \le \beta \|x\|_1, \forall x \in X$，即两个范数等价

**闭算子** $T: D(T) \to Y$ 为闭算子，若 $G_T = \{(x, T(x)): x \in X\}$ 为 $X \times Y$ 的闭集

**闭图像定理** 设 $X, Y$ 为 Banach 空间，$D(T) \subset X$ 为闭线性子空间，$T: D(T) \to Y$ 为闭算子，则 $T$ 为有界线性算子

## 在逼近论中的应用
