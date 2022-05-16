$$
% \global\newcommand{\n}{\\ \ \\}
% \global\newcommand{\embrace}[3]{
%     \left#2
%         \begin{split}
%             #1
%         \end{split}
%     \right#3
% }
% \global\newcommand{\aembrace}[1]{
%     \embrace{#1}{\{}{\}}
% }
% \global\newcommand{\pembrace}[1]{
%     \embrace{#1}{(}{)}
% }
% \global\newcommand{\cembrace}[1]{
%     \embrace{#1}{[}{]}
% }
$$
<center>TD4 FDPV</center>

# Ex 6
## 4)
$$

D = \aembrace{(x,y) \in \R^2 \ |\ y \ge 0, x-y+1\ge0, x+2y-4\lt0}\n
I = \int\int f(x,y)dxdy\n
$$

1) Représenter le domaine D
<div style="text-align:center">
<img src="https://i.imgur.com/PH9luq6.png" width="300">
</div>


2) Calculer l'intégrale

$$
\text{On segmente l'intervalle d'intégration sur x en 2 portions}\
\int^{x_m}_{-1}\int^{y_1}_{0}xdydx + \int^4_{x_M}\int^{y_2}_0xdydx\n
y_1(x)=x+1\ \ \ y_2(x)=2-\frac{x}{2}\n
\frac{3}{2}x=2-1 \Rightarrow x_m = \frac{2}{3} \Rightarrow y_m=\frac{5}{3}\n
$$

$$
\int\int f(x,y)dxdy \ \ \ |\ \ \ f(x,y)=x\n

\begin{split}
    \hspace{2cm}I &= \int^{\frac{2}{3}}_{-1}x\int^{x+1}_0dydx + \int^4_{\frac{2}{3}}x\int^{2-\frac{x}{2}}_0dydx\n
    &= \int^{\frac{2}{3}}_{-1}x[y]_0^{x+1}dx  + \int^4_{\frac{2}{3}}x[y]_0^{x+1}dx\n
    &= \int^{\frac{2}{3}}_{-1}x(x+1) + \int^4_{\frac{2}{3}}x(2-\frac{x}{2})dx\n
    &= \cembrace{\frac{x^3}{3}+\frac{x^2}{2}}^{\frac{2}{3}}_{-1}+\cembrace{x^2-\frac{x^3}{6}}^4_{\frac{2}{3}}\n
    &= \frac{1}{3}\pembrace{\frac{2}{3}}^3+\pembrace{\frac{2}{3}}^2*\frac{1}{2}\\
    &\quad\quad-\pembrace{\frac{(-1)^3}{3}+\frac{(-1)^2}{2} + 4^2 - \frac{4^3}{6}-\pembrace{\frac{2}{3}}^2-\pembrace{\frac{2}{3}}^3*\frac{1}{6}}\n

    &=\frac{8}{81}+\frac{2}{9}-\pembrace{\frac{-1}{3}+\frac{1}{2}}+16-\frac{32}{3}-\pembrace{\frac{4}{9}-\frac{4}{27}*\frac{1}{3}}\n
    &= \frac{8}{81}+\frac{18}{81}-\frac{1}{6} + 16-\frac{32}{3}-\frac{32}{81}\n
    &= \frac{8*6+18*16-81+16*81*6-32*81*2-32*6}{81*6}\n
    &=\frac{2475}{486} = \frac{275}{54} \approx 5,09
\end{split}
$$
---
## 5)
$$
D = \aembrace{(x,y) \in \R^2\ |\ 0\le x\le 1, x^2\le y\le x}
$$

1) Représenter le domaine D

<div style="text-align:center">
<img src="https://i.imgur.com/2oN9E2i.png" width="300">
</div>

2) Calculer l'intégrale
$$
\begin{split}
    I &=\int\int f(x,y)dxdy\ \ \ |\ \ \ f(x,y) =(x+y)\n
    &= \int^1_0\int^x_{x^2}(x+y)dydx\n
    &=\int^1_0\cembrace{xy+\frac{y^2}{2}}^x_{x^2}dx\n
    &= \int^1_0x^2+\frac{x^2}{2}-\pembrace{x^3+\frac{x^4}{2}}dx\n
    &= \int^1_0\pembrace{\frac{-x^4}{2}-x^3+\frac{3}{2}x^2}dx\n
    &=\cembrace{\frac{-x^5}{10}-\frac{x^4}{4}+\frac{3}{2}\frac{x^3}{3}}^1_0\n
    &= \frac{-1}{10}-\frac{1}{4}+\frac{1}{2}\n
    &=\frac{-2}{20}-\frac{5}{20}+\frac{10}{20}\n
    I&=\frac{3}{20}
\end{split}
$$
---
## 6)
$$
D = \aembrace{(x,y)\in \R^2\ |\ 1\le x\le 2, 0\le xy\le \frac{\pi}{2}}
$$

1) Représenter le domaine D
<div style="text-align:center">
<img src="https://i.imgur.com/PikPPw9.png" width="400">
</div>

2) Calculer l'intégrale

$$
\begin{split}
    I &= \int\int_D f(x,y)dxdy\ \ \ |\ \ \ f(x,y)=cos(x,y)\n
    &= \int^2_1\int^{\frac{\pi}{2x}}_0 cos(xy)dy\  dx\n
    &= \int^2_1\cembrace{\frac{1}{x}sin(xy)}^{\frac{\pi}{2x}}_0dx\n
    &= \int^2_1\frac{1}{x}\sin{\frac{\pi}{2}}\ dx\n
    &= \int^2_1\frac{1}{x}dx\n
    &= \cembrace{ln(x)}^2_1= ln(2)-ln(1)\n 
    I&= ln(2)
\end{split}
$$

---
## 7)
$$
D = \aembrace{(x,y) \in \R^2 \ |\ x\ge 0,\ y\ge 0,\ xy+x+y \le1 }\n
I = \int\int f(x,y)dxdy\n
$$

1) Représenter le domaine D
$$
xy+y+x \le1\n
y(x+1)\le1-x
\n
y\le \frac{1-x}{1+x}
$$
<div style="text-align:center">
<img src="https://i.imgur.com/r3F7img.png" width="300">
</div>

2) Calculer l'intégrale

$$
I = \int\int_D f(x,y)dxdy\ \ \ |\ \ \ f(x,y)=xy\n
= \int^1_0x\int^{\frac{1-x}{1+x}}_0ydy\ dx\n
= \int^1_0\cembrace{\frac{y^2}{2}}^{\frac{1-x}{1+x}}_0 dx\n
= \int^1_0 \frac{1}{2}\pembrace{\frac{1-x}{1+x}}^2xdx\n
= \int^1_0\frac{\pembrace{1+x^2-2x}x}{2\pembrace{1+x^2+2x}}dx\n
= \int^1_0\frac{x^3-2x^2+x}{2x^2+4x+2}dx\n
\text{Décomposition en éléments simples}\n
$$

<div style="text-align:center">
<img src="https://i.imgur.com/zcQ3E1W.png" width="200">
</div>

$$
\begin{split}
    I&= \int^1_0 \frac{x}{2}-2+\frac{4x+2}{\pembrace{1+x}^2}dx\n

    &\quad\embrace{
        &\frac{4x+2}{(1+x)^2} = \frac{\alpha}{1+x}+\frac{\beta}{(1+x)^2}\n
    
        &\frac{\alpha\pembrace{1+x}+\beta}{\pembrace{1+x}^2} =\frac{\alpha x + \alpha + \beta}{\pembrace{1+x}^2}\n
        
        &\embrace{
            &\alpha=4\\
            &\alpha+\beta=2
        }{\{}{.}\quad\Rightarrow\quad\beta=-2
    }{|}{.}\n
    
    
    I&= \int^1_0\frac{x}{2}-2+\frac{4}{1+x}-\frac{2}{\pembrace{1+x}^2}dx\n
    &= \cembrace{\frac{x^2}{4}-2x+4\ ln(1+x)+\frac{2}{1+x}}^1_0\n
    &= \frac{1}{4}-2+4\ ln(2)+\frac{2}{2}-(2)\n
    I&= \frac{1}{4}-3+4\ ln(2) = 4\ ln(2)-\frac{11}{4}
\end{split}
$$

---

