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

要从原点$\begin{bmatrix}0\\0\\0\end{bmatrix}$去往宇宙尽头的烧烤摊$\begin{bmatrix}30\\20\\10\end{bmatrix}$,我们就必须实实在在地在第一维度上走30步，第二维度走20步，第三维度走10步。如果我们有能力改变宇宙空间的形状，把$\begin{bmatrix}30\\20\\10\end{bmatrix}$拉近到$\begin{bmatrix}1\\1\\1\end{bmatrix}$，那我们就不用浪费太多时间在太空旅行上了呢。

可惜的是文明的本能是会把任何科技作为武器，线性变换引擎也不例外。它可以用来扭曲敌人的宇宙空间，让敌人无法到达目的地。这也是第一章真正主要介绍的内容：计算目的地在扭曲后空间的位置：

$$
空间扭曲A × 扭曲前的坐标c = 扭曲后的坐标z
$$

或是观测到空间扭曲后中的某物体，求它在空间扭曲前的位置：

$$
空间扭曲A × 扭曲前的坐标x = 扭曲后的坐标b
$$

一般有两种方式来知道扭曲前的坐标$x$。第一种方法是把已知数据告诉智子我，我再指派别人来计算（当然您也可以口算）；第二种方法是用我们自己的线性变换引擎把宇宙空间复原成扭曲前的样子，这样我们就可以直接观测，而不用计算了！

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

相信作为舰长的您，也会好奇如何掌握真·空间扭曲Z，并且口算出$真·反空间扭曲Z^{-1}$的吧？要提醒您的是，线性变换引擎虽然已经量产化，不过正如其名，它只能对空间进行线性变换。当然还有其它可能的空间扭曲方法，只是还没有宇宙文明掌握相应的科技。

### <span style="color:#6c9ef0"/> **A Cartographer of Space 太空地图师**

假设我们把地球和月球之间的空间延展10倍。从地球看，月球就会变小很多。但是我们并不知道是月球缩小了，还是距离变远了。如果我们正好在地球和月球之间放了一把尺子，就会发现这把尺子被放大了10倍。尺子上的1米刻度实际上有10米长。

尺子提供了用来度量1维空间的单位。在高于1维的空间中，我们用的是坐标系来作为度量长度以及方向的单位。当某片不包含任何可观测物的太空被线性空间扭曲时，虽然我们看不到扭曲的效果，但是我们可以把线性空间扭曲反映在标示此空间的坐标系上。

在2维空间中，标准坐标系是：

<center>
<img width="200" src="https://fengthedroid.github.io/spacetravelguide/resources/ch2-1.png"/>
</center>

$$
标准2维坐标系：
\begin{bmatrix}\overgroup{1}&\overgroup{0}\\\undergroup{0}&\undergroup{1}\end{bmatrix}
$$

我们可以把两个向量分别看成是坐标系在第一维度和第二维度内的两把标准长度的尺子。如果我们观测到这两把尺子的方向和长度变化，也就能计算出这个空间内任何线性空间变换的效果。例如：

$$
\begin{array}{c}
线性变换对标准2维坐标系的影响\\
\begin{bmatrix}\overgroup{1/20}&\overgroup{0}\\\undergroup{0}&\undergroup{1/10}\end{bmatrix}
\end{array}
×
\begin{array}{c}
宇宙尽头的烧烤摊\\
\begin{bmatrix}
20\\
10
\end{bmatrix}
\end{array}
=
\begin{array}{c}
空间扭曲后烧烤摊变近了\\
\begin{bmatrix}
1\\
1
\end{bmatrix}
\end{array}
$$

三体人的探测器水滴💧在摧毁人类舰队的时候，大家注意到了它可以做到速度不变的转向。在这里提起，应该不难想到它也装备了线性变换引擎吧。若是要在2维空间内180度转向并保留动量，只需将前方的空间扭曲为：

$$
\begin{array}{c}
线性变换对标准3维坐标系的影响\\
\begin{bmatrix}\overgroup{-1}&\overgroup{0}&\overgroup{0}\\
0&-1&0\\
\undergroup{0}&\undergroup{0}&\undergroup{-1}\end{bmatrix}
\end{array}
×
\begin{array}{c}
💧速度与方向\\
\begin{bmatrix}
20\\
10\\
55
\end{bmatrix}
\end{array}
=
\begin{array}{c}
💧新的速度与方向\\
\begin{bmatrix}
-20\\
-10\\
-55
\end{bmatrix}
\end{array}
$$

也就是说，我们可以用多维矩阵来描述多维太空区域的线性扭曲状态。矩阵就是我们在线性变换后的太空中的地图。

### <span style="color:#6c9ef0" /> **飞船舰长职责：计算多个线性变换后的坐标系**

显然，当整片太空区域被线性变换，区域内的太空以及物质都会受到影响。拿我们的宁静号飞船举例，在线性变换$\begin{bmatrix} \overgroup{0}&\overgroup{-0.5}\\\undergroup{1.5}&\undergroup{0}\end{bmatrix}$后，不但整个船被移动到了新的位置，而且船体的形状和方向也变了。

<center>
<img src="https://fengthedroid.github.io/spacetravelguide/resources/ch2-2.gif"/>
</center>

用矩阵来代表船体的变化：

$$
\begin{aligned}
&\begin{array}{c}
   线性变换\\
   \begin{bmatrix} 
\overgroup{0}&\overgroup{-0.5}\\
\undergroup{1.5}&\undergroup{0}
\end{bmatrix}
\end{array}
×
\begin{array}{c}
宁静号\\
\begin{bmatrix} 
船头&船尾\\
2.25&0.5\\
1&1.75
\end{bmatrix}
\end{array}
\\
\\
&=
\begin{array}{c}
   \begin{bmatrix} 
   \overgroup{\undergroup{\begin{bmatrix} 

\overgroup{0}&\overgroup{-0.5}\\
\undergroup{1.5}&\undergroup{0}
\end{bmatrix}
\begin{bmatrix} 
2.25\\
1
\end{bmatrix}}}
&
\overgroup{\undergroup{\begin{bmatrix} 
\overgroup{0}&\overgroup{-0.5}\\
\undergroup{1.5}&\undergroup{0}
\end{bmatrix}
\begin{bmatrix} 
0.5\\
1.75
\end{bmatrix}}}
\end{bmatrix}
\end{array}
\\
\\
&=
\begin{array}{c}
扭曲后的宁静号\\
\begin{bmatrix} 
船头&船尾   \\
-0.5&-0.875\\
3.375&0.75
\end{bmatrix}
\end{array}
\end{aligned}
$$

我们，或者任何拥有线性变换引擎的人，也可以对已经扭曲的空间再次线性扭曲。其最终效果可以从再次扭曲的坐标系显示出来。

$$
\begin{aligned}
&\begin{array}{c}
   线性变换\\
   \begin{bmatrix} 
\overgroup{0}&\overgroup{-1}\\
\undergroup{1}&\undergroup{0}
\end{bmatrix}
\end{array}
×
\begin{array}{c}
已经被线性扭曲的空间的坐标系\\
\begin{bmatrix} 
尺度1&尺度2\\
30&75\\
10&89
\end{bmatrix}
\end{array}
\\
\\
&=
\begin{array}{c}
再次扭曲后的效果\\
\begin{bmatrix} 
尺度1&尺度2\\
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
\end{bmatrix}
\end{array}
\\
\\
&=
\begin{array}{c}
最终的线性扭曲效果\\
\begin{bmatrix} 
尺度1&尺度2\\
-10&-89\\
30&75
\end{bmatrix}
\end{array}
\end{aligned}
$$

从这个例子不难看出，计算多重线性变换的叠加，同计算单个线性变换对于一组坐标向量的影响是相同的。毕竟，扭曲前或扭曲后的坐标系标准向量也是坐标向量，就像在1维空间中，1米既可以是长度的单位，也可以是具体的长度。

我们也可以通过一次或是多次坐标变换来将扭曲的空间还原。例如：$\begin{bmatrix} \overgroup{0}&\overgroup{-2}\\\undergroup{2}&\undergroup{0}\end{bmatrix}$是将空间左转90度，并将空间放大一倍的线性变换。我们可以：

$$
\begin{aligned}
&将空间右转90度的变换A
×
将空间缩小一倍的变换B
×
\begin{bmatrix} 
0&-2\\
2&0
\end{bmatrix}
\\
\\
&=
可以同时将空间右转90度并缩小一倍的变换AB
×
\begin{bmatrix} 
0&-2\\
2&0
\end{bmatrix}
\\
\\
&=
\begin{array}{c}
最终的回到正常的太空\\
\begin{bmatrix} 
1&0\\
0&1
\end{bmatrix}
\end{array}
\end{aligned}
$$

这样一次改变一点点，逐渐将扭曲的空间变回正常空间的算法，在人类文明中叫做Gauss–Jordan elimination（高斯-若尔当消元法）。

可惜的是，不是所有被线性变换所扭曲的太空都是可以还原的。某些线性变换对空间具有降维打击的效果。被降维的空间内的信息会被遗失。这样的空间将再也无法还原到过去。我们就在降维打击专门的章节再深入讨论吧！