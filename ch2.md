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

$$
\begin{array}{c}
   空间的扭曲&\\
   \begin{bmatrix} 
\overgroup{1/30}&\overgroup{0}&\overgroup{0}\\
0&1/20&0\\
\undergroup{0}&\undergroup{0}&\undergroup{1/10}
\end{bmatrix}
\end{array}

\begin{array}{c}
空间扭曲前坐标\\
\begin{bmatrix} 
30\\
20\\
10
\end{bmatrix}
\end{array}
=
\begin{array}{c}
空间扭曲后坐标\\
\begin{bmatrix} 
1\\
1\\
1
\end{bmatrix}
\end{array}
$$

可惜的是文明的本能是会把任何科技作为武器，线性变换引擎也不例外。它可以用来扭曲敌人的宇宙空间，让敌人无法到达目的地。这也是第一章真正主要介绍的内容：计算目的地在扭曲后空间的位置：

$$
空间扭曲A × 扭曲前的坐标c = 扭曲后的坐标z
$$

或是观测到空间扭曲后中的某物体，求它在空间扭曲前的位置：

$$
空间扭曲A × 扭曲前的坐标x = 扭曲后的坐标b
$$

以我们的技术，我们一般有两种方式来解得扭曲前的坐标$x$。第一种是口算，第二种是用我们自己的线性变换引擎把宇宙空间复原成扭曲前的样子：

$$
\begin{aligned}
&反空间扭曲A^{-1} × 空间扭曲A × 扭曲前的坐标x \\
&= 反空间扭曲A^{-1} × 扭曲后的坐标b \\
&= 扭曲前的坐标x
\end{aligned}
$$

没错，现在量产的多维飞船没有线性变换引擎都不好意思跟外星人打招呼。经常可以见到一片宇宙空间被路人们扭曲多次！

$$
真·空间扭曲Z = 第n次空间扭曲N × ... × 第2次空间扭曲B × 第1次空间扭曲A
$$

相信作为舰长的您，也会好奇如何掌握真·空间扭曲Z，并且口算出$真·反空间扭曲Z^{-1}$的吧？

### **矩阵的双重身份**

$$
\begin{aligned}
&\begin{array}{c}
   空间的扭曲&\\
   \begin{bmatrix} 
\overgroup{0.1}&\overgroup{0}\\
\undergroup{0}&\undergroup{0.2}
\end{bmatrix}
\end{array}
×
\begin{array}{c}
空间扭曲前坐标\\
\begin{bmatrix} 
食堂&篮球场&宿舍&烧烤摊\\
30&75&0&120\\
10&89&0&22
\end{bmatrix}
\end{array}
\\
\\
&=
\begin{array}{c}
空间扭曲后坐标\\
\begin{bmatrix} 
食堂&篮球场&宿舍&烧烤摊\\
\overgroup{\undergroup{\begin{bmatrix} 
.1&0\\
0&.2
\end{bmatrix}
\begin{bmatrix} 
30\\
10
\end{bmatrix}}}
&
\overgroup{\undergroup{\begin{bmatrix} 
.1&0\\
0&.2
\end{bmatrix}
\begin{bmatrix} 
75\\
89
\end{bmatrix}}}
&
\overgroup{\undergroup{\begin{bmatrix} 
.1&0\\
0&.2
\end{bmatrix}
\begin{bmatrix} 
0\\
0
\end{bmatrix}}}
&
\overgroup{\undergroup{\begin{bmatrix} 
.1&0\\
0&.2
\end{bmatrix}
\begin{bmatrix} 
120\\
22
\end{bmatrix}}}
\end{bmatrix}
\end{array}
\\
\\
&=
\begin{array}{c}
空间扭曲后坐标\\
\begin{bmatrix} 
食堂&篮球场&宿舍&烧烤摊\\
3&7.5&0&12\\
2&17.8&0&4.4
\end{bmatrix}
\end{array}

\end{aligned}
$$

-----


宇宙的维度与方向 -》 黑洞

multiply
determinant
inverse
column space
null space