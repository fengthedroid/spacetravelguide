## 多维飞船CH 2. 矩阵宇宙

蓝色药丸您已经服下了？现在起就让我们进入矩阵宇宙（The matrix）吧。那个，并没有进错片场啦。上一章讲飞船发动机什么的都是骗你的。毕竟您也会疑惑，如果发动机配置有异常，怎么不修理呢是不是？

现实是，飞船的发动机没有错。错的是我们总是在扭曲的宇宙中航行！三体人最开始发明线性变换引擎只是为了更快地太空旅行。回顾太空旅行的基本公式：

$$Ax=b$$

试想在3维宇宙中我们有这样的发动机组：

$$
\begin{bmatrix}
engine1&engine2&engine3\\ 
\overgroup{1}&\overgroup{0}&\overgroup{0}\\
0&1&0\\
\undergroup{0}&\undergroup{0}&\undergroup{1}
\end{bmatrix}
$$

要从$\begin{bmatrix}0\\0\\0\end{bmatrix}$去往$\begin{bmatrix}30\\20\\10\end{bmatrix}$我们就必须实实在在地在第一维度上走30步，第二维度走20步，第三维度走10步。如果我们有能力改变宇宙空间的形状，把$\begin{bmatrix}30\\20\\10\end{bmatrix}$拉近到$\begin{bmatrix}1\\1\\1\end{bmatrix}$，那我们就不用浪费太多时间在太空旅行上了！

线性变换引擎就是用来改变宇宙的形状的：

$$\begin{bmatrix} 
扭~曲&空~间&的~状~态\\
\overgroup{1/30}&\overgroup{0}&\overgroup{0}\\
0&1/20&0\\
\undergroup{0}&\undergroup{0}&\undergroup{1/10}
\end{bmatrix}

\begin{bmatrix} 
空间扭曲前坐标\\
30\\
20\\
10
\end{bmatrix}
=
\begin{bmatrix} 
空间扭曲后坐标\\
1\\
1\\
1
\end{bmatrix}
$$

可惜的是三体人发觉线性变换引擎也可以作为可怕的武器使用。首先是扭曲敌人的宇宙，让敌人无法到达目的地。这也是第一章主要介绍的内容：计算目的地在扭曲后宇宙的位置：

$$
扭曲宇宙状态A × 扭曲前的坐标c = 扭曲后的坐标z
$$

或是观测到扭曲后宇宙中的某物体，求它在扭曲宇宙前的位置：

$$
扭曲宇宙状态A × 扭曲前的坐标x = 扭曲后的坐标b
$$

以我们的技术，我们一般有两种方式来解得扭曲前得坐标x。第一种是口算，第二种是用我们自己的线性变换引擎把宇宙复原成扭曲前的样子：

$$
反扭曲宇宙状态A^{-1} × 扭曲宇宙状态A × 扭曲前的坐标x \newline
= 反扭曲宇宙状态A^{-1} × 扭曲后的坐标b \newline
= 扭曲前的坐标x
$$