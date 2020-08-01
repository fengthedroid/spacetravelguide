## 多维飞船CH 2. 矩阵宇宙

蓝色药丸您已经服下了？现在起就让我们进入矩阵宇宙（The Matrix）吧。那个，并没有进错片场啦。上一章讲飞船发动机什么的都是骗你的。毕竟您也会疑惑，如果发动机配置有异常，怎么不修理呢是不是？

### <span style="color:#6c9ef0" /> **Welcome Onboard For Real, Captain**

现实是，飞船的发动机没有错。错的是我们总是在扭曲的宇宙中航行！三体人最开始发明线性变换引擎只是为了更快地太空旅行。试想在3维宇宙中我们有这样的发动机组：

$$
\begin{bmatrix}
engine1&engine2&engine3\\ 
\overgroup{1}&\overgroup{0}&\overgroup{0}\\
0&1&0\\
\undergroup{0}&\undergroup{0}&\undergroup{1}
\end{bmatrix}
$$

要从原点$\begin{bmatrix}0\\0\\0\end{bmatrix}$去往宇宙尽头的烧烤摊$\begin{bmatrix}30\\20\\10\end{bmatrix}$,我们就必须实实在在地在第一维度上走30步，第二维度走20步，第三维度走10步。如果我们有能力改变宇宙空间的形状，把$\begin{bmatrix}30\\20\\10\end{bmatrix}$拉近到$\begin{bmatrix}1\\1\\1\end{bmatrix}$，那我们就不用浪费太多时间在太空旅行上了！

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
\begin{aligned}
真·空间扭曲Z = &第n次空间扭曲N × ... \\
&× 第2次空间扭曲B \\
&× 第1次空间扭曲A
\end{aligned}
$$

相信作为舰长的您，也会好奇如何掌握真·空间扭曲Z，并且口算出$真·反空间扭曲Z^{-1}$的吧？为此，咱们就要再深聊聊宇宙。

### <span style="color:#6c9ef0"/> **A Cartographer of Space 太空地图师**

假设我们把地球和月球之间的空间延展10倍。从地球看，月球就会变小很多。但是我们并不知道是月球缩小了还是远了。如果我们正好在地球和月球之间放了一把尺子，就会发现这把尺子被放大了10倍。尺子上的1米刻度实际上有10米长。

尺子提供了用来度量1维空间的单位。在高于1维的空间中，我们用的是坐标系来作为度量长度以及方向的单位。当某片不包含任何可观测物的太空被空间扭曲时，虽然我们看不到扭曲的效果，但是我们可以把空间扭曲反映在测量此空间的坐标系上。

在2维空间中，标准坐标系是：

$$
\begin{bmatrix}
\overgroup{1}&\overgroup{0}\\
\undergroup{0}&\undergroup{1}
\end{bmatrix}
$$


三体人的探测器💧在摧毁人类舰队的时候，大家注意到了它可以做到速度不变的转向。在这里提起，应该不难想到它也装备了线性变换引擎吧。若是要做到在2维空间内180度掉头并保留动量，只需将前方的空间扭曲为：

$$
\begin{aligned}
&\begin{array}{c}
   从原空间线性变换到新空间&\\
   \begin{bmatrix} 
   原空间的第一维度的新方向&原空间的第二维度的新方向\\
\overgroup{-1}&\overgroup{0}\\
\undergroup{0}&\undergroup{-1}
\end{bmatrix}
\end{array}
\\
\\
×
&\begin{array}{c}
原速度向量\\
\begin{bmatrix} 
第一维度上的速度&30\\
第二维度上的速度&10
\end{bmatrix}
\end{array}
\\
\\
=
&\begin{array}{c}
新速度向量\\
\begin{bmatrix} 
第一维度上的速度&-30\\
第二维度上的速度&-10
\end{bmatrix}
\end{array}


\end{aligned}
$$



-----
在未被扭曲过的3维宇宙中，光可以自由地在任一一个维度上以标准光速前进。这样的空间可以用：

$$
\begin{bmatrix}
&光的标准方向1&光的标准方向2&光的标准方向3\\ 
维度1:&\overgroup{1}&\overgroup{0}&\overgroup{0}\\
维度2:&0&1&0\\
维度3:&\undergroup{0}&\undergroup{0}&\undergroup{1}
\end{bmatrix}
$$

来表示。这个空间中任何光前进的方向都能够用以上三个基准方向组成。当空间被扭曲后，光前进的标准方向与速度也会被改变。例如上面遇到过的：

$$
\begin{array}{c}
   空间的扭曲&\\
   \begin{bmatrix} 
\overgroup{1/30}&\overgroup{0}&\overgroup{0}\\
0&1/20&0\\
\undergroup{0}&\undergroup{0}&\undergroup{1/10}
\end{bmatrix}
\end{array}

\Rightarrow


\begin{bmatrix} 
\begin{array}{c}
这个方向的光\\
变慢成1/30
\end{array}&
\begin{array}{c}
这个方向的光\\
变慢成1/20
\end{array}&
\begin{array}{c}
这个方向的光\\
变慢成1/10
\end{array}
\\
\overgroup{1/30}&\overgroup{0}&\overgroup{0}\\
0&1/20&0\\
\undergroup{0}&\undergroup{0}&\undergroup{1/10}
\end{bmatrix}
$$

光之所以会在扭曲的空间内变慢，是因为扭曲的空间被压缩了。空间除了可以被压缩或是扩张外，也可以被旋转。

$$
\begin{aligned}
&\begin{array}{c}
   线性变换后\\
   光的标准方向旋转了\\
   \begin{bmatrix} 
\overgroup{0}&\overgroup{-1}\\
\undergroup{1}&\undergroup{0}
\end{bmatrix}
\end{array}
×
\begin{array}{c}
空间扭曲前坐标\\
\begin{bmatrix} 
瓦肯星&南门二&地球&烧烤摊\\
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
瓦肯星&南门二&地球&烧烤摊\\
\overgroup{\undergroup{\begin{bmatrix} 
\overgroup{0}&\overgroup{-1}\\
\undergroup{1}&\undergroup{0}
\end{bmatrix}
\begin{bmatrix} 
30\\
10
\end{bmatrix}}}
&
\overgroup{\undergroup{\begin{bmatrix} 
\overgroup{0}&\overgroup{-1}\\
\undergroup{1}&\undergroup{0}
\end{bmatrix}
\begin{bmatrix} 
75\\
89
\end{bmatrix}}}
&
\overgroup{\undergroup{\begin{bmatrix} 
\overgroup{0}&\overgroup{-1}\\
\undergroup{1}&\undergroup{0}
\end{bmatrix}
\begin{bmatrix} 
0\\
0
\end{bmatrix}}}
&
\overgroup{\undergroup{\begin{bmatrix} 
\overgroup{0}&\overgroup{-1}\\
\undergroup{1}&\undergroup{0}
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
瓦肯星&南门二&地球&烧烤摊\\
-10&-89&0&-22\\
30&75&0&120
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
null space -->