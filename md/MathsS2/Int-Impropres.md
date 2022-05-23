# Intégrales Impropres
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
% \global\newcommand{\vec}[1]{\overrightarrow{#1}}
% \global\newcommand{\abs}[1]{\displaystyle\left\lvert {#1} \right\rvert}
$$


$$
I=\int_b^af(x)\ dx\n
\text{
Une intégrale est impropre si l'une des bornes est infinie
}\\
\text{
    ou si la fonction elle même devient infinie
}\n

\text{Exemples : }\n 
I_1=\int_0^{ +\infty}\n
I_2=\int_0^{+\infty}\frac1x\ dx\quad\quad x\in[0,+\infty]\n
I_2= \int_0^1\frac1x\ dx+\int_1^{+\infty}\frac1x\ dx\n
\embrace{
    \ &\cembrace{\ln x}_{0}^{1}=\ln1-\ln0=+\infty\\
    &\cembrace{\ln x}_{1}^{+\infty}=\ln\infty-\ln1=+\infty
}{|}{.}\n
\text{d'où } I_2=+\infty

$$

# SÈries
$$
U_n \text{ : terme général d'une suite}\n
\text{Suite arithmétique (+)}\\
\embrace{\ U_{n+1}=U_n+a\quad\text{avec a la raison}}{|}{.}\n
\text{Suite géométrique (x)}\\
\embrace{\ U_{n+1}=a*U_n\quad\text{avec a la raison}}{|}{.}\n
\text{Fibonacci}\\
\embrace{\ U_{n+2=U_n+U_n{n+1}}}{|}{.}\n
\n
\n
\embrace{
    \ &S_n=\sum u_n\quad\text{Série de terme général }U_n\\
    \ &\text{Si }S_n\text{ converge} \Rrightarrow \lim_{n\rightarrow\infty}U_n=0
}{|}{.}\n
\n
\n
\text{Série géométrique}\\
\boxed{S_N=\sum_{k=0}^Na^k}\n
S_N=1+a+a^2+a^3+\dots+a^N\n
a*S_N=a+a^2+a^3+a^4+\dots+a^{N+1}\n
\Rightarrow S_N-a*S_N=1-a^{N+1}\n
\Rightarrow S_N(1-a)=1-a^{N+1}\n
\Rightarrow S_N = \frac{1-a^{N+1}}{1-a\phantom{^{N+1}}}\n
\n
S_a=\lim_{N\rightarrow\infty}\frac{1-a^{N+1}}{1-a\phantom{^{N+1}}}\n
\text{si } \abs{a}\ge1\rightarrow\ \text{DV}\\
\text{si } \abs{a}\lt1\rightarrow\ S_a=\frac{1}{1-a}\\
\n
\n
\text{Série harmonique}\\
\boxed{
S_n=\sum^\infty_{n=1}\frac1n=1+\frac12+\frac13\dots=\infty}\n
\sum^\infty_{n=1}\ge\int_0^\infty\frac{1}{1+x}\ dx\\
\text{le prof a divagué, rip in peace petite suite}
\n
\n
\text{calculer :}\n
\boxed{
    S=\sum_{n=0}^\infty\pembrace{\frac13}^n
}\n
S=\frac13+\frac19+\frac1{27}
$$
</br>
</br>

Implémentation python d'une suite:
```python
import numpy as np

N=100
U=np.array([(1/3)**n for n in range(1,N)])
S = np.sum(U)
Sc = np.cumsum(U)
```
</br>

$$
\text{calculer :}\n
\boxed{
    \sum_{n=0}^\infty\frac1{n!}
}\n
\embrace{
    \ &e^x=1+\frac{x}{1!}+\frac{x¨2}{2!}+\frac{x^3}{3!}\\
    \ &e^1=e=1+\frac1{1!}+\frac1{2!}+\frac1{3!}\\
    \ &\text{donc la somme vaut }e
}{|}{.}
\n
\n
\text{calculer :}\n
\boxed{
    I=\int_0^1 \ln x\ dx
}\n
\cembrace{x\ln x-x}_{0}^{1}=-1-0=-1\n
\text{car } \lim_{x\rightarrow0}x\ln x=0\n
\n
\n
\text{calculer :}\n
\boxed{
    S=\sum_{k=1}^\infty\frac1{k^2}
}\n
S=\frac11+\frac14+\frac19+\frac1{16}+\frac1{25}+\dots\n
\int_1^\infty f(x+1)\ dx \le \sum_{k=2}^\infty f(k)\le\int_1^\infty f(x)\ dx\n
\text{jai pas eu le temps de copier la suite...}\n
1+\frac12\le S\le2
\n
\n
\text{Résolution exacte de S}\\
\text{1. Sépraration des termes pairs et impairs}\n
S = 1+\frac14+\frac19+\frac1{16}\n
S = \sum_{k=1}^\infty \frac1{k^2}=\sum_{k=1}^\infty \frac1{(2k)^2}+\sum_{k=0}^\infty \frac1{(2k+1)^2}\n
=\frac14\underbrace{\sum_{k=1}^\infty \frac1{k^2}}_{S_1}+\underbrace{\sum_{k=0}^\infty \pembrace{\frac1{2k+1}}^2}_{S_2}\n
S=\frac43S_2
\n
\text{2. Proposition}\n
S_2= \sum_{k=0}^\infty \frac1{(2k+1)^2}=\underbrace{\int_0^1\int_0^1\frac1{1-x^2y^2}\ dxdy}_{I_1}\n
\text{Avec un zeste de magie noire, on obtient : }\n
\frac1{1-x^2y^2}=\sum_{k=0}^\infty\pembrace{x^2y^2}^k\n
\int_0^1\int_0^1(x^2y^2)^k\ dxdy\n
\sum_{k=0}^\infty\ \int_0^1y^{2k}\int_0^1x^{2k}\ dxdy\n
= \sum_{k=0}^\infty\ \int_0^1 \frac{1}{2k+1}y^{2k}dy\n
= \sum_{k=0}^\infty\ \frac{1}{2k+1}*\cembrace{\frac{1}{2k+1}y^{2k+1}}_{0}^{1}\n
= \sum_{k=0}^\infty\ \frac{1}{(2k+1)^2}\n
I_1 = S_2\n
\int_0^1\int_0^1\frac1{1-x^2y^2}\ dxdy\n
\text{on propose le changement de variable}\n
\embrace{
    &x=\frac{\sin\alpha}{\sin\beta}\rightarrow (\alpha,\beta)\in T\\
    &y=\frac{\cos\beta}{\cos\alpha}\quad T=\aembrace{(\alpha,\beta) | 0\lt\alpha\lt\beta\lt \frac{\pi}2}
}{\{}{.}\n
J = \embrace{
    &\frac{\delta x}{\delta \alpha}\quad\frac{\delta x}{\delta\beta}\\
    &\frac{\delta y}{\delta\alpha}\quad\frac{\delta y}{\delta\beta}
    }{|}{|}\n
J = \embrace{
    &\frac{cos\alpha}{sin\beta}\quad\quad\frac{-\sin\alpha\cos\beta}{\sin^2\beta}\\
    &\frac{cos\beta\sin\alpha}{cos^2\alpha}\quad\frac{-sin\beta}{cos\alpha}
}{|}{|}\n

detJ = -1+\frac{cos^2\beta\sin^2\alpha}{cos^2\alpha\sin^2\beta}\n
\abs{detJ} = 1- \frac{cos^2\beta}{cos^2\alpha}\frac{sin^2\alpha}{sin^2\beta}\n
I_1=\int_0^{\frac{\pi}2}\int_0^\alpha d\beta d\alpha\n
I_1=\cembrace{\frac{\alpha^2}{2}}_{0}^{\frac{\pi}2}\n
I_1=S_2=\frac{\pi^2}8
$$
