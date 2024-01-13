# 内积空间和 Hilbert 空间

## 内积空间

**内积** $\langle \cdot, \cdot \rangle: X^2 \to \mathbb{K}, (x, y) \mapsto \langle x, y \rangle$，若

1. $\langle x + y, z \rangle = \langle x, z \rangle + \langle y, z \rangle$
2. $\langle \alpha x, y \rangle = \alpha \langle x, y \rangle$
3. $\langle x, y \rangle = \overline{\langle y, x \rangle}$
4. $\langle x, x \rangle \ge 0$
5. $\langle x, x \rangle = 0 \iff x = 0$

**内积空间** 序对 $(X, \langle \cdot, \cdot \rangle)$ 为内积空间，其中 $X$ 为线性空间，$\langle \cdot, \cdot \rangle$ 为内积

**诱导范数** $\|x\| = \langle x, x \rangle ^ \frac{1}{2}$

**Hilbert 空间** $X$ 为 Hilbert 空间，若诱导范数使之成为 Banach 空间

**平行四边形恒等式** $\|x + y\|^2 + \|x - y\|^2 = 2 \|x\|^2 + 2 \|y\|^2$

**极化恒等式**

- $\mathbb{K} = \mathbb{R}$ 时，$\langle x, y \rangle = \frac{1}{4} (\|x + y\|^2 - \|x - y\|^2)$
- $\mathbb{K} = \mathbb{C}$ 时，$\langle x, y \rangle = \frac{1}{4} (\|x + y\|^2 - \|x - y\|^2) + \frac{i}{4} (\|x + iy\|^2 - \|x - iy\|^2)$

## 正交补及正交投影

**正交** $x \perp y \iff \langle x, y \rangle = 0$

**正交补** $M^\perp = \{x \in X: \forall y \in M, \langle x, y \rangle = 0\}$

**凸集** $M \subset X$ 为凸集，若 $\forall x, y \in M, \forall \alpha \in [0, 1], \alpha x + (1 - \alpha) y \in M$

设 $X$ 为内积空间，$M$ 为非空凸集，且 $X$ 在 $M$ 上诱导度量使之成为完备空间，则任给 $x_0 \in X, \exist! y_0 \in M, \rho(x_0, M) = \|x_0 - y_0\|$

- 若 $X$ 为 Hilbert 空间，可设 $M$ 为非空凸闭集
- 若 $X$ 为内积空间，可设 $M$ 为完备线性子空间

**直和** $X = M \oplus N \iff X = \operatorname{span}(M \cup N)$ 且 $M \cap N = \{0\}, \forall x \in X, \exists! m \in M, n \in N, x = m + n$

**正交分解定理** 设 $H$ 为 Hilbert 空间，$M$ 为 $H$ 的闭线性子空间，则 $H = M \oplus M^\perp$

**正交投影** $P_M: H \to M$，$x \mapsto y$，$\|x - y\| = \rho(x, M)$

设 $H$ 为 Hilbert 空间，$M$ 为 $H$ 的闭子空间，则

1. $P_M$ 为有界线性算子，且 $\|P_M\| \le 1$
2. $P_M^2 = P_M$
3. $R(P_M) = M, N(P_M) = M^\perp$

设 $H$ 为 Hilbert 空间，$M$ 为 $H$ 的闭子空间，则 $(M^\perp)^\perp = M$

设 $X$ 为内积空间，$M$ 为 $X$ 的非空子集，则 $(\operatorname{span}(M))^\perp = M^\perp = (\overline{M})^\perp$

**完全集** $M \subset X$ 为完全集，若 $\operatorname{span}(M)$ 在赋范空间 $X$ 中稠密

设 $H$ 为 Hilbert 空间，$M$ 为非空子集，则 $M$ 为完全集 $\iff M^\perp = \{0\}$

## 标准正交集与标准正交基

**标准正交集** $M \subset X$ 为标准正交集，若 $M$ 线性无关且 $\forall x, y \in M, \langle x, y \rangle = 0, \|x\| = \|y\| = 1$

**标准正交序列** 若标准正交集为可数集，则称之为标准正交序列

**标准正交组** 若标准正交集为有限集，则称之为标准正交组

**Bessel 不等式** $\sum\limits_{i = 1}^\infty |\langle x, e_i \rangle|^2 \le \|x\|^2$

**标准正交基** $M$ 为标准正交基，若 $M$ 为内积空间 $H$ 的标准正交集且 $\overline{\operatorname{span}(M)} = H$

设 $M$ 为内积空间 $H$ 的标准正交集，则下述命题相互等价

1. $M$ 为 $H$ 的标准正交基
2. $\forall x \in H, x = \sum\limits_{e \in M}^\infty \langle x, e \rangle e$
3. $\forall x, y \in H, \langle x, y \rangle = \sum\limits_{e \in M}^\infty \langle x, e \rangle \langle e, y \rangle$
4. $\forall x \in H, \|x\|^2 = \sum\limits_{e \in M}^\infty |\langle x, e \rangle|^2$（Parseval 等式）

**Gram-Schmidt 标准正交化方法** 设 $\{x_1, x_2, \cdots\}$ 为内积空间 $X$ 的一列线性无关元素，则存在 $\{e_1, 2_2, \cdots\}$ 为标准正交序列，使得任给 $n \ge 1$，有 $\operatorname{span}(x_1, x_2, \cdots, x_n) = \operatorname{span}(e_1, e_2, \cdots, e_n)$

## Hilbert 空间上有界线性泛函的表示

**Riesz 表示定理** 若 $H$ 为 Hilbert 空间，则任取 $f \in H'$，$\exist! y \in H, \forall x \in H, f(x) = \langle x, y \rangle$

**共轭双线性泛函** $h: X \times Y \to \mathbb{K}$，若

1. $h(x_1 + x_2, y) = h(x_1, y) + h(x_2, y)$
2. $\forall \alpha \in \mathbb{K}, h(\alpha x, y) = \alpha h(x, y)$
3. $h(x, y_1 + y_2) = h(x, y_1) + h(x, y_2)$
4. $\forall \alpha \in \mathbb{K}, h(x, \alpha y) = \overline{\alpha} h(x, y)$

**共轭双线性泛函的范数** $\|h\| = \sup\limits_{x \ne 0, y \ne 0} \frac{|h(x, y)|}{\|x\| \|y\|}$

**Riesz 定理** 设 $H_1, H_2$ 为 Hilbert 空间，$h : H_1 \times H_2 \to \mathbb{K}$ 为有界共轭双线性泛函，则存在唯一的 $T \in B(H_1, H_2)$，使得 $\forall x \in H_1, y \in H_2, h(x, y) = \langle T(x), y \rangle$，此时 $\|T\| = \|h\|$

**伴随算子** $T^*: H_2 \to H_1$，$y \mapsto x$，$\forall x \in H_1, y \in H_2, \langle T(x), y \rangle = \langle x, T^*(y) \rangle$

**伴随算子的性质** 设 $H_1, H_2$ 为 Hilbert 空间，$S， T \in B(H_1, H_2)$，$\alpha \in \mathbb{K}$，则

1. $(S + T)^* = S^* + T^*$
2. $(\alpha S)^* = \overline{\alpha} S^*$
3. $(T^*)^* = T$
4. $\|T^* T\| = \|T T^*\| = \|T\|^2$
5. $T^* T = 0 \iff T = 0$
6. 若 $H_3$ 为 Hilbert 空间，$P \in B(H_2, H_3)$，则 $(PT)^* = T^* P^*$
