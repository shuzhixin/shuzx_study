# Typora-Markdown编辑数学公式

### 1. 插入公式

#### 1.1 行内公式

行内公式（行内与其它文字混编）可以用如下方法表示：`$ 数学公式 $` 。

为使用该功能，需先通过`偏好设置`->`Markdown`->`Markdown扩展语法`，勾选`内联公式`、`上标`、`下标`等，然后重启[Typora](https://so.csdn.net/so/search?q=Typora&spm=1001.2101.3001.7020)。

示例 \$ x^2 + y^2 = 1\$，即 $ x^2 + y^2 = 1$

示例 \$\lim_{x \to \infty} \exp(-x) = 0\$ ，即 
$$
\lim_{x \to \infty} \exp(-x) = 0
$$


#### 1.2 行间公式

独立公式可以用如下方法表示：`$$ 数学公式 $$`
$$
arg\ min_{x_{i,j}}\ \frac{1}{2}\ \sum_{i=1}^{m}\sum_{j=1}^{n}\begin{Vmatrix} z_{i,j} - h(x_{i,j})\end{Vmatrix}^2
$$


### 2. 常用的数学符号

数学公式中的一些常用的字符:

| **字母** | **实现** |    字母    | **实现** |    字母    | **实现** |    字母    | **实现** |
| :------: | :------: | :--------: | :------: | :--------: | :------: | :--------: | :------: |
| $\alpha$ |  \alpha  |  $\beta$   |  \beta   |  $\Gamma$  |  \Gamma  |  $\gamma$  |  \gamma  |
| $\Delta$ |  \Delta  |  $\delta$  |  \delta  |    $E$     |    E     | $\epsilon$ | \epsilon |
|   $Z$    |    Z     |  $\zeta$   |  \zeta   |    $H$     |    H     |   $\eta$   |   \eta   |
| $\Theta$ |  \Theta  |  $\theta$  |  \theta  |    $I$     |    I     |  $\iota$   |  \iota   |
|   $K$    |    K     |  $\kappa$  |  \kappa  | $\Lambda$  | \Lambda  | $\lambda$  | \lambda  |
|   $M$    |    M     |   $\mu$    |   \mu    |   $\nu$    |   \nu    |   $\Xi$    |   \Xi    |
|  $\xi$   |   \xi    | $\omicron$ | \omicron |   $\Pi$    |   \Pi    |   $\pi$    |   \pi    |
|   $P$    |    P     |   $\rho$   |   \rho   |  $\Sigma$  |  \Sigma  |  $\sigma$  |  \sigma  |
|  $\tau$  |   \tau   |   $\chi$   |   \chi   | $\Upsilon$ | \Upsilon | $\upsilon$ | \upsilon |
|  $\Phi$  |   \Phi   |   $\phi$   |   \phi   |   $\Psi$   |   \Psi   |   $\psi$   |   \psi   |
| $\Omega$ |  \Omega  |  $\omega$  |  \omega  |    $A$     |    A     |    $B$     |    B     |



### 3. 常用数学表达式

()、[]和|表示符号本身，使用 {} 来表示 {}。当要显示大号的括号或分隔符时，要用 \left 和 \right 命令。
$$
c(n) =
    \begin{cases}
      \sqrt{2n},  & \text{n = 0} \\
      \sqrt{\frac{1}{n}}, & n\neq 0
    \end{cases}
    \tag{12.1}
$$

| 输入                     | 显示                   | 说明             | 输入                      | 显示                    | 说明             |
| ------------------------ | ---------------------- | ---------------- | ------------------------- | ----------------------- | ---------------- |
| \$x^2\$                  | $x^2$                  | 上标             | \$x_1\$                   | $x_1$                   | 下标             |
| \$\sqrt{2}\$             | $\sqrt{2}$             | 平方根           | \$\sqrt[n]{2}\$           | $\sqrt[n]{2}$           | 开方             |
| \$\log_28\$              | $\log_28$              | 对数             | \$lg18\$                  | $lg18$                  | 对数             |
| \$ln18\$                 | $ln18$                 | 对数             | \$a^\hat{}\$              | $a^\hat{}$              | 反对称矩阵       |
| \$\frac{x}{y}\$          | $\frac{x}{y}$          | 分数             | \$\vec{a}\$               | $\vec{a}$               | 矢量             |
| \$\overleftarrow{x}\$    | $\overleftarrow{x}$    | 上方左箭头       | \$\overrightarrow{x}\$    | $\overrightarrow{x}$    | 上方右箭头       |
| \$\sin\$                 | $\sin$                 | 正弦             | \$\cos\$                  | $\cos$                  | 余弦             |
| \$\tan\$                 | $\tan$                 | 正切             | \$\cot\$                  | $\cot$                  | 余切             |
| \$\sum{a}\$              | $\sum{a}$              | 累加             | \$\sum_{n-1}^{100}{a_n}\$ | $\sum_{n-1}^{100}{a_n}$ | 累加             |
| \$\prod{x}\$             | $\prod{x}$             | 累乘             | \$\prod_{n=1}^{99}{x_n}\$ | $\prod_{n=1}^{99}{x_n}$ | 累乘             |
| \$A \bigcup B\$          | $A \bigcup B$          | 并集             | \$A \bigcap B\$           | $A \bigcap B$           | 交集             |
| \$\langle表达式\rangle\$ | $\langle表达式\rangle$ | 尖括号           | \$\lbrace表达式\rbrace$   | $\lbrace表达式\rbrace$  | 大括号           |
| \$\lfloor表达式\rfloor\$ | $\lfloor表达式\rfloor$ | 取底符号         | \$\lceil表达式\rceil\$    | $\lceil表达式\rceil$    | 取顶符号         |
| \$\ldots\$               | $\ldots$               | 与底线对齐省略号 | \$\cdots\$                | $\cdots$                | 与中线对齐省略号 |

### 4. 常用关系运算符

| 输入         | 显示       | 输入           | 显示         |
| ------------ | ---------- | -------------- | ------------ |
| \$\pm\$      | $\pm$      | \$\times\$     | $\times$     |
| \$\cdot\$    | $\cdot$    | \$\ast\$       | $\ast$       |
| \$\div\$     | $\div$     | \$\triangleq\$ | $\triangleq$ |
| \$\neq\$     | $\neq$     | \$\equiv\$     | $\equiv$     |
| \$\leq\$     | $\leq$     | \$\geq\$       | $\geq$       |
| \$\approx\$  | $\approx$  | \$\bigotimes\$ | $\bigotimes$ |
| \$\bigodot\$ | $\bigodot$ | \$\bigoplus\$  | $\bigoplus$  |
| \$\mid\$     | $\mid$     | \$\circ\$      | $\circ$      |

### 5. 集合运算符号

| 输入              | 显示            | 输入              | 显示            |
| ----------------- | --------------- | ----------------- | --------------- |
| \$a\in A\$        | $a\in A$        | \$a\notin A\$     | $a\notin A$     |
| \$A\subset B\$    | $A\subset B$    | \$A\supset B\$    | $A\supset B$    |
| \$A\subseteq B\$  | $A\subseteq B$  | \$A\supseteq B\$  | $A\supseteq B$  |
| \$A \bigcup B\$   | $A \bigcup B$   | \$A \bigcap B\$   | $A \bigcap B$   |
| \$A \bigvee B\$   | $A \bigvee B$   | \$A \bigwedge B\$ | $A \bigwedge B$ |
| \$A \biguplus B\$ | $A \biguplus B$ | \$A \bigsqcup B\$ | $A \bigsqcup B$ |
| \$\emptyset\$     | $\emptyset$     |                   |                 |

### 6. 微积分运算符

| 输入              | 显示            | 输入                                          | 显示                                        |
| ----------------- | --------------- | --------------------------------------------- | ------------------------------------------- |
| \$\lim{a+b}\$     | $\lim{a+b}$     | \$\lim_{x\rightarrow+\infty}{\frac{x}{x+1}}\$ | $\lim_{x\rightarrow+\infty}{\frac{x}{x+1}}$ |
| \$\int{x}dx\$     | $\int{x}dx$     | \$\int_{1}^{2}{x}dx\$                         | $\int_{1}^{2}{x}dx$                         |
| \$\iint{xy}dxdy\$ | $\iint{xy}dxdy$ | \$\iiint{xyz}dxdydz\$                         | $\iiint{xyz}dxdydz$                         |
| \$\oint xdx\$     | $\oint xdx$     | \$\nabla\$                                    | $\nabla$                                    |
| \$\infty\$        | $\infty$        | \$\partial x\$                                | $\partial x$                                |
| \$\mathrm{d}x\$   | $\mathrm{d}x$   | \$\dot x\$                                    | $\dot x$                                    |
| \$\ddot x\$       | $\ddot x$       | \$\prime\$                                    | $\prime$                                    |

### 7. 带帽符号

| 输入                | 显示              | 输入              | 显示            |
| ------------------- | ----------------- | ----------------- | --------------- |
| \$\hat{x}\$         | $\hat{x}$         | \$\check{x}\$     | $\check{x}$     |
| \$\bar{y}\$         | $\bar{y}$         | \$\tilde{y}\$     | $\tilde{y}$     |
| \$\widetilde{xyz}\$ | $\widetilde{xyz}$ | \$\widehat{xyz}\$ | $\widehat{xyz}$ |
| \$\breve{y}\$       | $\breve{y}$       | \$\acute{y}\$     | $\acute{y}$     |
| \$\grave{y}\$       | $\grave{y}$       |                   |                 |

### 8. 箭头符号

| 输入                | 显示              | 输入               | 显示             |
| ------------------- | ----------------- | ------------------ | ---------------- |
| \$\uparrow\$        | $\uparrow$        | \$\downarrow\$     | $\downarrow$     |
| \$\Uparrow\$        | $\Uparrow$        | \$\Downarrow\$     | $\Downarrow$     |
| \$\rightarrow\$     | $\rightarrow$     | \$\leftarrow\$     | $\leftarrow$     |
| \$\Rightarrow\$     | $\Rightarrow$     | \$\Leftarrow\$     | $\Leftarrow$     |
| \$\longrightarrow\$ | $\longrightarrow$ | \$\longleftarrow\$ | $\longleftarrow$ |
| \$\Longrightarrow\$ | $\Longrightarrow$ | \$\Longleftarrow\$ | $\Longleftarrow$ |

### 9. 连线符号

| 输入                                             | 显示                                           | 输入                                               | 显示                                             |
| ------------------------------------------------ | ---------------------------------------------- | -------------------------------------------------- | ------------------------------------------------ |
| \$\overline{a+b+c+d}\$                           | $\overline{a+b+c+d}$                           | \$\underline{a+b+c+d}\$                            | $\underline{a+b+c+d}$                            |
| \$\fbox{a+b+c+d}\$                               | $\fbox{a+b+c+d}$                               | \$\overleftarrow{a+b+c+d}\$                        | $\overleftarrow{a+b+c+d}$                        |
| \$\overrightarrow{a+b+c+d}\$                     | $\overrightarrow{a+b+c+d}$                     | \$\overleftrightarrow{a+b+c+d}\$                   | $\overleftrightarrow{a+b+c+d}$                   |
| \$\underleftarrow{a+b+c+d}\$                     | $\underleftarrow{a+b+c+d}$                     | \$\underrightarrow{a+b+c+d}\$                      | $\underrightarrow{a+b+c+d}$                      |
| \$\underleftrightarrow{a+b+c+d}\$                | $\underleftrightarrow{a+b+c+d}$                | \$\overbrace{a+b+c+d}^{Sample}\$                   | $\overbrace{a+b+c+d}^{Sample}$                   |
| \$\underbrace{a+b+c+d}_{Sample}\$                | $\underbrace{a+b+c+d}_{Sample}$                | \$\underbrace{a\cdot a\cdots a}_{b\text{ times}}\$ | $\underbrace{a\cdot a\cdots a}_{b\text{ times}}$ |
| \$\overbrace{a+\underbrace{b+c}_{1.0}+d}^{2.0}\$ | $\overbrace{a+\underbrace{b+c}_{1.0}+d}^{2.0}$ |                                                    |                                                  |

### 10. 其他特殊符号

| 输入              | 显示        | 输入            | 显示           |
| ----------------- | ----------- | --------------- | -------------- |
| \$\forall\$       | $\forall$   | \$\bot\$        | $\bot$         |
| \$\emptyset\$     | $\emptyset$ | \$\exists\$     | $\exists$      |
| \$\angle\$        | $\angle$    | \$30^\circ\$    | $30^\circ$     |
| \$\because\$      | $\because$  | \$\therefore\$  | $\therefore$   |
| \$not>\$          | $not>$      | \$not=\$        | $not=$         |
| 1\$\quad\$1  空格 | $1\quad1$   | 1\$\kern xpt\$1 | 1$\kern 50pt$1 |

### 11. 阵列

**语法：** `$$\begin{array}…\end{array}$$`，`r`[右对齐](https://so.csdn.net/so/search?q=右对齐&spm=1001.2101.3001.7020)，`l`左对齐，`c`居中，`|`垂直线，`\hline`横线，`\\`换行，元素之间以`&`间隔。

**exp.**

```
$$
  \begin{array}{c|lcr}
    n & \text{Left} & \text{Center} & \text{Right} \\
    \hline
    1 & 0.24 & 1 & 125 \\
    2 & -1 & 189 & -8 \\
    3 & -20 & 2000 & 1+10i
  \end{array}
$$

```


$$
\begin{array}{c|lcr}
    n & \text{Left} & \text{Center} & \text{Right} \\
    \hline
    1 & 0.24 & 1 & 125 \\
    2 & -1 & 189 & -8 \\
    3 & -20 & 2000 & 1+10i
  \end{array}
$$


### 12. 矩阵

**语法：** `$$\begin{matrix}…\end{matrix}$$`，每行以`\\`结尾，元素之间以`&`间隔。

exp.

```
$$
  \begin{matrix}
    1 & x & x^2 \\
    1 & y & y^2 \\
    1 & z & z^2 \\
  \end{matrix}
$$

```


$$
  \begin{matrix}
    1 & x & x^2 \\
    1 & y & y^2 \\
    1 & z & z^2 \\
  \end{matrix}
$$
**添加括号：**

- `pmatrix`()
- `bmatrix`[ ]
- `Bmatrix`{ }
- `vmatrix`| |
- `Vmatrix`‖ ‖

**添加省略号：**

```
$$
    \begin{pmatrix}
      1 & a_1^2 & a_1^2 & \cdots & a_1^2 \\
      1 & a_2^2 & a_2^2 & \cdots & a_2^2 \\
      \vdots & \vdots & \vdots & \ddots & \vdots \\
      1 & a_n^2 & a_n^2 & \cdots & a_n^2 \\
    \end{pmatrix}
$$

```

$$
    \begin{pmatrix}
      1 & a_1^2 & a_1^2 & \cdots & a_1^2 \\
      1 & a_2^2 & a_2^2 & \cdots & a_2^2 \\
      \vdots & \vdots & \vdots & \ddots & \vdots \\
      1 & a_n^2 & a_n^2 & \cdots & a_n^2 \\
    \end{pmatrix}
$$

**水平增广矩阵：** 使用阵列语法，

```
$$ 
  \left[
    \begin{array}{cc|c}
      1&2&3\\
      4&5&6
    \end{array}
  \right] 
$$

```

$$
  \left[
    \begin{array}{cc|c}
      1&2&3\\
      4&5&6
    \end{array}
  \right] 
$$

**垂直增广矩阵：**

```
$$
  \begin{pmatrix}
    a & b\\
    c & d\\
    \hline
    1 & 0\\
    0 & 1
  \end{pmatrix}
$$

```

$$
  \begin{pmatrix}
    a & b\\
    c & d\\
    \hline
    1 & 0\\
    0 & 1
  \end{pmatrix}
$$

**在行内插入矩阵：**

exp:

\$ \big ( \begin{smallmatrix} a & b \\\\ c& d \end{smallmatrix}   \big) \$ 

$ \big ( \begin{smallmatrix} a & b \\ c& d \end{smallmatrix}   \big)  $

### 13. 等式对齐

**语法：** `\begin{align}…\end{align}`，每行以`\\`结尾，元素之间以`&`间隔。

**示例：**

```
$$
  \begin{align}
    \sqrt{37} & = \sqrt{\frac{73^2-1}{12^2}} \\
     & = \sqrt{\frac{73^2}{12^2}\cdot\frac{73^2-1}{73^2}} \\ 
     & = \sqrt{\frac{73^2}{12^2}}\sqrt{\frac{73^2-1}{73^2}} \\
     & = \frac{73}{12}\sqrt{1 - \frac{1}{73^2}} \\ 
     & \approx \frac{73}{12}\left(1 - \frac{1}{2\cdot73^2}\right)
  \end{align}
$$
```

$$
  \begin{align}
    \sqrt{37} & = \sqrt{\frac{73^2-1}{12^2}} \\
     & = \sqrt{\frac{73^2}{12^2}\cdot\frac{73^2-1}{73^2}} \\ 
     & = \sqrt{\frac{73^2}{12^2}}\sqrt{\frac{73^2-1}{73^2}} \\
     & = \frac{73}{12}\sqrt{1 - \frac{1}{73^2}} \\ 
     & \approx \frac{73}{12}\left(1 - \frac{1}{2\cdot73^2}\right)
  \end{align}
$$



### 14. 分段函数

**语法：** `\begin{cases}…\end{cases}`，每行以`\\`结尾，元素之间以`&`间隔。使用 `\text{注释内容}`添加注释，使用 `\tag{公式序号}`添加序号

exp.

```
$$
  f(n) =
    \begin{cases}
      n/2,  & \text{if $n$ is even} \\
      3n+1, & \text{if $n$ is odd}
    \end{cases}
    \tag{12.1}
$$
```

$$
  f(n) =
    \begin{cases}
      n/2,  & \text{if $n$ is even} \\
      3n+1, & \text{if $n$ is odd}
    \end{cases}
    \tag{12.1}
$$

```
$$  
  \left.
    \begin{array}{l}
    \text{if $n$ is even:}&n/2\\
    \text{if $n$ is odd:}&3n+1
    \end{array}
  \right\}
  =f(n)
$$

```

$$
  \left.
    \begin{array}{l}
    \text{if $n$ is even:}&n/2\\
    \text{if $n$ is odd:}&3n+1
    \end{array}
  \right\}
  =f(n)
$$



### 15. 符号加粗

```
数字加粗
希腊字母加粗
斜体加粗
```

| 输入                   | 显示                 | 输入                  | 显示                |
| ---------------------- | -------------------- | --------------------- | ------------------- |
| \$\mathbf{3.1415926}\$ | $\mathbf{3.1415926}$ | \$\pmb{\alpha\beta}\$ | $\pmb{\alpha\beta}$ |
| \$\boldsymbol{ab}\$    | $\boldsymbol{ab}$    |                       |                     |



### 16. 常用的快捷键

- 加粗 `Cmd + B`
- 斜体 ``Cmd + I`
- 引用 ``Cmd + Q`
- 插入链接 ``Cmd + L`
- 插入代码 ``Cmd + K`
- 插入图片 ``Cmd + G`
- 提升标题 ``Cmd + H`
- 有序列表 ``Cmd + O`
- 无序列表 ``Cmd + U`
- 横线 ``Cmd + R`
- 撤销 ``Cmd + Z`
- 重做 ``Cmd + Y`