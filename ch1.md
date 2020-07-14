# 🚀多维飞船驾驶指南以及降维打击口诀，真的不是线性代数教程

您好，我是智子😘。首先我将在这份指南中向您介绍多维飞船的驾驶方法。多维飞船即是可以在任意维度的宇宙中航行的飞船，它也具有在不同维度的宇宙间跳跃的能力。后面的章节我也会介绍飞船的主武器：降维打击引擎😱。

## CH 1. 某一维度宇宙内的航行

### **坐标系**

您生活的地球是以经纬度这种二维的坐标向量(Vector)来区分地球上每个不同的地点。例如：

$$\begin{bmatrix} Latitude: 39.9042° N \\ Longitude: 116.4074° E\end{bmatrix}$$

宇宙的导航图也采用类似的坐标系。二维宇宙采用2维坐标，三为宇宙则是3维。而

$$\begin{bmatrix} 
5 \\ 7 \\ -3 \\ 0 \\12
\end{bmatrix}$$

则是在5维宇宙中的某点。🖖

### **发动机**

通常您可以告诉我坐标，由我驾驶飞船。但是作为舰长的您有必要了解飞船的发动机是如何运行的。目前我们处于3维宇宙中，我们有3个可以用的发动机：

$$\begin{bmatrix} 
engine 1 & engine 2 & engine 3\\
\overgroup{1}&\overgroup{0}&\overgroup{0}\\
0&1&1\\
\undergroup{0}&\undergroup{0}&\undergroup{1}\\
\end{bmatrix}$$

这里我们用3组向量的形式来代表当前发动机的动力方向配置。由于飞船的能量来源特殊，飞船是无法转向的，只能在发动机动力方向的直线上航行，因此我们会有多个发动机（后面章节会解释哦🥺）。如果我们需要前往：

$$\begin{bmatrix} 
 1\\ 1\\ 0
\end{bmatrix}$$

那么我们只需要为发动机No1和发动机No2各提供能量1次即可。发动机也可以逆向运行。前往

$$\begin{bmatrix} 
-5\\2\\2
\end{bmatrix}$$

只需要给发动机No1提供逆向能量5次，给发动机No3提供正向能量2次。另外需要注意的就是发动机No3每次运行，都会让飞船在这3维宇宙中的两个维度同时移动。这就让发动机提供能量几次才能到达某地的计算更复杂了。我们也想每次发动机都能只在自己的维度上运动，就像如下的发动机配置：

$$\begin{bmatrix} 
engine 1 & engine 2 & engine 3\\
\overgroup{1}&\overgroup{0}&\overgroup{0}\\
0&1&0\\
\undergroup{0}&\undergroup{0}&\undergroup{1}\\
\end{bmatrix}$$

可惜的是因为能量来源的问题，发动机提供动力的方向是我们无法决定的😅，而是由飞船所在的宇宙区域所决定。在飞船进入某个宇宙区域后，我们能决定的就是给每个发动机提供几次能量来到达我们的目的地。为了方便，我们将为发动机提供能量的次数也以向量来表示。

$$\begin{bmatrix} 
engine 1 & engine 2 & engine 3\\
\overgroup{1}&\overgroup{0}&\overgroup{0}\\
0&1&1\\
\undergroup{0}&\undergroup{0}&\undergroup{1}\\
\end{bmatrix}
\begin{bmatrix} 
&能量\\
engine 1 &-5\\
engine 2 &0\\
engine 3 &2
\end{bmatrix}
=
\begin{bmatrix} 
目的地\\
-5\\2\\2
\end{bmatrix}$$

### **飞船舰长职责 1：计算给发动机提供多少能量**

现在我们飞入了某个4维宇宙，舰长的责任之一就是在我掉线的时候也能给出w,x,y,z的数值🤔：

$$\begin{bmatrix} 
e1 & e2 & e3 & e4\\
\overgroup{1}&\overgroup{1}&\overgroup{0}&\overgroup{4}\\
0&-1&1&-2\\
-4&2&-2&0\\
\undergroup{0}&\undergroup{0}&\undergroup{1}&\undergroup{-1}\\
\end{bmatrix}
\begin{bmatrix} 
&能量\\
e1&w\\
e2&x\\
e3&y\\
e4&z
\end{bmatrix}
=
\begin{bmatrix} 
目的地\\
-2\\1\\2\\4
\end{bmatrix}$$

如果我们用A来代表发动机动力方向组成的矩阵，x代表每个发动机提供多少能量的向量，b代表目的地坐标向量。舰长责任1 就是求解：

$$Ax=b$$

这也是作为舰长最重要的职责了。大部分其它职责都和Ax=b有各种各样的联系。我们将在接下来的几章中慢慢讨论如何得到x的值。而在本章中，我们则先从更简单的舰长职责开始。

### **飞船舰长职责 2: 计算目的地**

一般来说，您告诉我想前往的目的地后，我会给出每个发动机需要多少能量的向量。例如：


$$\begin{bmatrix} 
e1 & e2 & e3 & e4\\
\overgroup{1}&\overgroup{1}&\overgroup{0}&\overgroup{4}\\
0&-1&1&-2\\
-4&2&-2&0\\
\undergroup{0}&\undergroup{0}&\undergroup{1}&\undergroup{-1}\\
\end{bmatrix}
\begin{bmatrix} 
&能量\\
e1&w\\
e2&x\\
e3&y\\
e4&z
\end{bmatrix}
=
\begin{bmatrix} 
目的地\\
-2\\1\\2\\4
\end{bmatrix}
解为  
\begin{bmatrix} 
w=1\\
x=5\\
y=2\\
z=-2
\end{bmatrix}
$$

那么以谨慎出名的舰长您自然是不能相信一个AI给出的答案，而会自己验算：

$$\begin{bmatrix} 
e1 & e2 & e3 & e4\\
\overgroup{1}&\overgroup{1}&\overgroup{0}&\overgroup{4}\\
0&-1&1&-2\\
-4&2&-2&0\\
\undergroup{0}&\undergroup{0}&\undergroup{1}&\undergroup{-1}
\end{bmatrix}

\begin{bmatrix} 
能量\\
1\\
5\\
2\\
-2
\end{bmatrix}

=
\begin{bmatrix} 
目的地\\
?\\?\\?\\?
\end{bmatrix}
$$
请使出必杀技尽情地验算吧！

$$\begin{matrix} 
\overgroup{1}\\
0\\
-4\\
\undergroup{0}
\end{matrix}
×1 +

\begin{matrix} 
\overgroup{1}\\
-1\\
2\\
\undergroup{0}
\end{matrix}
×5+

\begin{matrix} 
\overgroup{0}\\
1\\
-2\\
\undergroup{1}
\end{matrix}
×2+

\begin{matrix} 
\overgroup{4}\\
-2\\
0\\
\undergroup{-1}
\end{matrix}
×-2
=
\begin{bmatrix} 
目的地\\
1+5+0-8\\0-5+2+4\\-4+10-4+0\\0+0+2+2
\end{bmatrix}
$$
似乎我给了您准确的答案呢。时而我也会提供这样的答案：

$$\begin{bmatrix} 
\overgroup{1}&\overgroup{1}&\overgroup{0}\\
0&-1&1\\
\undergroup{0}&\undergroup{0}&\undergroup{1}
\end{bmatrix}

\begin{bmatrix} 
1\\
5\\
2\\
-2
\end{bmatrix}
=？

\\无法计算啊摔！多了一个能量数据啊八戒！
$$

或是：

$$\begin{bmatrix} 
\overgroup{1}&\overgroup{1}&\overgroup{0}\\
0&-1&1\\
\undergroup{0}&\undergroup{0}&\undergroup{1}
\end{bmatrix}

\begin{bmatrix} 
1\\
-3
\end{bmatrix}
=?
\\少了一个发动机的能量数据阿咧！剩下的两个哪个发动机用啊？
$$
所以最好还是不要依赖我这个AI来给出Ax=b的答案吧拜托了🙏🐶

### **飞船舰长职责 3: 发动机故障检测（初级）**

并不是每片宇宙都是美丽的🤘。有的宇宙会让我们的发动机组无法正常运转。几天前我们跳入了一个3维宇宙，却发现我们只有一组发动机了！

$$
\begin{bmatrix}
engine 1\\ 
\overgroup{1}\\
0\\
\undergroup{0}
\end{bmatrix}
$$

在这个3维宇宙中，我们只能在一条直线上移动😭！给1号发动机供能5次我们就到了$\begin{bmatrix}\overgroup{1}\\0\\\undergroup{0}\end{bmatrix}×\begin{bmatrix}5\end{bmatrix}=\begin{bmatrix}5\\0\\0\end{bmatrix}$。若是反向供能3次我们就到了$\begin{bmatrix}\overgroup{1}\\0\\\undergroup{0}\end{bmatrix}×\begin{bmatrix}-3\end{bmatrix}=\begin{bmatrix}-3\\0\\0\end{bmatrix}$。可是我们永远到不了$\begin{bmatrix}5\\0\\2\end{bmatrix}$！有时候宇宙会赐予我们三个发动机，它们却是像这样的：

$$
\begin{bmatrix}
engine1&engine2&engine3\\ 
\overgroup{1}&\overgroup{1}&\overgroup{0}\\
0&0&0\\
\undergroup{0}&\undergroup{0}&\undergroup{0}
\end{bmatrix}
$$

显然一号和二号发动机作用是完全一样的啊！而三号发动机完全没有用🤦！这和只有一个发动机有什么区别啊！但是！区别还是有的！那就是，如果您想前往$\begin{bmatrix}5\\0\\0\end{bmatrix}$，您可以有多个选择！您可以

$$
\begin{bmatrix}
\overgroup{1}&\overgroup{1}&\overgroup{0}\\
0&0&0\\
\undergroup{0}&\undergroup{0}&\undergroup{0}
\end{bmatrix}
×
\begin{bmatrix}5\\0\\0\end{bmatrix}=\begin{bmatrix}5\\0\\0\end{bmatrix}
$$

也可以

$$
\begin{bmatrix}
\overgroup{1}&\overgroup{1}&\overgroup{0}\\
0&0&0\\
\undergroup{0}&\undergroup{0}&\undergroup{0}
\end{bmatrix}
×
\begin{bmatrix}0\\5\\0\end{bmatrix}=\begin{bmatrix}5\\0\\0\end{bmatrix}
$$

甚至可以

$$
\begin{bmatrix}
\overgroup{1}&\overgroup{1}&\overgroup{0}\\
0&0&0\\
\undergroup{0}&\undergroup{0}&\undergroup{0}
\end{bmatrix}
×
\begin{bmatrix}-7\\12\\0\end{bmatrix}=\begin{bmatrix}5\\0\\0\end{bmatrix}
$$

也就是说只要是$\begin{bmatrix}t\\0\\0\end{bmatrix}$这一直线上的旅途的终点，您可以任性搭配1号和2号发动机！当然您还是不能去任何第二维度或是第三维度上非0的地方。

有时候，您会遇到这样的发动机组：

$$
\begin{bmatrix}
engine1&engine2&engine3\\ 
\overgroup{2}&\overgroup{0}&\overgroup{3}\\
\undergroup{0}&\undergroup{1}&\undergroup{0}
\end{bmatrix}
$$

在2维宇宙中有3个发动机，那么肯定是有多余的发动机不是吗？每次给发动机1号供能1.5的话，它的动力就和3号发动机一样了。同理，在5维宇宙只有5个方向，如果您配置了8个发动机，那么至少有3个是没用的。若是这8个发动机方向上有所重复，只能在2个方向上移动飞船，那么就有6个发动机是在划水摸鱼了喂。

这些就是发动机组故障的概述。今后我们还会回顾这些问题呦。例如在4维宇宙中，这样的发动机组：

$$
\begin{bmatrix}
engine1&engine2&engine3&engine4\\ 
\overgroup{2}&\overgroup{1}&\overgroup{4}&\overgroup{7}\\
-3&2&1&0\\
4&-2&0&2\\
\undergroup{1}&\undergroup{1}&\undergroup{3}
&\undergroup{5}
\end{bmatrix}
$$

到底是不是能随意游走到4维宇宙里到每个目的地呢？还是只能在4维空间的某个亚3维空间，或者只在一个平面上，或者只是一条直线上移动呢？