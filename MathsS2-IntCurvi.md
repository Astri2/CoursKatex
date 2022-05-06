$$
%\global\newcommand{\n}{\\ \ \\}
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
%\global\newcommand{\vec}[1]{\overrightarrow{#1}}
$$
# Exercice Intégrale curviligne

$$
\text{Calculons la valeur des intégrales de la forme : }\int_{C^+} xydx+(x+y)dy\\
\text{Avec}\ C^+\ \text{prenant différentes valeurs}
$$

## 1)
### a)
$$

C^+ = \aembrace{(x,y)\in\R^2\ |\ x^2+y^2=1}\\
\embrace{x=cos\theta\quad\quad &dx = sin\theta d\theta\\ y=sin\theta\quad\quad &dy=cos\theta d\theta}{\{}{.}\n
\begin{split}
I&=\int^{2\pi}_0cos\theta sin\theta\pembrace{-sin\theta d\theta}+\pembrace{cos\theta +sin\theta}cos\theta d\theta\n
&=\int^{2\pi}_0\pembrace{-cos\theta sin^2\theta + cos^2\theta +cos\theta  sin\theta}d\theta\n
&=-\int^{2\pi}_0cos\theta sin^2\theta d\theta + \int^{2\pi}_0cos^2\theta d\theta +\int^{2\pi}_0cos\theta \sin\theta d\theta\n
&=-\cembrace{\frac13sin\theta}_{0}^{2\pi}+\cembrace{\frac12\theta-\frac12sin2\theta}_{0}^{2\pi}+\cembrace{\frac12\sin^2\theta}_{0}^{2\pi}\n
&=0 + \cembrace{\frac12\theta}_{0}^{2\pi}+0=\pi
\end{split}
$$
### b) intégration sur un arc de parabole
$$
\int_{C^+}xydx+(x+y)dy=\pi\n
\text{Arc de parabole}\quad y=x^2\quad A=(-1;1),\ B=(2;4)\n

\text{Trouver une paramétrisation de}\ C^+\n
\embrace{&x(t)=t\quad\quad\quad t\in\cembrace{-1;2}\\&y(t)=t^2}{\{}{.}\n
\embrace{&dx=dt\\&dy=2tdt}{(}{.}\n
\begin{split}
I &=\int^2_{-1}t*t^2+\pembrace{t+t^2}2t\ dt\n
&=\int^2_{-1}\pembrace{t^3+2t^2+2t^3}dt\
\int^2_{-1}\pembrace{3t^3+2t^2}dt\n
&=3 \cembrace{\frac{t^4}4}_{-1}^{2}+ \cembrace{\frac{t^3}3}_{-1}^{2}\n
&= 3\pembrace{\frac{2^4}4-\frac14}+2\pembrace{\frac{Z^3}3-\frac{(-1)^3}3}\n
&=3\pembrace{4-\frac12}+2\pembrace{\frac83+\frac13}\n
&=3*\frac{15}4+\frac{18}3 = \frac{45}4+\frac{24}{4}\n
I&=\frac{69}4
\end{split}
$$

## 3)
$$
\int_C \frac{\pembrace{y+z}dx+\pembrace{z+x}dy+dz}{x^2+y^2}\n
$$
### 1. le long de la droite joingannt A(1,1,1) à B(2,2,2)
$$
\embrace{x=t\\y=t\\z=t}{\{}{.}\quad\Rightarrow\quad\embrace{dx=dt\\dy=dt\\dz=dt}{\{}{.}\n
\begin{split}
    I&=\int_1^2\frac{2tdt+2tdt+dt}{2t^2}\n
    &=\int_1^2\frac{4t+1}{2t^2}dt\n
    &=\int_1^2\frac{2dt}{t}+\int_1^2\frac1{2t^2}dt\n
    &=2 \cembrace{\ln{t}}_{1}^{2}+\frac12 \cembrace{-\frac1t}_{1}^{2}\n
    &=2\ln{2}+\frac12\pembrace{-\frac12+1}\n
    I&=2\ln{2}+\frac14
\end{split}
$$

### 2. Selon une hélice de rayon 1
$$
\embrace{&x=cos\theta\\&y=sin\theta\\&z=\theta}{\{}{.}\quad\theta\in\cembrace{0,2\pi}\Rightarrow\quad \embrace{&dx=-sin\theta d\theta\\&dy=cos\theta d\theta\\&dz=d\theta}{\{}{.}\n
\begin{split}
    I&=\int_0^{2\pi}\frac{(sin\theta+\theta)(-sin\theta d\theta)+(\theta + cos\theta)cos\theta d\theta +d\theta}{1}\n
    &=\int_0^{2\pi}\pembrace{-sin^2\theta-\theta sin\theta+\theta cos\theta+\theta^2\theta+1}d\theta\n
    &=\int_0^{2\pi}\pembrace{cos2\theta+1-\theta\pembrace{sin\theta-cos\theta}}d\theta\n
    &=\int_0^{2\pi}d\theta+\int_0^{2\pi}cos2\theta d\theta - \int_0^{2\pi}\theta\pembrace{sin\theta-cos\theta}d\theta\n
    &=2\pi + 0 -\int_0^{2\pi}\theta\pembrace{sin\theta-cos\theta}d\theta
\end{split}\n\n

\embrace{
    &\embrace{&u=\theta\\&v'=sin\theta-cos\theta}{(}{.}\quad\embrace{&u'=1\\&v=-cos\theta-sin\theta}{.}{.}\n
    &\int uv'=\cembrace{uv}-\int u'v
}{|}{.}\n\n

\begin{split}
    I&=2\pi+\cembrace{\cembrace{\theta(-cos\theta-sin\theta)}_0^{2\pi} +\int_0^{2\pi}\pembrace{cos\theta+sin\theta}d\theta}\n
    &=2\pi + 2\pi\n
    I&=4\pi
\end{split}


$$
