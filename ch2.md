## 多维飞船CH 2. 矩阵宇宙

蓝色药丸您已经服下了？现在起就让我们进入矩阵宇宙（The Matrix）吧。那个，并没有进错片场啦。上一章讲飞船发动机什么的都是骗你的。毕竟您也会疑惑，如果发动机配置有异常，怎么不修理呢是不是？

### <span style="color:#6c9ef0" /> **Welcome Onboard For Real, Captain**

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

要从原点$\begin{bmatrix}0\\0\\0\end{bmatrix}$去往宇宙尽头的烧烤摊$\begin{bmatrix}30\\20\\10\end{bmatrix}$,我们就必须实实在在地在第一维度上走30步，第二维度走20步，第三维度走10步。如果我们有能力改变宇宙空间的形状，把$\begin{bmatrix}30\\20\\10\end{bmatrix}$拉近到$\begin{bmatrix}1\\1\\1\end{bmatrix}$，那我们就不用浪费太多时间在太空旅行上了！

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
宇宙尽头的\\烧烤摊\\
\begin{bmatrix} 
30\\
20\\
10
\end{bmatrix}
\end{array}
=
\begin{array}{c}
空间扭曲后\\烧烤摊的位置\\
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
\begin{aligned}
~~~~真·空间扭曲Z = &第n次空间扭曲N × ... \\
&× 第2次空间扭曲B \\
&× 第1次空间扭曲A
\end{aligned}
$$

相信作为舰长的您，也会好奇如何掌握真·空间扭曲Z，并且口算出$真·反空间扭曲Z^{-1}$的吧？为此，咱们就要再深聊聊宇宙。

### <span style="color:#6c9ef0" /> **宇宙与光**（乐队队名预定，都别抢）

宇宙真的真的[好大好空](https://joshworth.com/dev/pixelspace/pixelspace_solarsystem.html)。就算空间被扭曲，似乎也没有办法什么观测到扭曲的效果。我们如何度量这样庞大的虚无呢？



之前我们用向量代表过坐标，或是发动机引擎，或是能量。下面我们要用向量代表光前进的速度和方向。

在未被扭曲过的3维宇宙中，光可以自由地在任一一个维度上以标准光速前进。这样的空间可以用：

$$
\begin{bmatrix}
&光的基准方向1&光的基准方向2&光的基准方向3\\ 
维度1:&\overgroup{1}&\overgroup{0}&\overgroup{0}\\
维度2:&0&1&0\\
维度3:&\undergroup{0}&\undergroup{0}&\undergroup{1}
\end{bmatrix}
$$

来表示。这个空间中任何光可以前进的方向都可以用以上三个基准方向来表示。


<!-- 
让我们先在学校附近的空间试用一下飞船的线性变换引擎吧：

$$
\begin{aligned}
&\begin{array}{c}
   用线性变换引擎\\
   实现空间的扭曲-矩阵B&\\
   \begin{bmatrix} 
\overgroup{0.1}&\overgroup{0}\\
\undergroup{0}&\undergroup{0.2}
\end{bmatrix}
\end{array}
×
\begin{array}{c}
空间扭曲前坐标-矩阵C\\
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
空间扭曲后坐标BC\\
\begin{bmatrix} 
食堂&篮球场&宿舍&烧烤摊\\
3&7.5&0&12\\
2&17.8&0&4.4
\end{bmatrix}
\end{array}

\end{aligned}
$$

为了操作线性变换引擎，我们用到了两个矩阵。矩阵$B$代表的是空间的扭曲，矩阵$C$则是4个不得不去的坐标的集合。之前我们介绍了矩阵（发动机）乘以向量（能量）的算法。现在两个矩阵相乘，也可以看成是右边的矩阵内每个向量单独和左边的矩阵相乘，最后再集合成为一个矩阵。如果明天学校把空间扭曲前的烧烤摊撤了，那么空间扭曲后的矩阵也只剩3个坐标向量。并且坐标的数值不会受到烧烤摊消失的影响。只是心情会有些许低落。

显然，教数学的体育老师是不会让你随便扭曲学校的空间的！为了让学生们有更多锻炼身体的机会，他也使用了线性变换$\begin{bmatrix} \overgroup{30}&\overgroup{10}\\\undergroup{10}&\undergroup{30}\end{bmatrix}$！

$$
\begin{aligned}
&\begin{array}{c}
   体育老师的线性变换A&\\
   \begin{bmatrix} 
\overgroup{30}&\overgroup{10}\\
\undergroup{10}&\undergroup{30}
\end{bmatrix}
\end{array}
×
\begin{array}{c}
我方线性变换后坐标BC\\
\begin{bmatrix} 
食堂&篮球场&宿舍&\sout{烧烤摊}\\
3&7.5&0\\
2&17.8&0
\end{bmatrix}
\end{array}
\\
\\
&=
\begin{array}{c}
   体育老师的线性变换A&\\
   \begin{bmatrix} 
\overgroup{30}&\overgroup{10}\\
\undergroup{10}&\undergroup{30}
\end{bmatrix}
\end{array}
×
\begin{array}{c}
   我方的线性变换B&\\
   \begin{bmatrix} 
\overgroup{0.1}&\overgroup{0}\\
\undergroup{0}&\undergroup{0.2}
\end{bmatrix}
\end{array}
×
\begin{array}{c}
最开始的坐标C\\
\begin{bmatrix} 
食堂&篮球场&宿舍\\
30&75&0\\
10&89&0
\end{bmatrix}
\end{array}
\\
\\
&=
\begin{array}{c}
   在线性变换B之上加以体育老师的变换AB&\\
   \begin{bmatrix} 
\overgroup{3}&\overgroup{2}\\
\undergroup{1}&\undergroup{6}
\end{bmatrix}
\end{array}
×
\begin{array}{c}
最开始的坐标C\\
\begin{bmatrix} 
食堂&篮球场&宿舍\\
30&75&0\\
10&89&0
\end{bmatrix}
\end{array}

\\
\end{aligned}
$$

尽管矩阵$A$和$B$代表的是线性变换，而$C$是坐标的集合，以上$AB$的计算方法和计算$BC$却是一致的。毕竟矩阵自身没有标签。若是把所有文字去掉只剩下数字，谁也不知道矩阵$C$到底是坐标的集合还是线性变换吧？

从上面的几次线性变换也可以看出，每次都是左边的矩阵~~扭曲~~变换右边的矩阵。顺序可是固定的哦。

### **派对后的打扫工作-反~~空间扭曲~~线性变换**
-----


宇宙的维度与方向 -》 黑洞

multiply
determinant
inverse
column space
null space -->