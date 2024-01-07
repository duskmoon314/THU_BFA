# 度量空间

## 1. 度量空间的定义及例子

**度量** d 为 $ X \times X \to \mathbb{R} $ 的函数，满足：

1. 非负性 $\forall x, y \in X, d(x, y) \geq 0$
2. 非退化性 $\forall x, y \in X, d(x, y) = 0 \iff x = y$
3. 对称性 $\forall x, y \in X, d(x, y) = d(y, x)$
4. 三角不等式 $\forall x, y, z \in X, d(x, z) \leq d(x, y) + d(y, z)$

**度量空间** $ (X, d) $ 是一个集合 $ X $ 和一个度量 $ d $ 的序对

## 2. 开集和闭集

**开球** $B(x_0, r) = \{ x \in X \mid d(x, x_0) < r \}$

**闭球** $\overline{B}(x_0, r) = \{ x \in X \mid d(x, x_0) \leq r \}$

**球面** $S(x_0, r) = \{ x \in X \mid d(x, x_0) = r \}$

**内点** $ x_0 \in X $ 是开集 $ U \subset X $ 的内点，如果存在 $ r > 0 $ 使得 $ B(x_0, r) \subset U $

**内部** $U^\circ = \{ x \in U \mid x \text{ 是 } U \text{ 的内点} \}$

**开集** $ U \subset X $ 是开集，如果 $ U = U^\circ $

**闭集** $ F \subset X $ 是闭集，如果 $ F^c = X \setminus F $ 是开集

**开集的性质**

1. $ \varnothing, X $ 是开集
2. 任意多个开集的并是开集
3. 有限多个开集的交是开集

**闭集的性质**

1. $ \varnothing, X $ 是闭集
2. 任意多个闭集的交是闭集
3. 有限多个闭集的并是闭集

**聚点** $ x_0 \in X $ 是集合 $ A \subset X $ 的聚点，如果 $ \forall r > 0, (B(x_0, r) \setminus {x_0}) \cap A \neq \varnothing $

**导集** $ A' = \{ x \in X \mid x \text{ 是 } A \text{ 的聚点} \} $

**闭包** $ \overline{A} = A \cup A' $

$ (X, d) $ 是度量空间，$ M \subset X $，则 $ \overline{M} $ 为闭集，且 $ \overline{M} $ 是包含 $ M $ 的最小闭集

$ (X, d) $ 是度量空间，$ M \subset X $，则 $ M $ 是闭集 $ \iff M = \overline{M} $

**连续映射** $ T: X_1 \to X_2 $ 是连续映射，如果 $ \forall x_0 \in X_1, \forall \varepsilon > 0, \exists \delta > 0, \forall x \in X_1, d_1(x, x_0) < \delta \implies d_2(T(x), T(x_0)) < \varepsilon $

$ (X_1, d), (X_2, d) $ 是度量空间，$ T: X_1 \to X_2 $ 是连续映射 $ \iff \forall U \subset X_2 $ 是开集，$ T^{-1}(U) $ 是开集

$ (X_1, d), (X_2, d) $ 是度量空间，$ T: X_1 \to X_2 $ 是连续映射 $ \iff \forall F \subset X_2 $ 是闭集，$ T^{-1}(F) $ 是闭集

**稠密** $ M \subset X $ 是稠密的，如果 $ \overline{M} = X $

**可分** $ X $ 是可分的，如果有至多可数的稠密子集

$(X, d)$ 是可分的，$Y \subset X$，则 $(Y, d \mid\_{Y \times Y})$ 是可分的

## 3. 收敛性、完备性及紧性

**收敛** $\{x_n\}$ 在 $X$ 中收敛，若 $\exists x \in X, \lim\limits_{n \to \infty} d(x_n, x) = 0$，记为 $x_n \to x$

$(X, d)$ 为度量空间，$M \subset X$，则

1. $x \in \overline{M} \iff \exists \{x_n\} \subset M, x_n \to x$
2. $M$ 是闭集 $\iff \forall \{x_n\} \subset M, x_n \to x \implies x \in M$

**柯西列** $\{x_n\}$ 是柯西列，如果 $\forall \varepsilon > 0, \exists N \in \mathbb{N}, \forall m, n \geq N, d(x_m, x_n) < \varepsilon$

**完备** $X$ 是完备的，如果 $X$ 中的任意柯西列都收敛

$(X, d)$ 是完备的，$Y \subset X$，$(Y, d \mid_{Y \times Y})$ 是完备子空间，则 $Y$ 是闭集

$(X, d)$ 完备，$Y \subset X$，$Y$ 是闭集 $\iff (Y, d \mid_{Y \times Y})$ 完备

**等价度量** $d_1, d_2$ 是等价度量，如果 $\exists c_1, c_2 > 0, \forall x, y \in X, c_1 d_1(x, y) \leq d_2(x, y) \leq c_2 d_1(x, y)$

**紧度量空间** $X$ 是紧的，如果 $X$ 中的任意序列都有收敛子列

**紧集** $M \subset X$ 是紧集，如果 $(M, d \mid_{M \times M})$ 是紧度量空间

**相对紧集** $M \subset X$ 是相对紧集，如果 $\forall x_n \in M, \exists x_{n_k} \subset M, x_{n_k} \to x \in X$

**$\epsilon$-网** $N \subset M$ 是 $\epsilon$-网，如果 $M \subset \bigcup\limits_{x \in N} B(x, \epsilon)$

**完全有界集** $M \subset X$ 是完全有界集，如果 $\forall \epsilon > 0$，都有有限个 $\epsilon$-网

度量空间中的紧集必为有界闭集

$(X, d)$ 为紧度量空间，则 $Y \subset X$ 是紧集 $\iff Y$ 是闭集

$(X, d), M \subset X$ 为相对紧集 $\iff \overline{M}$ 是紧集

$(X, d), M \subset X$ 为完全有界集 $\iff M$ 中的任意序列都有柯西子列

$(X, d), M \subset X$，

1. 若 $M$ 为相对紧集，则 $M$ 为完全有界集
2. 若 $(X, d)$ 完备，则 $M$ 为完全有界集 $\iff M$ 为相对紧集
3. $M$ 为紧集 $\iff M$ 完备且 $M$ 为完全有界集

**最佳逼近元** $y_0$ 为 $x_0$ 在 $M$ 中的最佳逼近元，如果 $d(x_0, y_0) = \rho(x_0, M) = \inf\limits_{y \in M} d(x_0, y)$

## 4. Banach 不动点定理及其应用

**压缩映射** $T: X \to X$ 是压缩映射，如果 $\exists 0 \leq k < 1, \forall x_1, x_2 \in X, d(T(x_1), T(x_2)) \leq k d(x_1, x_2)$

**Banach 不动点定理** $X$ 是完备度量空间，$T: X \to X$ 是压缩映射，则 $T$ 有唯一的不动点 $x_0$，且 $x_0 = \lim\limits_{n \to \infty} T^n(x)$，其中 $T^n(x) = T(T(\cdots T(x)))$

$(X, d)$ 是非空完备度量空间，$T: X \to X$ 是压缩映射，设存在 $m \geq 1$，使得 $T^m$ 为压缩映射，则 $T$ 有唯一的不动点
