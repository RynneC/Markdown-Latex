[TOC]

# 1 Markdown基本语法

## 1.1 markdown基本功能

(1) 建立代码块: ``,  中间填充内容

(2) 分割线: `***` + press "enter", 如

***

(3) 建立表格: `| | |` + press "enter", 如

|      |      |
| ---- | ---- |
|      |      |

(4) 数学公式: 在文字段落外独立建立数学公式(居中): `$$` + press "enter", 如
$$
1+1=2
$$
​					   在文字间建立数学公式: `$ $`, 中间填充内容, 如 $1+1=2$

在数学公式中打空格: 空格大小从小到大依次为: `\,`   `\; `  `\quad`  `\qquad`; 注意因为是数学公式所以要加$$, 且quad和qquad之后要空一格: 

$a\,b$, $a\;b$, $a\quad b$, $a\qquad b$

(5) 数学公式中需换行: \\\

(6) 加粗: `** **`, 中间填充, 如 **abc**

(7) 加斜体: `* *`, 中间填充, 如 *abc*

(8)数学公式中的删除线: 两侧$$ + `\cancel{}`, 

​	如 $\cancel{abc}$

​	将删除线翻转过来: 两侧$$ + `\bcancel`,  

​	如$\bcancel{abc}$

​	也可以用来表示将某个字符改为另一个字符: 两侧$$ + `\cancelto{}{}`, 如cancelto{0}{x}就是改	变x为0, 如下

​	$\cancelto{0}{x}$

​	综合运用: 内联符 + \frac{1\cancel9}{\cancel95} = \frac{1}{5}, 如下

​	$\frac{1\cancel9}{\cancel95} = \frac{1}{5}$

## 1.2 字体大小

### 1.2.1 字体大小变换

(两侧$$) 从小到大: 

\tiny{xxx}: $\tiny{xxx}$

\scriptsize{xxx}: $\scriptsize{xxx}$

\small{xxx}: $\small{xxx}$

\normalsize{xxx}: $\normalsize{xxx}$

\large{xxx}: $\large{xxx}$

\Large{xxx}: $\Large{xxx}$

\LARGE{xxx}: $\LARGE{xxx}$

### 1.2.2 数学公式大小

(两侧$$) 从小到大: 

{\scriptscriptstyle \int f^{-1}(x-x_a),dx}: ${\scriptscriptstyle \int f^{-1}(x-x_a),dx}$

{\scriptstyle \int f^{-1}(x-x_a),dx}: ${\scriptstyle \int f^{-1}(x-x_a),dx}$

{\textstyle \int f^{-1}(x-x_a),dx}: ${\textstyle \int f^{-1}(x-x_a),dx}$

{\displaystyle \int f^{-1}(x-x_a),dx}: ${\displaystyle \int f^{-1}(x-x_a),dx}$

## 1.3 插入图片以及调整大小

笔者认为最好的解决方法是这样的: 在Typora设置-图像中选择插入图片时复制图片到./${filename}.assets文件夹, 并且勾选对本地位置的图片应用上述规则, 以及允许根据YAML设置自动上传图片. 

这样之后, 默认在markdown文件的同一文件夹路径下创建一个该文件同名的文件夹以存该文件中的图片源等asset(需要点击确认). 

于是, 当将设备上的图片复制进markdown文件后, markdown会自动在asset文件夹中保存一份备份, 而后对复制的图片的markdown源代码全选并点击右键, 选择转换图片语法, 将图片从markdown格式转换为html格式, 而后直接在<>中末尾/前加上style = "width: ...px", 就可以调整图片大小. 笔者习惯使用width: 200px来存放小图片. 稍大一些可以500px. 

## 1.4 Html支持

### 1.4.1 文字的居中

令content居中: <div align = "center">(content)</div>

<div align = "center">Hello world</div>

### 1.4.2 用html改变字体样式和大小

`<font face="黑体">黑体字</font>
<font face="微软雅黑">微软雅黑</font>
<font face="STCAIYUN">华文彩云</font>
<font color=blue>蓝色</font>
<font color=#008000>绿色</font>
<font color=Red>红色</font>
<font size=5>尺寸</font>
`

<font face="黑体">黑体字</font>
<font face="微软雅黑">微软雅黑</font>
<font face="STCAIYUN">华文彩云</font>
<font color=blue>蓝色</font>
<font color=#008000>绿色</font>
<font color=Red>红色</font>
<font size=5>尺寸</font>

### 1.4.3 用html改变字体颜色和背景颜色

`<table>
  <tbody>
  <tr>
    <th>颜色名</th>
    <th>十六进制颜色值</th>
    <th>颜色</th>
  </tr>
  <tr>
    <td><font color="AliceBlue">AliceBlue</font></td>
    <td><font color="AliceBlue">F0F8FF</font></td>
    <td bgcolor="AliceBlue">rgb(240, 248, 255)</td>
  </tr>
  <tr>
    <td><font color="AntiqueWhite">AntiqueWhite</font></td>
    <td><font color="AntiqueWhite">#FAEBD7</font></td>
    <td bgcolor="AntiqueWhite">rgb(250, 235, 215)</td>
  </tr>
  <tr>
    <td><font color="Lavender">Lavender</font></td>
    <td><font color="Lavender">#E6E6FA</font></td>
    <td bgcolor="Lavender">rgb(230, 230, 250)</td>
  </tr>
  <tr>
    <td><font color="LavenderBlush">LavenderBlush</font></td>
    <td><font color="LavenderBlush">#FFF0F5</font></td>
    <td bgcolor="LavenderBlush">rgb(255, 240, 245)</td>
  </tr>
  <tr>
    <td><font color=" LightPink"> LightPink</font></td>
    <td><font color=" LightPink">#FFB6C1</font></td>
    <td bgcolor=" LightPink">rgb(255, 182, 193)</td>
  </tr>
  <tr>
    <td><font color="LightSalmon">LightSalmon</font></td>
    <td><font color="LightSalmon">#FFA07A</font></td>
    <td bgcolor="LightSalmon">rgb(255, 160, 122)</td>
  </tr>
  <tr>
    <td><font color="MintCream">MintCream</font></td>
    <td><font color="MintCream">#F5FFFA</font></td>
    <td bgcolor="MintCream">rgb(245, 255, 250)</td>
  </tr>
  <tr>
    <td><font color="MistyRose">MistyRose</font></td>
    <td><font color="MistyRose">#FFE4E1</font></td>
    <td bgcolor="MistyRose">rgb(255, 228, 225)</td>
  </tr>
  <tr>
    <td><font color="Moccasin">Moccasin</font></td>
    <td><font color="Moccasin">#FFE4B5</font></td>
    <td bgcolor="Moccasin">rgb(255, 228, 181)</td>
  </tr>
  <tr>
    <td><font color="MintCream">MintCream</font></td>
    <td><font color="MintCream">#F5FFFA</font></td>
    <td bgcolor="MintCream">rgb(245, 255, 250)</td>
  </tr>
  <tr>
    <td><font color="PaleVioletRed">PaleVioletRed</font></td>
    <td><font color="PaleVioletRed">#D87093</font></td>
    <td bgcolor="PaleVioletRed">rgb(216, 112, 147)</td>
  </tr>
</table>
`

<table>
  <tbody>
  <tr>
    <th>颜色名</th>
    <th>十六进制颜色值</th>
    <th>颜色</th>
  </tr>
  <tr>
    <td><font color="AliceBlue">AliceBlue</font></td>
    <td><font color="AliceBlue">F0F8FF</font></td>
    <td bgcolor="AliceBlue">rgb(240, 248, 255)</td>
  </tr>
  <tr>
    <td><font color="AntiqueWhite">AntiqueWhite</font></td>
    <td><font color="AntiqueWhite">#FAEBD7</font></td>
    <td bgcolor="AntiqueWhite">rgb(250, 235, 215)</td>
  </tr>
  <tr>
    <td><font color="Lavender">Lavender</font></td>
    <td><font color="Lavender">#E6E6FA</font></td>
    <td bgcolor="Lavender">rgb(230, 230, 250)</td>
  </tr>
  <tr>
    <td><font color="LavenderBlush">LavenderBlush</font></td>
    <td><font color="LavenderBlush">#FFF0F5</font></td>
    <td bgcolor="LavenderBlush">rgb(255, 240, 245)</td>
  </tr>
  <tr>
    <td><font color=" LightPink"> LightPink</font></td>
    <td><font color=" LightPink">#FFB6C1</font></td>
    <td bgcolor=" LightPink">rgb(255, 182, 193)</td>
  </tr>
  <tr>
    <td><font color="LightSalmon">LightSalmon</font></td>
    <td><font color="LightSalmon">#FFA07A</font></td>
    <td bgcolor="LightSalmon">rgb(255, 160, 122)</td>
  </tr>
  <tr>
    <td><font color="MintCream">MintCream</font></td>
    <td><font color="MintCream">#F5FFFA</font></td>
    <td bgcolor="MintCream">rgb(245, 255, 250)</td>
  </tr>
  <tr>
    <td><font color="MistyRose">MistyRose</font></td>
    <td><font color="MistyRose">#FFE4E1</font></td>
    <td bgcolor="MistyRose">rgb(255, 228, 225)</td>
  </tr>
  <tr>
    <td><font color="Moccasin">Moccasin</font></td>
    <td><font color="Moccasin">#FFE4B5</font></td>
    <td bgcolor="Moccasin">rgb(255, 228, 181)</td>
  </tr>
  <tr>
    <td><font color="MintCream">MintCream</font></td>
    <td><font color="MintCream">#F5FFFA</font></td>
    <td bgcolor="MintCream">rgb(245, 255, 250)</td>
  </tr>
  <tr>
    <td><font color="PaleVioletRed">PaleVioletRed</font></td>
    <td><font color="PaleVioletRed">#D87093</font></td>
    <td bgcolor="PaleVioletRed">rgb(216, 112, 147)</td>
  </tr>
</table>

### 1.4.4 用html添加网址链接

<div class="footnotes"><hr><ol>
    <li id="fn:wx">  文章作者1（任意想输入的汉字）, 
    <a href="转载文章的网址"> 转载文章的名称 </a>. 
    <a href="#fnref:wx" rel="nofollow" title="Return to article" class="reversefootnote">↩</a></li>

 `<div class="footnotes"><hr><ol>
    <li id="fn:wx">  文章作者1（任意想输入的汉字）, 
    <a href="转载文章的网址"> 转载文章的名称 </a>. 
    <a href="#fnref:wx" rel="nofollow" title="Return to article" class="reversefootnote">↩</a></li>` 

## 1.5 字体样式

(1) Caligraphic letters(印刷字体): \mathcal{A}

$\mathcal{A} \mathcal{B} \mathcal{C} \mathcal{D} \mathcal{E} \mathcal{F} \mathcal{G} \mathcal{H} \mathcal{I} \mathcal{J} \mathcal{K} \mathcal{L} \mathcal{M} \mathcal{N} \mathcal{O} \mathcal{P} \mathcal{Q} \mathcal{R} \mathcal{S} \mathcal{T} \mathcal{U} \mathcal{V} \mathcal{W} \mathcal{X} \mathcal{Y} \mathcal{Z}$

(2) Mathbb letters(数学字母): \mathbb{A}

$\mathbb{A} \mathbb{B} \mathbb{C} \mathbb{D} \mathbb{E} \mathbb{F} \mathbb{G} \mathbb{H} \mathbb{I} \mathbb{J} \mathbb{K} \mathbb{L} \mathbb{M} \mathbb{N} \mathbb{O} \mathbb{P} \mathbb{Q} \mathbb{R} \mathbb{S} \mathbb{T} \mathbb{U} \mathbb{V} \mathbb{W} \mathbb{X} \mathbb{Y} \mathbb{Z}$

(3) Mathfrak letter(马弗雷克信): \mathfrak{A}

$\mathfrak{A} \mathfrak{B} \mathfrak{C} \mathfrak{D} \mathfrak{E} \mathfrak{F} \mathfrak{G} \mathfrak{H} \mathfrak{I} \mathfrak{J} \mathfrak{K} \mathfrak{L} \mathfrak{M} \mathfrak{N} \mathfrak{O} \mathfrak{P} \mathfrak{Q} \mathfrak{R} \mathfrak{S} \mathfrak{T} \mathfrak{U} \mathfrak{V} \mathfrak{W} \mathfrak{X} \mathfrak{Y} \mathfrak{Z}$

(4) Math Sans serif letter(无衬线字母类型): \mathsf{A}

$\mathsf{A} \mathsf{B} \mathsf{C} \mathsf{D} \mathsf{E} \mathsf{F} \mathsf{G} \mathsf{H} \mathsf{I} \mathsf{J} \mathsf{K} \mathsf{L} \mathsf{M} \mathsf{N} \mathsf{O} \mathsf{P} \mathsf{Q} \mathsf{R} \mathsf{S} \mathsf{T} \mathsf{U} \mathsf{V} \mathsf{W} \mathsf{X} \mathsf{Y} \mathsf{Z}$

(5) Math bold letters(加粗): \mathbf{A}

$\mathbf{A} \mathbf{B} \mathbf{C} \mathbf{D} \mathbf{E} \mathbf{F} \mathbf{G} \mathbf{H} \mathbf{I} \mathbf{J} \mathbf{K} \mathbf{L} \mathbf{M} \mathbf{N} \mathbf{O} \mathbf{P} \mathbf{Q} \mathbf{R} \mathbf{S} \mathbf{T} \mathbf{U} \mathbf{V} \mathbf{W} \mathbf{X} \mathbf{Y} \mathbf{Z}$

# 2 数学公式

## 2.1 基本运算符 Fundamental Operators

### 2.1.1 基本运算 

|                 Operator                  |       Code(+$$)        |
| :---------------------------------------: | :--------------------: |
|                    $+$                    |           +            |
|                    $-$                    |           -            |
|           $\pm$ (plus or minus)           |          \pm           |
|           $\mp$ (minus or plus)           |          \mp           |
|             $\times$ (times)              |         \times         |
|    $\cdot$ (times, between variables)     |         \cdot          |
|        $a\div b$ (a divided by b)         |        a \div b        |
|         $\frac{x}{y}$ (x over y)          | \frac{x}{y}或x \over y |
|         $|x+y|$ (absolute value)          |        \|x+y\|         |
|                 $\cdots$                  |         \cdots         |
|   $\lceil x \rceil$ (Ceiling, 向上取整)   |    \lceil x \rceil     |
| $\lfloor x \rfloor$ (Flooring, 向下取整)  |   \lfloor x \rfloor    |
| $\sqrt[n]{x}$ (nth root of x, x的n次方根) |      \sqrt[n]{x}       |
|   $x^n$ (the nth power of x, x的n次幂)    |          x^n           |
|               $a \uparrow$                |       a \uparrow       |
|              $a \downarrow$               |      a \downarrow      |
|            $a!$ (a factorial)             |           a!           |

### 2.1.2 Relation Operators (关系运算符)

|              Operator              | Code(+$$) |
| :--------------------------------: | :-------: |
|       $\neq$ (Not equal to)        |   \neq    |
| $\approx$ (Approximately equal to) |  \approx  |
|   $\leq$ (less than or equal to)   |   \leq    |
| $\geq$ (greater than or equal to)  |   \geq    |
|         $\lt$ (less than)          |    \lt    |
|        $\gt$ (greater than)        |    \gt    |
|               $\ll$                |    \ll    |
|               $\gg$                |    \gg    |
|               $\lll$               |   \lll    |
|               $\ggg$               |   \ggg    |
|              $\Join$               |   \Join   |
|     $\cong$ (congruent, 全等)      |   \cong   |
|          $\sim$ (similar)          |   \sim    |

## 2.2 累加累乘累除

(1) 累加: 

(1) $y = \sum_{i=1}^{n}{x_i}$: 	y = \sum_{i=1}^{n}{x_i}

$\displaystyle y = \sum_{i=1}^{n}{x_i}$:	 \displaystyle y = \sum_{i=1}^{n}{x_i}

(2) $z =\sum^{x \to \infty}_{y \to 0}{\frac{x}{y}}$:	 y=\sum^{x \to \infty}_{y \to 0}{\frac{x}{y}}

$\displaystyle y=\sum^{x \to \infty}_{y \to 0}{\frac{x}{y}}$:	 \displaystyle y=\sum^{x \to \infty}_{y \to 0}{\frac{x}{y}}

(2) 累乘:

(1) $\prod_{n=1}^{99}{x_n}$: 	\prod_{n=1}^{99}{x_n}

$\displaystyle \prod_{n=1}^{99}{x_n}$:	 \displaystyle \prod_{n=1}^{99}{x_n}

(3) 累除:

(1) $\coprod_{n=1}^{99}{x_n}$:	 \coprod_{n=1}^{99}{x_n}

$\displaystyle \coprod_{n=1}^{99}{x_n}$:	 \displaystyle \coprod_{n=1}^{99}{x_n}

## 2.3 联立

\begin{cases}
	y = a_0x^n + a_1x^{n-1} + a_2x^{n-2} + \cdots+a_n \\
	a_0, a_1,a_2,\cdots,a_n\;are\;constants \\
	n\in Z^+ 
\end{cases}		
$$
\begin{cases}
y = a_0x^n + a_1x^{n-1} + a_2x^{n-2} + \cdots+a_n
\\
a_0, a_1,a_2,\cdots,a_n\;are\;constants
\\
n\in Z^+
\end{cases}
$$

$$
y:\begin{cases} x+y=1 \\ x-y = 0\end{cases}
$$

y : \begin{cases} x+y=1 \\ x-y = 0\end{cases}

## 2.4 Add Commentary(注释)

数学公式中添加注释: \text{文字}

文字注释中仍可以使用内联公式！
$$
y = a_0x^n + a_1x^{n-1} + a_2x^{n-2} + \cdots+a_n,\quad \text{$a_0, a_1,a_2,\cdots,a_n$ are constants}, n\in Z^+
$$
y = a_0x^n + a_1x^{n-1} + a_2x^{n-2} + \cdots+a_n,\quad \text{$a_0, a_1,a_2,\cdots,a_n$ are constants}, n\in Z^+

## 2.5 Common Functions

### 2.5.1 Trigonometric function(trig function, 三角函数)

|           Function           |         Code (+$$)         |
| :--------------------------: | :------------------------: |
|       $\sin 30^\circ$        |       \sin 30^\circ        |
|       $\cos 30^\circ$        |       \cos 30^\circ        |
|       $\tan 30^\circ$        |       \tan 30^\circ        |
|       $\cot 30^\circ$        |       \cot 30^\circ        |
|       $\sec 30^\circ$        |       \sec 30^\circ        |
|       $\csc 30^\circ$        |       \csc 30^\circ        |
|    $arctan{\frac{1}{2}}$     |    arctan{\frac{1}{2}}     |
| $arccot{\frac{\sqrt{3}}{3}}$ | arccot{\frac{\sqrt{3}}{3}} |
|         $arcsin{1}$          |         arcsin{1}          |
|         $arccos{0}$          |         arccos{0}          |
|           $\angle$           |           \angle           |
|            $\bot$            |            \bot            |
|            $\bot$            |            \bot            |

### 2.5.2 Logarithmic function

|  Function   | Code (+$$) |
| :---------: | :--------: |
| $\log_2{8}$ | \log_2{8}  |
|  $\ln{2}$   |   \ln{2}   |
|  $\lg{10}$  |  \lg{10}   |

### 2.5.3 Complexity

|    Function    |  Code (+$$)  |
| :------------: | :----------: |
|   $O(g(x))$    |   O(g(x))    |
| $\Theta(g(x))$ | \Theta(g(x)) |
| $\Omega(g(x))$ | \Omega(g(x)) |

## 2.6 跨行连等

固定等号位置, 使得跨行左对齐: &=
$$
\begin{aligned}
    (f,K^{’}_{x}y+K^{''}_{x}y)_{F}
    &=(f^{'}+f^{''},K^{'}_{x}y+K^{''}_{x}y)_{F}\\
    &=(f^{'},K^{'}_{x}y)_{F}+(f^{''},K^{''}_{x}y)_{F}+(f^{'},K^{''}_{x}y)_{F}+(f^{''},K^{'}_{x}y)_{F}\\
    &=(f^{'},K^{'}_{x}y)_{F}+(f^{''},K^{''}_{x}y)_{F}\\
    &=(f^{'}(x),y)_{Y}+(f^{''}(x),y)_{Y}\\
    &=(f^{'}(x)+f^{''}(x),y)_{Y}\\
    &=(f(x),y)_{Y}\\
    &=(f,K_{x}y)_{F}
\end{aligned}
$$
\begin{aligned}
    (f,K^{‘}_{x}y+K^{''}_{x}y)_{F}
    &=(f^{'}+f^{''},K^{'}_{x}y+K^{''}_{x}y)_{F}\\
    &=(f^{'},K^{'}_{x}y)_{F}+(f^{''},K^{''}_{x}y)_{F}+(f^{'},K^{''}_{x}y)_{F}+(f^{''},K^{'}_{x}y)_{F}\\
    &=(f^{'},K^{'}_{x}y)_{F}+(f^{''},K^{''}_{x}y)_{F}\\
    &=(f^{'}(x),y)_{Y}+(f^{''}(x),y)_{Y}\\
    &=(f^{'}(x)+f^{''}(x),y)_{Y}\\
    &=(f(x),y)_{Y}\\
    &=(f,K_{x}y)_{F}
\end{aligned}

## 2.7 Calculus 

### 2.7.1 Limits

|                          Operator                          |                        Code (+$$)                        |
| :--------------------------------------------------------: | :------------------------------------------------------: |
|                          $\infty$                          |                          \infty                          |
|        $\lim^{x \to \infty}_{y \to 0}{\frac{x}{y}}$        |        \lim^{x \to \infty}_{y \to 0}{\frac{x}{y}}        |
|       $\displaystyle \lim_{x \to \infty}{1 \over x}$       |       \displaystyle \lim_{x \to \infty}{1 \over x}       |
| $\displaystyle \lim^{x \to \infty}_{y \to 0}{\frac{x}{y}}$ | \displaystyle \lim^{x \to \infty}_{y \to 0}{\frac{x}{y}} |

### 2.7.2 Derivative and Differentiation 导数与微分

| Operator | Code (+$$) |
| :------: | :----------------------------------------------------------: |
| $y\prime$ | y\prime |
| $\displaystyle \frac{dy}{dx}$ | \displaystyle \frac{dy}{dx} |
| $\dfrac{\partial f}{\partial x}$ | \dfrac{\partial f}{\partial x} |
| $\frac{du}{dx}\vert _{x=0}$ | \frac{du}{dx}\vert _{x=0} |
| $\dot{a}$ (Derivative of a, 第三种表述方式) | \dot{a} |
| $a \sim 1$ (equivalent infinitesimal) | a \sim 1 |

### 2.7.3 Definite and Indefinite Integrals

|        Operation         |          Code          |
| :----------------------: | :--------------------: |
| $\int^{\infty}_{0}{xdx}$ | \int^{\infty}_{0}{xdx} |
|       $\int{xdx}$        |       \int{xdx}        |
|       $\iint{xdx}$       |       \iint{xdx}       |
|      $\iiint{xdx}$       |      \iiint{xdx}       |
|         $\oint$          |         \oint          |

## 2.8 Linear Algebra

### 2.8.1 Vectors, matrices and determinants

|                             Code                             |                        Figure                         |
| :----------------------------------------------------------: | :---------------------------------------------------: |
| ($$ on both side) + \begin{matrix}  0 & 1 \\  4 & 5 \\  \end{matrix} |    $\begin{matrix} 0 &1 \\ 4 & 5 \\ \end{matrix}$     |
| ($$ on both side) + \begin{pmatrix}  0 & 1 \\  4 & 5 \\  \end{pmatrix} | $ \begin{pmatrix}  0 & 1 \\  4 & 5 \\  \end{pmatrix}$ |
| ($$ on both side) + \begin{vmatrix}  0 & 1 \\  4 & 5 \\  \end{vmatrix} | $\begin{vmatrix}  0 & 1 \\  4 & 5 \\  \end{vmatrix}$  |
| ($$ on both side) + \begin{Vmatrix}  0 & 1 \\  4 & 5 \\  \end{Vmatrix} | $\begin{Vmatrix}  0 & 1 \\  4 & 5 \\  \end{Vmatrix}$  |
| ($$ on both side) + \begin{bmatrix}  0 & 1 \\  4 & 5 \\  \end{bmatrix} | $\begin{bmatrix}  0 & 1 \\  4 & 5 \\  \end{bmatrix}$  |
| ($$ on both side) + \begin{Bmatrix}  0 & 1 \\  4 & 5 \\  \end{Bmatrix} | $ \begin{Bmatrix}  0 & 1 \\  4 & 5 \\  \end{Bmatrix}$ |
|              ($$ on both side) + \overline{abc}              |                   $\overline{abc}$                    |
|           ($$ on both side) + \overrightarrow{abc}           |                $\overrightarrow{abc}$                 |
|                        \lang a,b\rang                        |                   $\lang a,b\rang$                    |
|                      \lvert a,b \rvert                       |                  $\lvert a,b \rvert$                  |
|                      \lVert a,b \rVert                       |                  $\lVert a,b \rVert$                  |
|                     \lbrace a,b \rbrace                      |                 $\lbrace a,b \rbrace$                 |
|           A\bigodot B (Boolean product of A and B)           |                    $ A\bigodot B$                     |
|                        A \bigotimes B                        |                   $A \bigotimes B$                    |

### 2.8.2 How to add lines inside brackets

(1) use {array} instead of {matrix}

(2) 加横线: 在需要加横线的行上加上\hline

(3) 加竖线: 直接在\begin{array}这一statement之后加上{ccc...|ccc...}的statement. The number of c equals the number of columns, and the |is added to the position where you put the line.

\left[ 

\begin{array}{ccc|c}

​		\psi(x) & g(x)  & \cdots & a_{1n} \\

​		\hline

​		a_{21} & a_{22} & \dots  & a_{2n} \\

​		\vdots & \vdots & \ddots & \vdots \\

​		a_{n1} & a_{n2} & ...   & a_{nn}

\end{array}

\right]
$$
\left[ 

\begin{array}{ccc|c}

 	 \psi(x) & g(x)  & \cdots & a_{1n} \\

 	 \hline

  	a_{21} & a_{22} & \dots  & a_{2n} \\

  	\vdots & \vdots & \ddots & \vdots \\

  	a_{n1} & a_{n2} & ...   & a_{nn}

\end{array}

\right]
$$

### 2.8.3 simple application: matrix multiplication

\begin{bmatrix}

​		1 & x_{0} &...   & x_{0}^{n} \\

​		1 & x_{1} &...     & x_{1}^{n} \\

​		&    & \cdots & \\

​		1 & x_{n} & \dots  & x_{n}^{n}

\end{bmatrix}

\begin{bmatrix}

​		a_{0}\\ a_{1}\\ ...\\ a_{n}

\end{bmatrix}=

\begin{bmatrix}

​		y_{0}\\ y_{1}\\ ...\\ y_{n}

\end{bmatrix}
$$
\begin{bmatrix}

  	1 & x_{0} &...   & x_{0}^{n} \\

  	1 & x_{1} &...     & x_{1}^{n} \\

  	&    		& \cdots & \\

  	1 & x_{n} & \dots  & x_{n}^{n}

\end{bmatrix}

\begin{bmatrix}

  	a_{0}\\ a_{1}\\ ...\\ a_{n}

\end{bmatrix}=

\begin{bmatrix}

  	y_{0}\\ y_{1}\\ ...\\ y_{n}

\end{bmatrix}
$$

## 2.9 Number Theory and Combinatorics (组合数学)

|                          Operator                           |      Code(+$$)      |
| :---------------------------------------------------------: | :-----------------: |
|                  $a \mid b$ (a divides b)                   |      a \mid b       |
|                       $a \not\mid b$                        |    a \not\mid b     |
|                       $\dbinom{n}{k}$                       |   $\dbinom{n}{k}$   |
|                        ${n\brace k}$                        |     {n\brace k}     |
|                       $\widehat{abc}$                       |   \widetilde{abc}   |
|       $gcd(x,y)$ (greatest common divider of a and b)       |      gcd(x,y)       |
|        $lcm(a,b)$ (least common multiple of a and b)        |      lcm(a,b)       |
|   $a\;mod\;b$ (remainder when a is divided by b, 求余数)    |      a\;mod\;b      |
|   $a\;div\;b$ (quotient when a is divided by b, 求整除商)   |      a\;div\;b      |
| $C^r_n$ (number of r-combinations of a set with n elements) |        C^r_n        |
|     $a\equiv b (mod\;m)$ (a is congruent to b modulo m)     | a \equiv b (mod\;m) |
| $P^r_n$ (number of r-permutations of a set with n elements) |        P^r_n        |

## 2.10 Probability and Statistics

|                      Operator                       |                   Code(+$$)                   |
| :-------------------------------------------------: | :-------------------------------------------: |
| $p(E\mid F)$ (conditional probability of E given F) |                  p(E\mid F)                   |
|          $\overline{x}$ (mean value of x)           |                 \overline{x}                  |
|         $\widehat{a}$ (estimated parameter)         |                  \widehat{a}                  |
|  $\tbinom{n}{k}$ (binomial coefficient n choose r)  | \tbinom{n}{k} 或 \binom{n}{k} 或 {n\choose k} |
|          $E(X)$ (mathematical expectation)          |                     E(X)                      |
|                  $V(X)$ (variance)                  |                     V(X)                      |
|        $\sigma(x)$ (standard deviation of x)        |                   \sigma(x)                   |

## 2.11 Logical Operators

|                     Operator                     |      Code(+$$)      |
| :----------------------------------------------: | :-----------------: |
|        $\lnot p$ (the negation of p, 非p)        |       \lnot p       |
|        $\forall a \exist b$ (任取b存在b)         | \forall a \exist b  |
|                   $\because a$                   |     \because a      |
|                  $\therefore b$                  |    \therefore b     |
|                      $\vee$                      |        \vee         |
|          $\bigvee$ (disjunction, 析取)           |       \bigvee       |
|                     $\wedge$                     |       \wedge        |
|         $\bigwedge$ (cpnjunction, 结合)          |      \bigwedge      |
|        $\rightarrow$ (implication, 推导)         |     \rightarrow     |
|                  $\Rightarrow$                   |     \Rightarrow     |
| $p \leftrightarrow q$ (biconditional of q and q) | p \leftrightarrow q |
|              $p \Leftrightarrow q$               | p \Leftrightarrow q |
|       $A \bigoplus B$ (Exclusive or, 异或)       |    A \bigoplus B    |
|    $p \equiv q$ (the equivalence of p and q)     |     p \equiv q      |

## 2.12 Set Operators(集合运算符)

|                           Operator                           |              Code(+$$)              |
| :----------------------------------------------------------: | :---------------------------------: |
|                            $\cup$                            |                \cup                 |
|                    $\bigcup$ (Union, 并)                     |               \bigcup               |
|                            $\cap$                            |                \cap                 |
|                  $\bigcap$ (Intersect, 交)                   |               \bigcap               |
|                   $\bigcup_{i=1}^{n} R_i$                    |        \bigcup_{i=1}^{n} R_i        |
|            $\displaystyle \bigcup_{i=1}^{n} R_i$             | \displaystyle \bigcup_{i=1}^{n} R_i |
|         $\subset$ (is a proper subset of, 真包含于)          |               \subset               |
|      $\not\subset$ (is a proper subset of, 不真包含于)       |              \subseteq              |
|        $\not\subseteq$ (is not a subset of, 不包含于)        |            \not\subseteq            |
|                 $\in$ (is a member of, 属于)                 |                 \in                 |
|            $\not\in$ (is not a member of, 不属于)            |               \not\in               |
|          $A \times B$ (Cartesian product, 笛卡尔积)          |             A \times B              |
|             $A-B$ (difference of A and B, 差集)              |                 A-B                 |
|         $C_U{A}$ (complement of A in U, U中A的补集)          |               C_U{A}                |
| $A \bigoplus B$ (symmetric difference of A and B, 对称差, 余集) |            A \bigoplus B            |
|                 $\emptyset$ (emptyset, 空集)                 |              \emptyset              |
|                        $\varnothing$                         |             \varnothing             |

## 2.13 Other Special Symbols

|              Symbol               |            Code(+$$)            |
| :-------------------------------: | :-----------------------------: |
|            $\check{a}$            |            \check{a}            |
|            $\breve{a}$            |            \breve{a}            |
|            $\grave{a}$            |            \grave{a}            |
|            $\acute{a}$            |            \acute{a}            |
|         $\stackrel{x}{y}$         |         \stackrel{x}{y}         |
|         $\overset{z}{y}$          |         $\overset{z}{y}         |
|         $\underset{x}{y}$         |         \underset{x}{y}         |
| $\sideset{^ 1_2}{^3_4}\bigotimes$ | \sideset{^ 1_2}{^3_4}\bigotimes |

# 3 希腊字母

| Number | Lower-case Letters |    Code     | Higher-case Letters |   Code   |
| :----: | :----------------: | :---------: | :-----------------: | :------: |
|   1    |      $\alpha$      |   \alpha    |      $\Alpha$       |  \Alpha  |
|   2    |      $\beta$       |    \beta    |       $\Beta$       |  \Beta   |
|   3    |      $\gamma$      |   \gamma    |      $\Gamma$       |  \Gamma  |
|   4    |      $\delta$      |   \delta    |      $\Delta$       |  \Delta  |
|   5    |     $\epsilon$     |  \epsilon   |     $\Epsilon$      | \Epsilon |
|   6    |      $\zeta$       |    \zeta    |       $\Zeta$       |  \Zeta   |
|   7    |       $\eta$       |    \eta     |       $\Eta$        |   \Eta   |
|   8    |      $\theta$      |   \theta    |      $\Theta$       |  \Theta  |
|   9    |      $\iota$       |    \iota    |       $\Iota$       |  \Iota   |
|   10   |      $\kappa$      |   \kappa    |      $\Kappa$       |  \Kappa  |
|   11   |     $\lambda$      |   \lambda   |      $\Lambda$      | \Lambda  |
|   12   |       $\mu$        |     \mu     |        $\Mu$        |   \Mu    |
|   13   |       $\nu$        |     \nu     |        $\Nu$        |   \Nu    |
|   14   |       $\xi$        |     \xi     |        $\Xi$        |   \Xi    |
|   15   |     $\omicron$     |  \omicron   |     $\Omicron$      | \Omicron |
|   16   |       $\pi$        |     \pi     |        $\Pi$        |   \Pi    |
|   17   |       $\rho$       |    \\rho    |       $\Rho$        |   \Rho   |
|   18   |      $\sigma$      |   \sigma    |      $\Sigma$       |  \Sigma  |
|   19   |       $\tau$       |    \tau     |       $\Tau$        |   \Tau   |
|   20   |     $\upsilon$     |  \upsilon   |     $\Upsilon$      | \Upsilon |
|   21   |       $\phi$       |    \phi     |       $\Phi$        |   \Phi   |
|   22   |       $\chi$       |    \chi     |       $\Chi$        |   \Chi   |
|   23   |       $\psi$       |    \psi     |       $\Psi$        |   \Psi   |
| Bonus  |   $\varepsilon$    | \varepsilon |      $\varphi$      | \varphi  |

# 4 Mermaid绘图

# 5 Phonetic symbols(音标)

Guess what? There is actually no way to type phonetic symbols in Markdown.

So there is one way: copy and paste.

## 5.1 辅音

|        | 双唇音 | [唇齿音 | 齿间音 | 齿龈音 | 齿龈后音 | 硬颚音 | 软颚音 | 声门音 |
| :----: | :----: | :-----: | :----: | :----: | :------: | :----: | :----: | :----: |
|  鼻音  |   m    |         |        |   n    |          |        |   ŋ    |        |
|  塞音  |  p b   |         |        |  t d   |          |        |  k ɡ   |        |
| 塞擦音 |        |         |        | ts dz  |  tʃ dʒ   |        |        |        |
|  擦音  |        |   f v   |  θ ð   |  s z   |   ʃ ʒ    |        |  (x)   |   h    |
|  近音  |        |         |        |   ɹ    |          |   j    | (ʍ) w  |        |
|  边音  |        |         |        |  l,ɫ   |          |        |        |        |

## 5.2 元音

### 5.2.1 单元音短

|      |  前  |  后  |
| :--: | :--: | :--: |
|  闭  |  ɪ   |  ʊ   |
|  中  |  ɛ   |  ʌ   |
|  开  |  æ   |  ɒ   |

### 5.2.2 单元音长

|      |  前  |  央  |  后  |
| :--: | :--: | :--: | :--: |
|  闭  |  i:  |      |  u:  |
|  中  |      |  ɜ:  |  ɔ:  |
|  开  |      |  ɑ:  |      |

### 5.2.3 双元音

|              | 尾音为/ɪ/ | 尾音为/ʊ/ | 中央元音为尾音 |
| :----------: | :-------: | :-------: | :------------: |
| 闭元音为首音 |           |           |     ɪə ʊə      |
| 中元音为首音 |   eɪ ɔɪ   |    əʊ     |       ɛə       |
| 开元音为首音 |    aɪ     |    aʊ     |                |
