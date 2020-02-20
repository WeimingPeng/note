# LaTeX公式语法  

简要说明：
一下latex其实也是一套完整的文本编辑工具，但是和Markdown不同，他的语法并没有那么简单。会使用markedown简的文字编辑就够了，毕竟对于需要排版的工具大家都使用office办公套件多一些

- tips1
  由于系统的教学都比较复杂，使用例子的方式来说明  
  因为OneNote本身不支持latex语言本笔记迁移至markdown语言书写  

### 参考链接  
https://www.zybuluo.com/knight/note/96093
https://zhuanlan.zhihu.com/p/50667788

## 括号  
()，[]和|都表示它们自己，但是{}因为有特殊作用因此当需要显示大括号时一般使用\lbrace \rbrace来表示。要使括号能够扩住括号内的所用内用需要使用\left 与 \right，此外|有特殊用法，具体见下：
`\left\|{\frac{a}{b} }\right\|_2`用以表示范数
$$
\left\|{\frac{a}{b} }\right\|_2
$$
注意下面两句话的区别：
`f(x,y,z) = 3y^2z ( 3+\frac{7x+5}{1+y^2} )`
$$
f(x,y,z) = 3y^2z ( 3+\frac{7x+5}{1+y^2} )
$$
`f(x,y,z) = 3y^2z \left( 3+\frac{7x+5}{1+y^2} \right)`
$$
f(x,y,z) = 3y^2z \left( 3+\frac{7x+5}{1+y^2} \right)
$$
## 基本运算   
- 加法与减法
加法与减法使用直接相加的方式`a+b` $ a+b $

- 乘除
  点乘：`a \cdot b`结果： $ a \cdot b $
  叉乘：`a \times b` 结果：$a \times b$
  除以：`a \div b`结果： $a \div b$
  分数 `\frac {a}{b}` 结果：$\frac {a}{b}$
  
- 开方 
  `\sqrt{2}$　和　\sqrt[n]{3}`结果为$\sqrt{2}$　和　$\sqrt[n]{3}$

- 省略号 
数学公式中常见的省略号有两种，\ldots表示与文本底线对齐的省略号，\cdots表示与文本中线对齐的省略号。\vdots表示竖直省略号，\ddots表示左斜省略号

  例子：`f(x_1,x_2,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2`
  $$f(x_1,x_2,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2$$
  
- 顶部符号
加^号 \hat 或 \widehat [公式]
加横线 \overline [公式]
加波浪线 \widetilde [公式]
加一个点 \dot{要加点的字母} [公式]
加两个点 \ddot{要加点的字母} [公式]
加箭头 输入 \vec [公式] 
`\vec{abc} \cdot \vec{b}=0`结果：$\vec{abc} \cdot \vec{b}=0$

- 正上下标

下标：`\underset{234}{asd}`
$$
\underset{234}{asd}
$$
  上标`\overset{123}{like}`
$$
\overset{123}{like}
$$
$$
c=\underset{xia}{abc} \overset{cd}{c}
$$
上中下标：`\underset{xia}{\overset{shang}{mid}}`
$$
\underset{xia}{\overset{shang}{mid}}
$$
  注意在Markdown中单行`$\sum_{i=0}^n \frac{1}{i^2}$` 会被解释为$\sum_{i=0}^n \frac{1}{i^2}$而在word编辑器里不会
在markdown中可使用如下命令强制` \sum \limits_{i=0}`结果：$\sum \limits_{i=0}^2$

- 等号对齐
```
\begin{align*} 
v(s) 
&={a+3a^{43} \times r_2}\\ 
&={d+5a}
\end{align*}
```
$$
\begin{align} 
v(s) 
&={a+3a^{43} \times r_2}\\ 
&={d+5a}
\end{align}
$$

- 多行公式
```
$$
st.\left\{ \begin{array}{c}
	\sum_{i=0}^n{y_{ij}\le 1}\\
	H_{aj}\cdot H_{ai}\ge 0\\
	H_{fj}\cdot H_{fi}\ge 0\\
	G_i-G_j=0\\
	A_{kj}-F_{rj}\ge 45\\
	T_{p}^{flownew}=\left\{ \begin{array}{l}
	T_{p}^{flow},\,\,T_{p}^{success}>0\\
	0,\,\,T_{p}^{success}=0\\
	360,\,\,T_{p}^{success}<0\\
\end{array} \right.\\
\end{array} \right. \text{其中}i\in N,\,\,j\in M，k,r\in N
$$
```
$$
st.\left\{ \begin{array}{c}
	\sum_{i=0}^n{y_{ij}\le 1}\\
	H_{aj}\cdot H_{ai}\ge 0\\
	H_{fj}\cdot H_{fi}\ge 0\\
	G_i-G_j=0\\
	A_{kj}-F_{rj}\ge 45\\
	T_{p}^{flownew}=\left\{ \begin{array}{l}
	T_{p}^{flow},\,\,T_{p}^{success}>0\\
	0,\,\,T_{p}^{success}=0\\
	360,\,\,T_{p}^{success}<0\\
\end{array} \right.\\
\end{array} \right. \text{其中}i\in N,\,\,j\in M，k,r\in N
$$
$$
y_i = \left\{ \begin{array}{}
	min, \ x<min \\
	x\\
	max, \ x>max \end{array} \right.
$$


- 设置字体
 \texttt{}
[公式] 打字机
\textsf{}
[公式] 无衬字
\textrm{}
[公式] 罗马
\textbf{}
[公式] 加粗命令
__字体的大小__
Command
\tiny [公式] 
\scriptsize [公式] 
\small [公式] 
\normalsize [公式] 
\large [公式] 
\Large [公式] 
\LARGE [公式] 
\huge [公式] 
\Huge [公式]
- 矩阵
```
S
=\begin{bmatrix}
A & B & \cdots\ &C\\
D & E & \cdots\ & F\\
\vdots & \vdots & \ddots & \vdots \\
G & H & \cdots\ & I\\
\end{bmatrix}
```
$$
S
=\begin{bmatrix}
A & B & \cdots\ &C\\
D & E & \cdots\ & F\\
\vdots & \vdots & \ddots & \vdots \\
G & H & \cdots\ & I\\
\end{bmatrix}
$$
### 123

基本公式
	`\lbrace a^{123} \times b_{456} \rbrace`
$$
\lbrace a^{123}\times b_{456} \rbrace
$$
## 常用的一些符号  
- __常用希腊字母__
``
\alpha　A　\beta　B　\gamma　\Gamma　\delta　\Delta　\epsilon　E 
\varepsilon　　\zeta　Z　\eta　H　\theta　\Theta　\vartheta 
\iota　I　\kappa　K　\lambda　\Lambda　\mu　M　\nu　N 
\xi　\Xi　o　O　\pi　\Pi　\varpi　　\rho　P 
\varrho　　\sigma　\Sigma　\varsigma　　\tau　T　\upsilon　\Upsilon 
\phi　\Phi　\varphi　　\chi　X　\psi　\Psi　\omega　\Omega
``
$$
\alpha　A　\beta　B　\gamma　\Gamma　\delta　\Delta　\epsilon　E 
$$

$$
\varepsilon　　\zeta　Z　\eta　H　\theta　\Theta　\vartheta
$$

$$
\iota　I　\kappa　K　\lambda　\Lambda　\mu　M　\nu　N
$$

$$
\xi　\Xi　o　O　\pi　\Pi　\varpi　　\rho　P 
$$

$$
\varrho　　\sigma　\Sigma　\varsigma　　\tau　T　\upsilon　\Upsilon 
$$

$$
\phi　\Phi　\varphi　　\chi　X　\psi　\Psi　\omega　\Omega
$$

- __关系运算符：__
±：\pm 
×：\times 
÷：\div 
∣：\mid 
∤：\nmid 
⋅：\cdot 
∘：\circ 
∗：\ast 
⨀：\bigodot 
⨂：\bigotimes 
⨁：\bigoplus 
≤：\leq 
≥：\geq 
≠：\neq 
≈：\approx 
≡：\equiv 
∑：\sum 
∏：\prod 
∐：\coprod

- __集合运算符：__
∅：\emptyset 
∈：\in 
∉：\notin 
⊂：\subset 
⊃：\supset 
⊆：\subseteq 
⊇：\supseteq 
⋂：\bigcap 
⋃：\bigcup 
⋁：\bigvee 
⋀：\bigwedge 
⨄：\biguplus 
⨆：\bigsqcup

- __对数运算符：__
log：\log 
lg：\lg 
ln：\ln

- __三角运算符：__
⊥：\bot 
∠：\angle 
30∘：30^\circ 
sin：\sin 
cos：\cos 
tan：\tan 
cot：\cot 
sec：\sec 
csc：\csc

- __微积分运算符：__
′：\prime 
∫：\int 
∬：\iint 
∭：\iiint 
⨌：\iiiint 
∮：\oint 
lim：\lim 
∞：\infty 
∇：\nabla

- __逻辑运算符：__
∵：\because 
∴：\therefore 
∀：\forall 
∃：\exists 
≠：\not= 
≯：\not> 
⊄：\not\subset

- __上加符号运算__
`$
\widehat{x}
$`:$\widehat{x}$
`$
\overrightarrow{x}
$`$\overrightarrow{x}
$
