## 关于MATLAB与LaTeX
MATLAB提供了实时脚本和LaTeX接口，下面通过一个例子简单说明
```syms x
y = sin(x)/(x^2+2*x+4);
latex(y)
```	 
> '\frac{\sin\left(x\righe)}{x^2+x\,x+4}'  

感觉这个可以用来验证代码是否打对，在可以考虑写一段小代码来验证。
* 这里再多说一下实时脚本，和Python的jupyter差不多。