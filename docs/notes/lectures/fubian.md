---
comments: true
---

# 复变函数与数理方程

## 复变函数 上

---

### 1 复数和复变函数

---

#### 1.1 复数及运算

- 复数
- 实部、虚部
- 实轴、虚轴
- 三角式、指数式
- 模、辐角
- 主值、主辐角
- 共轭
- 加法、减法、乘法、除法、乘方、开方
- 加法交换律、加法结合律、乘法交换律、乘法结合律、乘法分配律

---

> **注记 1.1** 我们有 $\arg(z_{1} z_{2}) = \arg z_{1} + \arg z_{2}$ ，但 $\arg z^{2} = \arg z + \arg z \neq 2 \arg z$ 。

---

#### 1.2 复变函数及性质

---

- 点集
- 复变函数
- 宗量
- 定义域、区域
- 邻域、内点、外点、边界点、区域、闭区域
- 周期性
  - $\sin z$ 和 $\cos z$ 具有实周期 $2 \pi$
  - $e^{z}$ ， $\mathrm{sh} z$ 和 $\mathrm{ch} z$ 具有纯虚数周期 $2 \pi i$
- 连续

---

> - 在复变函数论中，主要研究的是解析函数。
> - $|\sin z|$ 和 $|\cos z|$ 的平方和可大于 $1$ 。但 $\sin z^{2} + \cos z^{2} = 1$ 仍成立。
> - 将复变函数 $f(z)$ 的实部和虚部分别记为 $u(x,y)$ 和 $v(x,y)$ ， $f(z) = u(x,y) + iv(x,y)$ 。则复变函数可以归结为一对二元实变函数。

---

### 2 解析函数

#### 2.1 复变函数的导数

---

- 可导、导数/微商
- 复变函数的部分性质
  - $\frac{\mathrm{d}}{\mathrm{d} z} (w_{1} + w_{2}) = \frac{\mathrm{d} w_{1}}{\mathrm{d} z} + \frac{\mathrm{d} w_{2}}{\mathrm{d} z}$
  - $\frac{\mathrm{d}}{\mathrm{d} z} (w_{1} w_{2}) = w_{1} \frac{\mathrm{d} w_{2}}{\mathrm{d} z} + w_{2} \frac{\mathrm{d} w_{1}}{\mathrm{d} z}$
  - $\frac{\mathrm{d}}{\mathrm{d} z} \left(\frac{w_{1}}{w_{2}}\right) = \frac{w_{1}' w_{2} - w_{1} w_{2}'}{w_{2}^{2}}$
  - $\frac{\mathrm{d} w}{\mathrm{d} z} = \frac{1}{\frac{\mathrm{d} z}{\mathrm{d} w}}$
  - $\frac{\mathrm{d}}{\mathrm{d} z} F(w) = \frac{\mathrm{d} F}{\mathrm{d} w} \cdot \frac{\mathrm{d} w}{\mathrm{d} z}$
  - $\frac{\mathrm{d}}{\mathrm{d} z} z^{n} = nz^{n-1}$
  - $\frac{\mathrm{d}}{\mathrm{d} z} e^{z} = e^{z}$
  - $\frac{\mathrm{d}}{\mathrm{d} z} \sin z = \cos z$
  - $\frac{\mathrm{d}}{\mathrm{d} z} \cos z = -\sin z$
  - $\frac{\mathrm{d}}{\mathrm{d} z} \ln z = \frac{1}{z}$
- Cauchy-Riemann 方程 / Cauchy-Riemann 条件
  - $\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}$，$\frac{\partial v}{\partial x} = -\frac{\partial u}{\partial y}$

---

> - 形式上看，复变函数和实变函数导数的定义相同，因此在某些方面具有一致性。然而，它们具有本质的区别，因为实变函数只需要沿实轴逼近极限，而复变函数则需要在全方向逼近极限。

---

> **定义 2.1** 设函数 $w = f(z)$ 是在区域 $B$ 上定义的单值函数，即对于 $B$ 上的每一个 $z$ 值，有且只有一个 $w$ 值与之相对应。若在 $B$ 上的某点 $z$，极限
> 
> $$\lim \limits_{\Delta z \to 0} \frac{\Delta w}{\Delta z} = \lim \limits_{\Delta z \to 0} \frac{f(z + \Delta z) - f(z)}{\Delta z}$$
> 
> 存在且与 $\Delta z \to 0$ 的方式无关，则称函数 $w = f(z)$ 在 $z$ 点可导。

---

> **定理2.1** 函数 $f(z) = u + iv$ 可导的充要条件是： $u(x,y)$ 和 $v(x,y)$ 可微，且偏导数满足 C-R 条件。

---

> **注记 2.1** 上述初等函数导数（指复变函数的部分性质）的存在性，既可以用定义证明，也可以用后续的 C-R 条件验证。

---

#### 2.2 解析函数

---

- 解析、解析函数
- 调和函数
  - 若函数 $f(z) = u + iv$ 在区域 $B$ 上解析，则 $u$, $v$ 均为 $B$ 上的调和函数，即： $u$, $v$ 在区域 $B$ 上均有二阶连续偏导数，且满足拉普拉斯方程 $\frac{\partial^{2} u}{\partial x^{2}} + \frac{\partial^{2} u}{\partial y^{2}} = \frac{\partial^{2} v}{\partial x^{2}} + \frac{\partial^{2} v}{\partial y^{2}} = 0$
- 计算 $v = \int \mathrm{d} v$ 的方法：曲线积分法、凑全微分显式法、不定积分法

---

> - 解析函数的实部和虚部不是独立的，知道了其中之一，例如实部 $u$ ，根据 C-R 条件，就可以唯一地（相差一个常数）确定虚部 $v$ ，这是因为$\mathrm{d} v = \frac{\partial v}{\partial x} \mathrm{d} x + \frac{\partial v}{\partial y} \mathrm{d} y = -\frac{\partial u}{\partial y} \mathrm{d} x + \frac{\partial u}{\partial x} \mathrm{d} y$ 。类似的，当虚部 $v$ 确定后，也可以唯一的确定实部 $u$ 。
> - 另外，并不是任意一个二元函数 $u$ 都可以作为解析函数的实部或虚部，它需要是调和函数。

---

> **定义2.2** 若函数 $f(z)$ 在点 $z_{0}$ 及其邻域上处处可导，则称 $f(z)$ 在 $z_{0}$ 点解析。又若 $f(z)$ 在区域 $B$ 上的每一点都解析，则称 $f(z)$ 是区域 $B$ 上的解析函数。

---

> **注记2.2** 根据 C-R 条件，我们直接有
> 
> $$\frac{\partial^{2} u}{\partial x^{2}} + \frac{\partial^{2} u}{\partial y^{2}} = \frac{\partial}{\partial x} \frac{\partial v}{\partial y} - \frac{\partial}{\partial y} \frac{\partial v}{\partial x} = 0$$
> 
> 类似的 $v$ 也满足调和方程。关于函数 $u$, $v$ 的二阶可微性，可以推广到任意阶可微，请参考后续内容（本章推论 3.1）。

---

> **注记2.3** 回顾C-R条件
> 
> $$\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}, \quad \frac{\partial v}{\partial x} = -\frac{\partial u}{\partial y}$$
> 
> 将上面两式相乘，则有
> 
> $$\frac{\partial u}{\partial x} \frac{\partial v}{\partial x} = -\frac{\partial v}{\partial y} \frac{\partial u}{\partial y}$$
> 
> 即梯度 $\nabla u$ 和 $\nabla v$ 正交
> 
> $$\nabla u \cdot \nabla v = 0$$
> 
> 由于 $\nabla u$ 和 $\nabla v$ 分别是曲线簇 $u = C_{1}$ 和 $v = C_{2}$ 的法向矢量，因此可得结论。

---

#### 2.3 多值函数*

---

### 3 复变函数积分

---

#### 3.1 复变函数积分

---

#### 3.2 柯西积分定理

---

#### 3.3 柯西积分公式

---

#### 3.4 积分公式的应用

---

## 复变函数 下

---

### 1 幂级数和泰勒级数

---

#### 1.1 复数项级数

---

- 复数项无穷级数 $\sum_{k=0}^{\infty} w_{k}$ 的收敛性问题可归结为两个实数项级
数 $\sum_{k=0}^{\infty} u_{k}$ 和 $\sum_{k=0}^{\infty} v_{k}$ 的收敛性问题。

---

#### 1.2 幂级数

---

#### 1.3 泰勒级数

---

#### 1.4 解析延拓*

---

### 2 洛朗级数

---

#### 2.1 洛朗级数

---

- 洛朗级数

---

> **定理 2.1** 设 $f(z)$ 在环形区域 $R_{2} < |z - z_{0}| < R_{1}$ 内部单值解析，则对环域上任一点 $z$ ， $f(z)$ 可展为双边幂级数
> 
> $$f(z) = \sum_{k=-\infty}^{\infty} a_{k} (z - z_{0})^{k}$$
> 
> 其中
> 
> $$a_{k} = \frac{1}{2 \pi i} \oint_{l} \frac{f(\zeta)}{(\zeta - z_{0})^{k+1}} \mathrm{d} \zeta$$
> 
> 这里 $l$ 是环域内的绕内圆一周的任意闭合曲线。
> 
> 该定理中 $f(z) = \sum_{k=-\infty}^{\infty} a_{k} (z - z_{0})^{k}$ 称为 $f(z)$ 的洛朗展开，右端的级数称为洛朗级数。

---

> **注记 2.1** 关于洛朗级数，有如下几点说明：
> - 尽管上述级数中含有 $z-z_{0}$ 的负幂项，这些项在 $z=z_{0}$ 时都是奇异的，但点z0可能是也可能不是函数 $f(z)$ 的奇点。
> - 展开系数 $a_{k}$ 的公式与泰勒级数的公式形式相同，但本质不同，因为泰勒级数要求在圆内解析，而洛朗级数不要求。
> - 如果只有环心 $z_{0}$ 是 $f(z)$ 的奇点，则内圆半径可以任意小，同时 $z$ 可以无限地接近 $z_{0}$ 点。这时称上式为 $f(z)$ 在它的孤立奇点 $z_{0}$ 的邻域内的洛朗展开式。
> - 类似于泰勒展开，洛朗展开也是唯一的（证明略）。

---

#### 2.2 孤立奇点的分类

---

> **定义 2.1** 若函数 $f(z)$ 在某点 $z_{0}$ 不可导（不连续、无法定义），而在 $z_{0}$ 的任意小邻域内除 $z_{0}$ 外处处可导。便称 $z_{0}$ 为 $f(z)$ 的孤立奇点。若在 $z_{0}$ 的无论多小的邻域内总可以找到除 $z_{0}$ 以外的不可导点（不连续、无法定义），便称 $z_{0}$ 为 $f(z)$ 的非孤立奇点。

---

> **定义 2.2** 在挖去孤立奇点 $z_{0}$ 而形成的环域（ $0 < |z − z_{0}| < R $ ）上的解析函数f(z)可展为洛朗级数
> 
> $$f(z) = \sum_{k=-\infty}^{\infty} a_{k} (z - z_{0})^{k}$$
> 
> 其中洛朗级数的正幂部分称为解析部分，负幂部分称为主要部分或无限部分。
> 
> 对于负幂项，它有三种情况： (1) 没有负幂项； (2) 有限个负幂项； (3) 无限个负幂项。在这三种情况下，分别将 $z_{0}$ 称为函数 $f(z)$ 的可去奇点、极点及本性奇点。

---

> **注记 2.2** 定义函数
> 
> $$f(z)=\left\{\begin{array}{ll}{\frac{\sin z}{z}} & {z \neq 0} \\ {\lim \limits_{z \to 0} \frac{\sin z}{z} = 1} & {z=0}\end{array}\right.$$
> 
> 则 $f(z)$ 在整个开平面上是解析的，且直接给出 $f(z)$ 在 $z_{0}=0$ 邻域上的展开式
> 
> $$f(z) = 1 - \frac{z^{2}}{3!} + \frac{z^{4}}{5!} - \frac{z^{6}}{7!} + \cdots (|z| < +\infty)$$

---

> **注记 2.3** 根据洛朗展开，如果 $z_{0}$ 是函数 $f(z)$ 的极点，则显然有
> 
> $$\lim \limits_{z \to z_{0}} f(z) = \infty$$

---

> **注记 2.4** 事实上，只要作变换 $\zeta = \frac{1}{z}$ ，将 $z = \infty$ 变换为 $\zeta = 0$ ，从 $\zeta$ 平面的原点来看，这些定义[^1]就都是显然的了。

[^1]: 如果该洛朗级数没有正幂项，无限远点称为 $f(z)$ 的可去奇点；如果只有有限个正幂项，则称为极点，最高幂指数称为极点的阶；如果有无限个正幂项，则称为本性奇点。

---

### 3 留数定理

---

#### 3.1 留数定理

---

> **定义 3.1** 若 $z_{0}$ 是 $f(z)$ 的孤立奇点，即存在 $R > 0$ 使 $f(z)$ 在圆环 $0 < |z − z_{0}| < R $ 内解析，其洛朗展开为
>
> $$f(z) = \sum_{k=-\infty}^{\infty} a_{k} (z - z_{0})^{k}$$
>
> 其中项 $(z - z_{0})^{-1}$ 的系数
>
> $$a_{-1} = \frac{1}{2 \pi i} \oint_{|z - z_{0}| = r} f(z) \mathrm{d} z, 0 < r < R$$
>
> 称为 $f(z)$ 在 $z_{0}$ 点的留数（或残数、英 residue），记为 $\mathrm{Res} f(z_{0})$ 。

---

> **定理 3.1（留数定理）** 设函数 $f(z)$ 在回路 $l$ 所围区域 $B$ 上除有限个孤立奇点 $z_{1}, z_{2}, \cdots, z_{n}$ 外解析，在闭区域 $\bar{B}$ 上除 $z_{1}, z_{2}, \cdots, z_{n}$ 外连续，则
>
> $$\oint_{l} f(z) \mathrm{d} z = 2 \pi i \sum_{k=1}^{n} \mathrm{Res} f(z_{k})$$

---

> **注记 3.1** 留数定理指出了被积函数的回路积分等于该函数所围奇点留数之和。因此，积分问题可以转换为留数求解问题。

---

> **注记 3.2** 一般的，对函数在奇点附近做洛朗展开，即可得到留数，但这样做工作量太大，需要考虑不作洛朗展开直接算出留数的方法。

---

#### 3.2 $\infty$ 点的留数

---

#### 3.3 留数定理的应用

---