{%hackmd @RintarouTW/DarkTheme %}

# 微積分Calculus

前言:什麼是微積分?
一種工具，利用函數「給定某些值」，「輸出某些值」的特性將問題簡化
微積分被廣泛應用在各種領域，例如統計學，運動學，熱力學，量子力學
微積分是一種基礎工具，其原理就是

「研究『變化率』的學問」

## 函數Function

函數是什麼?一種對應關係  
$輸入一個自變數x，經由對應法則f，得到一個應變數y$

而$y和x的關係記為y=f(x)$  

函數的定義：  
$f:A\to{B}$  
其中  
$A$稱為$f$的定義域(Domain)  
$B$稱為$f$的對應域(Codomain)  

例如:
$x為今天的溫度，經過一連串的運算後，得到一個人的心情指數y=f(x)$

$f$的值域$R_f$是所有函數值的集合

合成函數：  
存在兩個函數  
$f：A\to{B}, g：C\to{D}$  
則  
$f\circ{g}：C\to{D\cap{A}}\to{B}$  
$g\circ{f}：A\to{B\cap{C}}\to{D}$  

> 合成函數的定義域：
> 「所有$x$使得被合成的函數的值都在合成的函數定義域中」

反函數：
$f：A\to{B}$
則  
$f^{-1}：B\to{A}$  
$f^{-1}$滿足  
$(f\circ{f^{-1}})(x)=x$  
$(f^{-1}\circ{f})(x)=x$  
但是$x$的範圍有可能會變

## 極限Limitation

極限的嚴格定義

$\forall\varepsilon>0,\exists 1\ \delta>0,s.t$  
$0<|x-c|<\delta\implies|f(x)-l|<\varepsilon$  
$\iff\displaystyle\lim_{x\to{c}}f(x)=l$  

例子：

試證明$\displaystyle\lim_{x\to{3}}(2x-1)=5$  

### 運算性質

若$\displaystyle\lim_{x\to{a}}f(x)=L,\lim_{x\to{a}}g(x)=M$
則

1. $\displaystyle\lim_{x\to{a}}f(x)\pm g(x)=L\pm M$
2. $\displaystyle\lim_{x\to{a}}f(x)g(x)=LM$
3. $\displaystyle\lim_{x\to{a}}\dfrac{f(x)}{g(x)}=\dfrac{L}{M},M\not={0}$


### 夾擠定理(三明治定理)

若函數在$a$附近有$f(x)\le{g(x)}\le{h(x)}$  
且$\displaystyle\lim_{x\to{a}}f(x)=\lim_{x\to{a}}h(x)=L$  
則$\displaystyle\lim_{x\to{a}}g(x)=L$

### 連續的定義

若函數$f(x)$滿足  $\displaystyle\lim_{x\to{a}}f(x)=f(a),a\in{D_f}$  
則稱函數在$x=a$處連續

常見在$\mathbb{R}$上的連續函數：

1. 多項式函數$f(x)=\displaystyle\sum^{n}_{k=1}a_kx^k$
2. 指數函數$g(x)=a^x,where\ a>0$
3. 對數函數$h(x)=\log_{a}x,where\ a>0\land a\not=1$
4. 正餘弦函數$i(x)=\sin(x),j(x)=\cos(x)$
5. 絕對值函數$k(x)=\displaystyle\sum^{n}_{k=1}|a_kx-b_k|$

連續函數的意義為：在其定義域上連續的函數  
在高中範圍，多項式，指對數，三角函數，絕對值函數皆為連續函數，但三角函數中只有正餘弦在$\mathbb{R}$上連續，其餘函數只能稱為連續函數，因為如$\tan{x}$的定義域為$D=\{x\mid x\neq\dfrac{\pi}{2}+k\pi,k\in\mathbb{Z}\}\cap\mathbb{R}$  
也因此$\tan{x}$在$\mathbb{R}$上不連續，但為連續函數。


### 不定型

1. $\dfrac{0}{0}$型
2. $\dfrac{\infty}{\infty}$型
3. $0\cdot\infty$型
4. $1^{\infty}$型
5. $\infty^{0}$型
6. $\infty-\infty$型

不定型的例子：

1. $\displaystyle\lim_{x\to{0}}\dfrac{\sin{x}}{x}$
2. $\displaystyle\lim_{x\to{0}}|\dfrac{\ln|{x|}}{\cot{x}}|$
3. $\displaystyle\lim_{x\to{0}}\sin{x}\ln{|x|}$
4. $\displaystyle\lim_{x\to{0}}(\dfrac{\sin{x}}{x})^{\ln|x|}$
5. $\displaystyle\lim_{x\to{0}}(\dfrac{1}{x})^x$
6. $\displaystyle\lim_{x\to{0}}(\ln{x}-\log_{3}x)$

如何解不定型？

1. 分子分母同除以分母最大者  
例如：$\displaystyle\lim_{x\to\infty}\dfrac{7x^{2}-34x+3819^{299999}}{x^2+x+3}
\\=\displaystyle\lim_{x\to\infty}\dfrac{\dfrac{7x^2-34x+3819^{299999}}{x^2}}{\dfrac{x^2+x+3}{x^2}}
\\=\displaystyle\lim_{x\to\infty}\dfrac{7-\dfrac{34}{x}+\dfrac{3819^{299999}}{x^2}}{1+\dfrac{1}{x}+\dfrac{3}{x^2}}=7$
2. 根式有理化法
3. 羅畢達法則

漸進線

若函數$f$至少滿足其中一以下性質：

1. $\displaystyle\lim_{x\to{c}}f(x)=\pm\infty$
2. $\displaystyle\lim_{x\to\pm\infty}f(x)=a, a\in\mathbb{R}$
3. $\displaystyle\lim_{x\to\pm\infty}\dfrac{f(x)}{x}=m,m\in\mathbb{R}$

則稱$f$具有漸進線
而滿足1.則稱$x=c$為$f$之垂直漸進線

滿足2.則稱$y=a$為$f$之水平漸進線

滿足3.則稱$y=mx+b$為$f$之斜漸進線，其中$b=\displaystyle\lim_{x\to\pm\infty}(f(x)-mx)$

## 微分Differential

微分是一個動作，而微分是求導函數的過程

導數的定義：  
設函數$f(x)$，$x_0\in D_f$，則$f$在$x=x_0$處的導數定義為  
$\displaystyle\lim_{x\to{x_0}}\dfrac{f(x)-f(x_0)}{x-x_0}$  
而若取$x=x_0+h$則可得$h=x-x_0\to{0}$  
故導數的另一定義為$\displaystyle\lim_{h\to 0}\dfrac{f(x_0+h)-f(x_0)}{h}$

> 觀察：當此極限存在時，必須為$\dfrac{0}{0}$型，故  
> $\displaystyle\lim_{x\to{x_0}}f(x)-f(x_0)=0$  
> 而由此可得當函數在$x=x_0$處可導時，函數在$x=x_0$處必連續(可微必連續)但其逆敘述不成立。

導數的幾何意義：$f$在$x=x_0$處的切線斜率

導函數的定義：  
設函數$f(x)$，若$x\in D_f$，$\displaystyle\lim_{h\to 0}\dfrac{f(x+h)-f(x)}{h}$存在  
則稱此為$f(x)$的導函數，可寫為$f'(x)=\dfrac{d}{dx}f(x)=(f(x))'$

導函數的各種寫法：
$\dfrac{dy}{dx}=\dfrac{df(x)}{dx}=\displaystyle\lim_{x\to{x_0}}\dfrac{f(x)-f(x_0)}{x-x_0}=\displaystyle\lim_{h\to{0}}\dfrac{f(x+h)-f(x)}{h}$

導函數的幾何意義：$f$在其可微點上的切線斜率函數

冪法則

$(x^{p})'=px^{p-1},p\in\mathbb{R}$

證明：
先由正整數證明再推廣到實數。

$n\in\mathbb{N},\displaystyle\lim_{h\to{0}}\dfrac{(x+h)^n-x^n}{h}=nx^{n-1}$  
$pf:$
1.$\displaystyle\lim_{h\to{0}}\dfrac{(x+h)^n-x^n}{h}
\\=\displaystyle\lim_{h\to{0}}\dfrac{x^n+\binom{n}{1}x^{n-1}h+\binom{n}{2}x^{n-2}h^2+\dots+h^n-x^n}{h}
\\=\displaystyle\binom{n}{1}x^{n-1}=nx^{n-1}$

2.$\displaystyle\lim_{h\to{0}}\dfrac{\sqrt[n]{x+h}-\sqrt[n]{x}}{h}=(n\sqrt[n]{x^{n-1}})^{-1}$  
$pf:$
$\displaystyle\lim_{h\to 0}\dfrac{h}{h(\displaystyle\sum^{n-1}_{k=0}\sqrt[n]{(x+h)^{n-1-k}x^k})}=\dfrac{1}{n\sqrt[n]{x^{n-1}}}$

3.$\displaystyle\lim_{h\to 0}\dfrac{\dfrac{1}{x+h}-\dfrac{1}{x}}{h}=\displaystyle\lim_{h\to 0}\dfrac{\dfrac{x-x-h}{(x+h)x}}{h}=\lim_{h\to 0}\dfrac{-1}{x(x+h)}=\dfrac{-1}{x^2}$

以1.2.可以得到$\displaystyle\lim_{h\to 0}\dfrac{(x+h)^{-n}-x^{-n}}{h}$

利用連鎖律得到 $(x^{-n})'=((x^{-1})^{n})'=n(x^{n-1})^{-1}(\dfrac{-1}{x^2})=\dfrac{-n}{x^{1-n+2}}=-nx^{-n-1}$

綜合上述我們已知對於所有整數冪法則皆成立
對於有理數次方，設$n,m\in\mathbb{Z}$
則$(x^{\frac{n}{m}})'=((x^n)^{\frac{1}{m}})'=(\dfrac{1}{m}x^{\frac{n}{m}-1})(nx^{n-1})=\dfrac{n}{m}x^{\frac{n}{m}-1}$

故冪法則對於有理數次方成立

而對於無理數次方則需使用$\exp(x)$函數  
$f(x)=x^q,q\in\mathbb{Q}^c$  
則$f'(x)=(x^q)'=(e^{q\ln{x}})'=\dfrac{qe^{q\ln{x}}}{x}=qx^{q-1}$

因此冪法則對於實數次方皆成立

### 指對數微積分

先定義$e$

$n\in\mathbb{N},\displaystyle\lim_{n\to\infty}(1+\cfrac{1}{n})^n\overset{def}{=}e$

推廣1：$t\in\mathbb{R^+},\displaystyle\lim_{t\to\infty}(1+\dfrac{1}{t})^t=e$  
推廣2：$x\in\mathbb{R},\displaystyle\lim_{x\to{0}}(1+x)^\frac{1}{x}=e$  
推廣3：$\displaystyle\lim_{x\to{\infty}}(1+\dfrac{a}{x})^{bx}=e^{ab}$  
推廣4：$\displaystyle\lim_{h\to{0}}\dfrac{e^h-1}{h}=1$  

證明：  
1:  
$\because\forall t\in\mathbb{R},t>1,\exists n\in\mathbb{N}\ s.t.\ n\le t <n+1
\\\therefore(1+\dfrac{1}{n+1})^n\le(1+\dfrac{1}{t})^t<(1+\dfrac{1}{n})^{n+1},\forall t\in\mathbb{R^+}$

$\implies\displaystyle\lim_{n\to\infty}(1+\dfrac{1}{n+1})^n\le\lim_{t\to\infty}(1+\dfrac{1}{t})^t<\lim_{n\to\infty}(1+\dfrac{1}{n})^{n+1}
\\\implies\dfrac{e}{1}=\displaystyle\lim_{n+1\to\infty}\dfrac{(1+\dfrac{1}{n+1})^{n+1}}{(1+\dfrac{1}{n+1})}\le\lim_{t\to\infty}(1+\dfrac{1}{t})^t<\lim_{n\to\infty}(1+\dfrac{1}{n})^n(1+\dfrac{1}{n})=e\times1$

依據夾擠定理可得$\displaystyle\lim_{t\to\infty}(1+\dfrac{1}{t})^t=e$

2:  
由1得$\displaystyle\lim_{t\to\infty}(1+\dfrac{1}{t})^t=e$  
取$k=-t$，則仿1之證明可得$\displaystyle\lim_{k\to\infty}(1+\dfrac{1}{k})^k=e
\\\implies\displaystyle\lim_{t\to-\infty}(1-\dfrac{1}{t})^{-t}=e$

此時取$x=\dfrac{1}{t}$，則$e=\displaystyle\lim_{\frac{1}{x}\to\pm\infty}(1+x)^{\frac{1}{x}}=\displaystyle\lim_{x\to{0}}(1+x)^{\frac{1}{x}}$  

3:  
先證明$\displaystyle\lim_{x\to\infty}(1+\dfrac{a}{x})^{x}=e^a$  
$\displaystyle\lim_{x\to\infty}(1+\dfrac{a}{x})^{x}=\lim_{\frac{x}{a}\to\infty}(1+\dfrac{a}{x})^{\frac{x}{a}\times{a}}$  
令$\dfrac{x}{a}=y$，則有$\displaystyle\lim_{y\to\infty}(1+\dfrac{1}{y})^{ya}=(\lim_{y\to\infty}(1+\dfrac{1}{y})^{y})^a=e^a$  
故此時$\displaystyle\lim_{x\to\infty}(1+\dfrac{a}{x})^{bx}=(\displaystyle\lim_{x\to\infty}(1+\dfrac{a}{x})^{x})^b=e^{ab}$

4:  
由$e=\displaystyle\lim_{h\to{0}}(1+h)^\frac{1}{h}$，利用極限運算，整理一下式子可以得到  
$\displaystyle\lim_{h\to{0}}e^h=\displaystyle\lim_{h\to{0}}(h+1)$  
$\therefore\displaystyle\lim_{h\to{0}}\dfrac{e^h-1}{h}=1$

### 以自然常數為底的指數函數

$let\ f(x)=e^x$
$f(x)=\dfrac{d^nf(x)}{(dx)^n},n\in\mathbb{N}$
> $f(x)=e^x的n階導數是自己\iff \displaystyle\int f(x)dx=f(x)+c$

$pf:$

$let\ f(x)=e^x$  
$\dfrac{df(x)}{dx}
\\=\displaystyle\lim_{h\to{0}}\dfrac{e^{x+h}-e^x}{h}
\\=e^x\displaystyle\lim_{h\to{0}}\dfrac{e^h-1}{h}
\\=e^x(1)
\\=e^x$

重複微分$n$次皆為自己

---  

### 自然對數

$y=f(x)=e^x$  
$y=g(x)=\ln{x}=\log_{e}x$  
$f(x),g(x)$互為反函數  
$g(x)=\ln{x}$保有所有對數函數的性質  

求一般指數函數$f(x)=a^x,(a>0)$的導數  
$\displaystyle\lim_{h\to{0}}\cfrac{a^{x+h}-a^x}{h}$  
$\because f(x)=a^x=e^{x{\ln{a}}}
\\\therefore f'(x)=(e^{x\ln{a}})\ln{a}=\ln{a}(a^x)$

### 對數函數

換底公式告訴我們所有的對數函數都可換成同底來觀察  
而指對數微積分全繞在$e$這個數上，所有對數函數都可以先化為$\ln{x}$，因此只需討論$\ln{x}$的微分與積分

$\ln{x}$的導數  
$f(x)=\ln{x}, f'(x)=\dfrac{1}{x}$  
$pf:$

$\because f(x)=\ln{x}
\\\therefore e^{f(x)}=x$  
令$g(x)=e^x,h(x)=g(f(x))=x$  
利用連鎖律可得：  
$h'(x)=g'(f(x))f'(x)=e^{f(x)}f'(x)=1
\\\therefore f'(x)=\dfrac{1}{e^{f(x)}}=\dfrac{1}{e^{\ln{x}}}=\dfrac{1}{x}$

推廣：
若$f(x)=\log_{a}x$，求$f'(x)$  
解：
$f(x)=\dfrac{\ln{x}}{\ln{a}}
\\\therefore f'(x)=\dfrac{1}{x\ln{a}}$

---

### 三角函數之微分公式

1. $\dfrac{d}{dx}\sin{x}=\cos{x}$
2. $\dfrac{d}{dx}\cos{x}=-\sin{x}$
3. $\dfrac{d}{dx}\tan{x}=\sec^2{x}$
4. $\dfrac{d}{dx}\cot{x}=-\csc^2{x}$
5. $\dfrac{d}{dx}\sec{x}=\tan{x}\sec{x}$
6. $\dfrac{d}{dx}\csc{x}=-\cot{x}\csc{x}$

$pf:$
只需做正餘弦函數之證明，因為其餘三角函數皆可利用定義表成正餘弦函數

法一：和角公式  
$\dfrac{d}{dx}\sin{x}=\displaystyle\lim_{h\to{0}}\dfrac{\sin{(x+h)}-\sin{x}}{h}
\\=\displaystyle\lim_{h\to{0}}\dfrac{\sin{x}\cos{h}+\cos{x}\sin{h}-\sin{x}}{h}
\\=\displaystyle\lim_{h\to{0}}(\dfrac{\cos{x}\sin{h}}{h}+\dfrac{\sin{x}(\cos{h}-1)}{h})
\\=\displaystyle\lim_{h\to{0}}\cos{x}+\displaystyle\lim_{h\to{0}}\dfrac{\sin{x}(\cos^2{h}-1)}{h(\cos{h}+1)}
\\=\cos{x}+\displaystyle\lim_{h\to{0}}(\dfrac{\sin{h}}{h}\times\dfrac{\sin{x}\sin{h}}{\cos{h}+1})=\cos{x}$

法二：和差化積

$\dfrac{d}{dx}\sin{x}=\displaystyle\lim_{h\to{0}}\dfrac{\sin{(x+h)}-\sin{x}}{h}
\\=\displaystyle\lim_{h\to{0}}\dfrac{2\cos{(\dfrac{2x+h}{2})}\sin{(\dfrac{h}{2})}}{h}
\\=2(\displaystyle\lim_{h\to{0}}\dfrac{\cos{(\dfrac{2x+h}{2})}}{h}\times\displaystyle\lim_{h\to{0}}\dfrac{\sin{(\dfrac{h}{2})}}{h})
\\=2(\dfrac{1}{2}\cos{x})=\cos{x}$

---

證明$\dfrac{d}{dx}\cos{x}=-\sin{x}$

法一：和角公式
$\dfrac{d}{dx}\cos{x}=\displaystyle\lim_{h\to{0}}\dfrac{\cos{(x+h)}-\cos{x}}{h}
\\=\displaystyle\lim_{h\to{0}}\dfrac{\cos{x}\cos{h}-\sin{x}\sin{h}-\cos{x}}{h}
\\=\displaystyle\lim_{h\to{0}}\dfrac{\cos{x}(\cos{h}-1)-\sin{x}\sin{h}}{h}
\\=\displaystyle\lim_{h\to{0}}\dfrac{\cos{x}(\cos{h}-1)}{h}-\sin{x}
\\=\displaystyle\lim_{h\to{0}}\dfrac{\cos{x}(\cos^2{h}-1)}{h(\cos{h}+1)}-\sin{x}=-\sin{x}$

法二：和差化積

$\dfrac{d}{dx}\cos{x}=\displaystyle\lim_{h\to{0}}\dfrac{\cos{(x+h)}-\cos{x}}{h}
\\=\displaystyle\lim_{h\to{0}}\dfrac{-2\sin{(\dfrac{2x+h}{2})}\sin{\dfrac{h}{2}}}{h}
\\=\displaystyle\lim_{h\to{0}}(-\sin{\dfrac{(2x+h)}{2}})=-\sin{x}$

> 利用和角公式化簡過程中需要較多技巧  
而使用和差化積則只需看出
$\displaystyle\lim_{h\to{0}}\dfrac{\sin{\dfrac{h}{2}}}{h}=\dfrac{1}{2}$即可化簡  
因此證明時使用和差化積將可節省時間。  

### 反三角函數

函數：
$f:{A}\to{B}$  
則反函數(不一定存在)：  
$f^{-1}:{B\to{A}}$  

即定義域與值域對調  
其代數意義為「求根」  
幾何意義為關於$y=x$對稱  

比如：  
若$\sin{x}=\dfrac{1}{4},x=?$  

顯然此方程式無法使用任何高中的方法解出，因此需要反三角的表示法。  
$x=\sin^{-1}(\dfrac{1}{4})+2k\pi$  
或  
$x=\pi-\sin^{-1}(\dfrac{1}{4})+2k\pi$  
其中$k\in\mathbb{Z}$

三角函數為已知角度求邊比  
反三角函數為已知邊比求角度  

反三角函數的表示法  
反三角函數可以使用集合表示  

$y=f(x)=\sin^{-1}(x)=\{y\mid x=\sin(y), \dfrac{-\pi}{2}\le{x}\le\dfrac{\pi}{2}\}$
$y=f(x)=\cos^{-1}(x)=\{y\mid x=\cos(y), \dfrac{-\pi}{2}\le{x}\le\dfrac{\pi}{2}\}$
$y=f(x)=\tan^{-1}(x)=\{y\mid x=\tan(y), \dfrac{-\pi}{2}\le{x}\le\dfrac{\pi}{2}\}$
$y=f(x)=\cot^{-1}(x)=\{y\mid x=\cot(y), \dfrac{-\pi}{2}\le{x}\le\dfrac{\pi}{2}\}$
$y=f(x)=\sec^{-1}(x)=\{y\mid x=\sec(y), \dfrac{-\pi}{2}\le{x}\le\dfrac{\pi}{2}\}$
$y=f(x)=\csc^{-1}(x)=\{y\mid x=\csc(y), \dfrac{-\pi}{2}\le{x}\le\dfrac{\pi}{2}\}$

> 若$x$無範圍限制，則會形成一對多的關係，非函數關係。
> 因此必須限定範圍。
  
#### 雜項  

1. $\sin^{-1}x+\cos^{-1}x=\dfrac{\pi}{2}$
2. $\sec^{-1}x+\csc^{-1}x=\dfrac{\pi}{2}$
3. $\tan^{-1}x+\cot^{-1}x=\dfrac{\pi}{2}$

反函數微分法

1. 求出$\dfrac{dx}{dy}$再倒數
2. 由定義$f^{-1}(f(x))=x$做連鎖律
3. 由定義$f(f^{-1}(x))=x$做連鎖律

> $f^{-1}(f(x))=x\not=f(f^{-1}(x))=x$
> 因為$x$的範圍有可能不同

利用法1微分$\sin^{-1}x$

令$x=\sin{y}\implies|x|\le{1}$  
$\dfrac{dx}{dy}=\cos{y}=\sqrt{1-\sin^{2}y}
\\\therefore\dfrac{dy}{dx}=\dfrac{1}{\sqrt{1-\sin^{2}y}}=\dfrac{1}{\sqrt{1-x^2}}$

利用法2微分$\sin^{-1}x$

$\because\sin^{-1}{(\sin{x})}=x\in\mathbb{R}
\\\therefore(\dfrac{d}{dx}\sin^{-1}(\sin{x}))\cos{x}=1
\\\therefore\dfrac{d}{dx}\sin^{-1}(\sin{x})=\dfrac{1}{\cos{x}}
\\令t=\sin{x},x=\sin^{-1}t,|t|\le{1}
\\\therefore\dfrac{d}{dx}\sin^{-1}(t)=\dfrac{1}{\cos{(\sin^{-1}t)}}
\\=\dfrac{1}{\sqrt{1-\sin^{2}{(\sin^{-1}t)}}}
\\=\dfrac{1}{\sqrt{1-\sin^2{t}}}
\\\therefore\dfrac{d}{dx}\sin^{-1}x=\dfrac{1}{\sqrt{1-x^2}},|x|\le{1}$

其餘反三角函數之導函數皆可使用此法一一證出

公式整理：

$\dfrac{d}{dx}\sin^{-1}x=\dfrac{1}{\sqrt{1-x^2}}$  
$\dfrac{d}{dx}\cos^{-1}x=\dfrac{-1}{\sqrt{1-x^2}}$   
$\dfrac{d}{dx}\tan^{-1}x=\dfrac{1}{1+x^2}$   

### 高階導數

表示法：  
$y=f(x)$的$n$階導函數表示為$y^{(n)}=\dfrac{d^n}{dx^n}f(x)=f^{(n)}(x)$  

求法：看出規律，寫成一般項，搭配數列求一般項的技巧。

例：$y=f(x)=\sin{x}$，則$y^{(n)}=?$  
解：  
$y'=\cos{x},y''=-\sin{x},y'''=-\cos{x},y''''=\sin{x}$形成循環  
而$\cos{x}=\sin{(x+\dfrac{\pi}{2})},-\sin{x}=\cos{(x+\dfrac{\pi}{2})},-\cos{x}=-\sin{(x+\dfrac{\pi}{2})}\dots$  
因此可得$y^{(n)}=\sin{(x+\dfrac{n\pi}{2})}$

### 萊布尼茲定理

若兩函數$f(x)$，$g(x)$的$n$階導函數皆存在，則  
$[f(x)g(x)]^{(n)}=\displaystyle\sum_{k=0}^{n}\binom{n}{k}f^{(n-k)}(x)g^{(k)}(x)$

> 與二項式定理有異曲同工之妙，其證明也是仿二項式定理的證明，利用數學歸納法與巴斯卡定理。

### 均值定理

均值定理事實上有三個，分別為洛爾定理，拉格朗日定理，柯西均值定理  
以下分別以定理A,B,C描述  

定理A敘述：  
設函數$f(x)$在$[a,b]$上連續，且在$(a,b)$內各點皆可微  
若$f(a)=f(b)$，則在$\exists c\in(a,b)\ s.t\ f'(c)=0$

定理B敘述：
若函數$f(x)$在$[a,b]$上連續，且在$(a,b)$內各點皆可微  
則$\exists c\in(a,b)\ s.t.\ f'(c)=\dfrac{f(b)-f(a)}{b-a}$

定理C敘述：
設函數$f(x)$，$g(x)$皆在$[a,b]$上連續，且在$(a,b)$內各點皆可微  
則$\exists\xi\in(a,b)\ s.t.\ \dfrac{f(b)-f(a)}{g(b)-g(a)}=\dfrac{f'(\xi)}{g'(\xi)}$

### 微分應用

1. 求$f$在$x=a$處的切線方程式$y=f'(x)(x-a)+f(a)$
2. 求極值
3. 求反曲點

求極值步驟：  
先求$f'(x)$的所有根得到臨界點(Critical point)  
再檢驗在某根$a$附近的凹性或切線斜率正負。  

即若$f'(a)=0$且有一個很小的正數$\varepsilon$使得 $f'(a+\varepsilon)f'(a-\varepsilon)<0$  
則稱在$x=a$時$f(a)$有極值  
此為一階導數檢驗法

若$f'(a)=0$且$f''(a)\not=0$，則在$x=a$時$f(a)$有極值  
此為二階導數檢驗法

而極大值與極小值的區別為  
若$x=a$時$f(x)$有極大值，則在$x=a$附近皆有$f(a)\ge f(x)$  
若$x=a$時$f(x)$有極小值，則在$x=a$附近皆有$f(a)\le f(x)$  

極大值與極小值分別為最大值與最小值的候選點。  

最大值與最小值的定義為  

若$x=a$時$f(x)$有最大值，則$\forall x\in D_f\implies f(x)<f(a)$  
若$x=a$時$f(x)$有最小值，則$\forall x\in D_f\implies f(x)>f(a)$  

> 極值產生於峰點，谷點，尖點，斷點。

求反曲點步驟

先找$f''(x)=0$，再判別有無重根

即若$f''(a)=0$，且$f'''(a)\not= 0$，則$(a,f(a))$為$f(x)$的反曲點

### 羅畢達定理

若兩函數$f(x),g(x)$滿足以下性質：  
$c\in{D_f\cap D_g}
\\\displaystyle\lim_{x\to{c}}f(x)=f(c)=g(c)=\lim_{x\to{c}}g(x)=0$  
且兩函數在$x=c$附近均可微
則$\displaystyle\lim_{x\to{c}}\dfrac{f(x)}{g(x)}=\lim_{x\to{c}}\dfrac{f'(x)}{g'(x)}$

證明：  
$\displaystyle\lim_{x\to{c}}\dfrac{f(x)}{g(x)}=\lim_{x\to{c}}\dfrac{f(x)-f(c)}{g(x)-g(c)}=\lim_{x\to{c}}\dfrac{\dfrac{f(x)-f(c)}{x-c}}{\dfrac{g(x)-g(c)}{x-c}}=\lim_{x\to{c}}\dfrac{f'(x)}{g'(x)}$

推廣：對於不定型$\dfrac{\infty}{\infty},0\times\infty,\infty^{0},1^{\infty}$此定理皆適用

考慮$f(x),g(x)$分別滿足以下不同條件  

1. $\displaystyle\lim_{x\to{c}}f(x)=\pm\infty,\displaystyle\lim_{x\to{c}}g(x)=\pm\infty$

2. $\displaystyle\lim_{x\to{c}}f(x)=0,\displaystyle\lim_{x\to{c}}g(x)=\pm\infty$

3. $\displaystyle\lim_{x\to{c}}f(x)=1,\displaystyle\lim_{x\to{c}}g(x)=\pm\infty$

與其極限  

1. $\displaystyle\lim_{x\to{c}}\dfrac{f(x)}{g(x)}$

2. $\displaystyle\lim_{x\to{c}}f(x)g(x)$

3. $\displaystyle\lim_{x\to{c}}(f(x))^{g(x)}$

則對於條件1.與極限1.而言：  
$\displaystyle\lim_{x\to{c}}\dfrac{f(x)}{g(x)}=\displaystyle\lim_{x\to{c}}\dfrac{\dfrac{1}{g(x)}}{\dfrac{1}{f(x)}}$，此時令二新函數$h(x)=\dfrac{1}{g(x)},i(x)=\dfrac{1}{f(x)}$  
而$\because\displaystyle\lim_{x\to{c}}f(x)=\pm\infty,\displaystyle\lim_{x\to{c}}g(x)=\pm\infty
\\\therefore\displaystyle\lim_{x\to{c}}h(x)=\lim_{x\to{c}}i(x)$  
則$\displaystyle\lim_{x\to{c}}\dfrac{h(x)}{i(x)}$為$\dfrac{0}{0}$型

對於條件2.與極限2.而言：  
$\displaystyle\lim_{x\to{c}}f(x)g(x)=\lim_{x\to{c}}\dfrac{f(x)}{\dfrac{1}{g(x)}}$  
令$h(x)=\dfrac{1}{g(x)}$  
$\because\displaystyle\lim_{x\to{c}}f(x)=0,\displaystyle\lim_{x\to{c}}g(x)=\pm\infty
\\\therefore\displaystyle\lim_{x\to{c}}h(x)=0
\\\implies\displaystyle\lim_{x\to{c}}\dfrac{f(x)}{h(x)}$為$\dfrac{0}{0}$型

對於條件2與極限3.而言：

$\displaystyle\lim_{x\to{c}}(g(x))^{f(x)}=\lim_{x\to{c}}e^{(\ln{g(x)})f(x)}$  
此時令$h(x)=\ln{g(x)}$但$g(x)>0$則$\displaystyle\lim_{x\to{c}}h(x)=\displaystyle\lim_{x\to{c}}\ln{g(x)}=\infty$  
可發現指數為$0\times\infty$型，故可化簡為$\dfrac{0}{0}$型  

## 積分Intergration

積分是用來求曲線下面積的一種工具

### 定積分

定義：  
設$y=f(x)$在閉區間$[a,b]$上連續  
$S$是$[a,b]$的任意一種分割  
得到$n$個區間$[x_{k-1},x_k],k\in\mathbb{n}$  
且$a=x_0<x_1<\dots<x_{n-1}<x_n=b$  
若於每一區間上取一$\varepsilon_k$   
使得$x_k\le\varepsilon_k\le{x_{k+1}}$  
再取一$\delta=\max\{x_1-x_0,x_2-x_1,x_3-x_2\dots,x_{n}-x_{n-1}\}$  
則定義  
$\displaystyle\lim_{\delta\to{0}}\sum_{k=0}^{n}f(\varepsilon_{k})(x_{k+1}-x_k)=\displaystyle\lim_{\delta\to{0}}\sum_{k=0}^{n}f(\varepsilon_{k})(\Delta{x_{k}})=\displaystyle\int_{a}^{b}f(x)dx$

> 為何$\delta=\max\{x_1-x_0,x_2-x_1,x_3-x_2\dots,x_{n}-x_{n-1}\}?$  
> 答：若整個分割中最大塊的區間長度趨近於0，那麼其餘的分割區間長度也必趨近於0。

### 等分

由定積分的嚴格定義，可取將$[a,b]$n等分的分割$S$  
即$|[x_k-1,x_k]|=|[x_k,x_{k+1}]|,\forall k\in\mathbb{N}$

可得$\displaystyle\sum_{k=1}^nf(\dfrac{k}{n})\dfrac{b-a}{n}\approx\int_{a}^{b}f(x)dx$

而由定義，當$\delta\to 0$時，$n\to\infty$   
故$\displaystyle\lim_{n\to\infty}\sum_{k=1}^nf(\dfrac{k}{n})\dfrac{b-a}{n}=\int_{a}^{b}f(x)dx$

上和與下和：

$\displaystyle\sum_{k=1}^nf(\dfrac{k}{n})\dfrac{b-a}{n}$稱為上和$M$

$\displaystyle\sum_{k=0}^{n-1}f(\dfrac{k}{n})\dfrac{b-a}{n}$稱為下和$m$

### 微積分基本定理

反導函數：若$F'(x)=f(x)$，則稱$F(x)$為$f(x)$的一個反導函數

1. 若$F'(x)=f(x)$，則$F(x)+c=\displaystyle\int f(x)dx$，$c$是一個常數
2. $若F(x)$是$f(x)$的一個反導函數，則$\displaystyle\int_a^bf(x)dx=F(b)-F(a)$

$pf:$  
先證明2.  
$\because F(x)$是$f(x)$的一個反導函數$\therefore F'(x)=f(x)$  
而$\displaystyle\int_{a}^bf(x)dx=\lim_{\delta \to 0}\sum_{k=1}^{n}f(\varepsilon_k)(x_{k+1}-x_k)$

又由均值定理：若$f(x)$在$(a,b)$上連續，則$\exists c\in(a,b)\ s.t.\ f'(c)=\dfrac{f(b)-f(a)}{b-a}$

而此時對於區間$[x_{k},x_{k+1}]$，也有一常數$c\in(a,b)$使得$F'(c)=\dfrac{F(x_{k+1})-F(x_k)}{x_{k+1}-x_k}$，則此時取$\varepsilon_k$為此常數，則

$\displaystyle\int_{a}^{b}f(x)dx=\lim_{\delta\to 0}\sum^{n}_{k=1}f(\varepsilon_k)(x_{k+1}-x_k)
\\=\displaystyle\lim_{\delta\to 0}\sum^{n}_{k=1}F'(\varepsilon_k)(x_{k+1}-x_k)
\\=\displaystyle\lim_{\delta\to 0}\sum^{n}_{k=1}\dfrac{F(x_{k+1})-F(x_k)}{x_{k+1}-x_k}(x_{k+1}-x_k)=\lim_{\delta\to 0}\sum^{n}_{k=1}[F(x_{k+1})-F(x_k)]=F(b)-F(a)$

再證明1.  
因為已知$\displaystyle\int_a^bf(x)dx=F(b)-F(a)$  
因此$\displaystyle\int^{x}_{a}f(x)dx=F(x)-F(a)$  
而當下界也不確定時，即$\displaystyle\int f(x)dx=F(x)+C$  
微積分基本定理從而得證。  

### 運算性質  

1. $\displaystyle\int_{a}^{b}f(x)dx=\int^c_af(x)dx+\int^b_cf(x)dx$
2. $\displaystyle\int_{a}^{b}f(x)dx=-\int_b^af(x)dx$
3. 若$f(x)$為奇函數，則$\displaystyle\int^a_{-a}f(x)dx=0$。
4. 若$f(x)$為偶函數，則$\displaystyle\int^a_{-a}f(x)dx=2\int^a_{0}f(x)dx$
5. $\displaystyle\int_a^af(x)dx=0$
6. $\displaystyle\int cf(x)dx=c\int f(x)dx$
7. $\displaystyle\int [f(x)\pm g(x)]dx=\int f(x)dx\pm\int g(x)dx$
8. $\displaystyle\int f(x)dx=\int f(u)du=\int f(t)dt$

### 積分方法

### 變數代換

設$F(x)$為$f(x)$的一個反導函數，且$g(x)$可微

$\because(F(g(x)))'=F'(g(x))g'(x)=f(g(x))g'(x)
\\\therefore\displaystyle\int f(g(x))g'(x)dx=F(g(x))$

而因為可令$u=g(x)$，則$du=g'(x)dx$，故稱為變數代換

例如
$\displaystyle\int\dfrac{x}{\sqrt{1-x^2}}dx
\\\overset{u=1-x^2}{=}\displaystyle\dfrac{1}{2}\int\dfrac{du}{\sqrt{u}}=\dfrac{1}{2}(-2\sqrt{1-x^2})+\text{C}=-\sqrt{1-x^2}+\text{C}$

### 分部積分

由微分乘則$(f(x)g(x))'=f'(x)g(x)+f(x)g'(x)$
可得$\displaystyle\int(f(x)g(x))'dx=\int [f'(x)g(x)+f(x)g'(x)]dx$
$\implies f(x)g(x)=\displaystyle\int f(x)dg(x)+\int g(x)df(x)
\\\therefore\displaystyle\int f(x)dg(x)=f(x)g(x)-\int g(x)df(x)$

例如
$\displaystyle\int e^x\cos{x}dx$  
令$dv=e^xdx,u=\cos{x}$  
$\therefore du=-\sin{x}dx,v=e^x$  
$\implies\displaystyle\int e^x\cos{x}dx=e^x\cos{x}+\int e^x\sin{x}dx
\\=\displaystyle e^x\cos{x}+(e^x\sin{x}-\int e^{x}\cos{x}dx)
\\\implies\displaystyle\int e^x\cos{x}dx=\dfrac{e^{x}(\cos{x}+\sin{x})}{2}+\text{C}$

### 三角代換

使用時機

1. 看到$\sqrt{a^2-x^2}$令$x=\sin{u}$
2. 看到$\sqrt{x^2-a^2}$令$x=\sec{u}$
3. 看到$a^2+x^2$令$x=\tan{u}$

例如
$\displaystyle\int\sqrt{1-x^2}dx$
令$x=\sin{u},dx=\cos{u}du$
則原式
$\displaystyle\int\cos^2{u}du=\int\dfrac{1+\cos{2u}}{2}du=\dfrac{u}{2}+\dfrac{-\cos{2u}}{4}+\text{C}=\dfrac{\sin^{-1}{x}}{2}-\dfrac{x\sqrt{1-x^2}}{2}+\text{C}$

### 部分分式

當遇到有理函式時，如$\dfrac{p(x)}{q(x)}$，其中$p(x),q(x)$皆為實係數多項式，則可使用此積分方法

例如：  
$\displaystyle\int\dfrac{1}{x^2-1}dx=?$  
令$\dfrac{1}{(x+1)(x-1)}=\dfrac{A}{x+1}+\dfrac{B}{x-1}$  
則$1=A(x-1)+B(x+1)$  
故$\begin{cases}A=\dfrac{-1}{2}\\B=\dfrac{1}{2}\end{cases}$  
因此$\displaystyle\int\dfrac{1}{x^2-1}dx=\int\dfrac{-1}{2(x+1)}dx+\int\dfrac{1}{2(x-1)}dx=\dfrac{1}{2}(\ln|\dfrac{x-1}{x+1}|)+\text{C}=-\tanh^{-1}x+\text{C}$


### 基本函數積分公式

### 冪函數

$\displaystyle\int x^{p}dx=\dfrac{x^{p+1}}{p+1}+\text{C},p\in\mathbb{R}-\{-1\}$

$\displaystyle\int\dfrac{1}{x}dx=\ln|x|+\text{C}$

### 指對數

$\displaystyle\int e^{cx}dx=\dfrac{e^{cx}}{c}+\text{C},c\in\mathbb{R}-\{0\}$

$\displaystyle\int\log_axdx=\dfrac{1}{x\ln{a}}+\text{C}$

### 三角函數

由微積分基本定理能夠輕易得出正餘弦函數的不定積分

$\because\dfrac{d}{dx}\sin{x}=\cos{x},\dfrac{d}{dx}\cos{x}=-\sin{x}
\\Using\ The\ Fundemental\ Theorem\ of \ Calculus
\\\displaystyle\int\cos{x}dx=\sin{x}+c
\\\displaystyle\int\sin{x}dx=-\cos{x}+c$

> 正餘弦函數積分相當於圖形向右平移$\dfrac{\pi}{2}$後，在$y$方向加上某個常數。
> 但正餘切和正餘割函數則較複雜

$\displaystyle\int\tan{x}dx=-\ln{|\cos{x}|}+c$
$\displaystyle\int\sec{x}dx=\ln{|\tan{x}+\sec{x}|}+c$

$pf:
\\\displaystyle\int\tan{x}dx
\\=\displaystyle\int\dfrac{\sin{x}}{\cos{x}}dx$
令
$u=\cos{x}$
$\therefore du=-\sin{x}dx$

$\displaystyle\int\tan{x}dx
\\=\displaystyle\int\dfrac{\sin{x}}{\cos{x}}\dfrac{du}{-\sin{x}}
\\=\displaystyle\int\dfrac{-1}{u}du
\\=-\ln{|u|}
\\=-\ln{|\cos{x}|}+c$

$\displaystyle\int\sec{x}dx
\\=\displaystyle\int\dfrac{\sec{x}(\sec{x}+\tan{x})}{(\sec{x}+\tan{x})}dx
\\=\displaystyle\int\dfrac{\sec^2{x}+\sec{x}\tan{x}}{\sec{x}+\tan{x}}dx$

令$u=\sec{x}+\tan{x}\therefore du=\tan{x}\sec{x}+\sec^2{x}$

$\therefore\displaystyle\int\dfrac{\sec^2{x}+\sec{x}\tan{x}}{\sec{x}+\tan{x}}dx=\displaystyle\int\dfrac{du}{u}=\ln{|u|}=\ln{|\sec{x}+\tan{x}|}+c$


### 高次三角函數與其高次乘積

1. $\displaystyle\int\sin^{n}xdx=\dfrac{1}{n}(-\sin^{n-1}x\cos{x}+(n-1)\int\sin^{n-2}xdx)$
2. $\displaystyle\int\sec^{n}xdx=\dfrac{1}{n-1}(\sec^{n-2}x\tan{x}+(n-2)\int\sec^{n-2}xdx)$
3. $\csc^{n}x$

只證明1.其餘可利用類似想法完成  
皆為先分部積分再利用平方關係化為遞迴關係。  
$\displaystyle\int\sin^{n}xdx=-\int\sin^{n-1}xd\cos{x}=-\sin^{n-1}x\cos{x}+\int\cos{x}d\sin^{n-1}x$  
又
$d\sin^{n-1}x=(n-1)\sin^{n-2}x\cos{x}dx$  
$\displaystyle\therefore\int\sin^{n}xdx\\=-\sin^{n-1}x\cos{x}+(n-1)\int\cos^2{x}\sin^{n-2}xdx\\=-\sin^{n-1}x\cos{x}+(n-1)\int(1-\sin^2{x})\sin^{n-2}xdx\\=-\sin^{n-1}x\cos{x}+(n-1)(\int\sin^{n-2}xdx-\int\sin^{n}xdx)
\\\implies\displaystyle\int\sin^{n}xdx=\dfrac{1}{n}(-\sin^{n-1}x\cos{x}+(n-1)\int\sin^{n-2}xdx)$

其餘可利用平方關係與以下公式化簡

1. $\sin^{n}x\cos^{m}x$

先討論奇偶  
一奇一偶 奇減一  
二偶 用平方換  
二奇 cos減一  
次方相同時 二倍角  
$\displaystyle\int\sin^{2n+1}x\cos^{2m}xdx=-\int\sin^{2n}x\cos^{2m}xd\cos{x}=-\int(1-\cos^{2}x)^n\cos^{2m}xd\cos{x}$  
令$u=\cos{x}$，即求$\displaystyle\int(1-u^2)^nu^{2m}du$  
以二項式定理展開後得：  
$-\displaystyle\int[\sum_{k=0}^{n}(-1)^k\binom{n}{k}u^{2m+2k}]du
\\=\displaystyle\sum_{k=0}^{n}[(-1)^{k+1}\binom{n}{k}\int{u^{2m+2k}}du]
\\=\displaystyle\sum_{k=0}^{n}[(-1)^{k+1}\binom{n}{k}\dfrac{\cos^{2m+2k+1}x}{2m+2k+1}]+C
\\\therefore\displaystyle\int\sin^{2n+1}x\cos^{2m}xdx=\sum_{k=0}^{n}[(-1)^{k+1}\binom{n}{k}\dfrac{\cos^{2m+2k+1}x}{2m+2k+1}]+C$  
$\displaystyle\int\sin^{2n}x\cos^{2m}x=\int(1-\cos^{2}x)^n\cos^{2m}xdx=\int\sum_{k=0}^{n}(-1)^k\cos^{2k+2m}xdx$  
再使用高次三角函數漸化式化簡。  
2. $\sec^{n}x\tan^{m}x$  

3. $\csc^{n}x\cot^{m}x$  

多種三角函數合在一起時可使用$\tan{2x}$萬能公式
化為部分分式再積分

### 其他雜項

$\displaystyle\int x^ne^{mx}dx=\sum^{n}_{k=0}\dfrac{(-1)^{k}}{m^{k+1}}\binom{n}{k}k!x^{n-k}e^{mx}+C,n,m\in\mathbb{N}$  
$\displaystyle\int\sin{ax}\cos{bx}dx=\dfrac{-1}{2}(\dfrac{\cos{((a+b)x)}}{a+b}+\dfrac{\cos{((a-b)x)}}{a-b})+C,a,b\in\mathbb{R}\land a^2+b^2\not=0\land a\not=b$  

### 積分應用

### 求弧長

一小段弧長可近似為直線，故$dl=\sqrt{(dx)^2+(dy)^2}$  
故函數$f(x)$在區間$[a,b]$之弧長為
$\displaystyle\int_{a}^{b}dl=\int_{a}^{b}\sqrt{1+(\dfrac{dy}{dx})^2}dx$

推廣：  
參數式$\begin{cases}x=x(t)\\y=y(t)\end{cases}\quad t\in[a,b]$  
其弧長為
$\displaystyle\int_{a}^{b}\sqrt{(dx)^2+(dy)^2}=\int_{a}^{b}\sqrt{(\dfrac{dx}{dt})^2+(\dfrac{dy}{dt})^2}dt$

### 求曲線下面積

函數$f(x)$在$[a,b]$上連續，則其與$x$軸所圍成的面積為
$\displaystyle\int^{b}_{a}|f(x)|dx$

例如：
求$f(x)=\sqrt{(x+1)(x-1)}$與$\begin{cases}(x-3)(x-6)=0\\y=0\end{cases}$所圍成的圖形面積

先作圖，確定圖形形狀，上下界之間有根需分段積分，負區變號
![what](https://i.imgur.com/BDoPh36.png)

再寫積分式

$\displaystyle\int^{6}_{3}|\sqrt{x^2-1}|dx=\int^{6}_{3}\sqrt{x^2-1}dx$

利用三角代換  
令$x=\sec{u},dx=\tan{u}\sec{u}du$
則原式變為  
$\displaystyle\int^{6}_{3}\tan^2{u}\sec{u}du$
先求其不定積分  
$\displaystyle\int\sec^{3}{u}-\sec{u}du=\int\sec^{3}{u}du-\int\sec{u}du\\
=\displaystyle\dfrac{1}{2}\tan{u}\sec{u}+\dfrac{1}{2}\int\sec{u}du-\int\sec{u}du
\\=\dfrac{1}{2}\tan{u}\sec{u}-\dfrac{1}{2}\ln{|\sec{u}+\tan{u}|}+C$

而因為$x=\sec{u}\therefore\tan{u}=\sqrt{x^2-1}$  
因此$\displaystyle\int\sqrt{x^2-1}dx=\dfrac{1}{2}(x\sqrt{x^2-1}-\ln{|x+\sqrt{x^2-1}|})+C$

將上下界代入後
$\displaystyle\int^{6}_{3}\sqrt{x^2-1}dx=3\sqrt{35}-3\sqrt{2}+\ln{\sqrt{\dfrac{3+2\sqrt{2}}{6+\sqrt{35}}}}$即為所求

### 定積分求體積

若有一面積函數$A(x)$，則其與$(x-a)(x-b)=0$兩平面所圍成的體積為  
$|\displaystyle\int^{b}_{a}A(x)dx|$

例如：
求證三角錐體積$V$為$\dfrac{A_{0}h}{3}$，其中$A_0$，$h$分別為三角錐之底面積，高

$pf:$

![what](https://i.imgur.com/V9VDcFe.png)

### 求旋轉體體積

旋轉體體積定義：$f(x)$繞$x$軸旋轉所圍成的體積

1. 圓盤法

利用定積分求體積的方法，先寫出面積函數，再做積分  
面積函數為每個圓盤的面積，即以$|y|$值為半徑的圓面積$\pi{y^2}$  
則函數$y=f(x)$繞$x$軸旋轉與$(x-a)(x-b)=0$兩平面所圍成之體積為  
$|\displaystyle\int_{a}^{b}\pi{y^2}dx|$  

2. 套筒法

此法通常使用於$y=f(x)$繞$y$軸旋轉的體積  
即求$y=f(x)$繞$y$軸旋轉與$(y-a)(y-b)=0$所形成的體積  
作法為：  
先將每個小中空圓柱面的面積函數算出，再將這些小圓柱體面積加起來即為所求  
故所求為$|\displaystyle\int_{a}^{b}2\pi xydx|$

變化型：

有兩函數$f(x)$與$g(x)$，求其繞$x$軸與$(x-a)(x-b)=0$所形成的體積

解：  
$|\displaystyle\int_{a}^{b}\pi(f(x)-g(x))^2dx|$

### 求旋轉體表面積

求$f(x)$繞$x$軸與$(x-a)(x-b)=0$所形成的旋轉體表面積$A_r$  
面積就是弧長的積分  
因此先將弧長算出後再求出旋轉體積分  
$|\displaystyle\int_{a}^{b} 2\pi f(x) dl|$  
其中$dl=\sqrt{1+(\dfrac{dy}{dx})^2}dx$  
故$A_r=|\displaystyle\int_{a}^{b} 2\pi f(x) \sqrt{1+(f'(x))^2}dx|$  
