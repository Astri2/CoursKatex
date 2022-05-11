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
$$
le td1
$$
\begin{split}
    &f:\R^2\rightarrow\R\n

    &f(x,y)=\frac{\pembrace{x+y}^2}{x^2+y^2}\n

    &\vec{\nabla}f=\pembrace{
        &\frac{\delta f}{\delta x}\\
        &\frac{\delta f}{\delta y}
    }\n

    &\text{lignes de niveau: f(x,y) = cst}\\

    &\text{gradient perpendiculaires aux lignes de niveaux}\\
    &\text{Si }\vec{\nabla}f(x,y)=\vec{0}\Rightarrow\text{ (x,y) est un pt critique}\\
    &\vec{\nabla}f\text{ pointe vers la ou ca monte le plus}
\end{split}
$$

# oui
$$
\begin{split}
    &f(x_0+h,y_0+k)=f(x_0,y_0)+\frac12\pembrace{rh^2+2shk+tk^2}+||\epsilon(h,k)||^2\epsilon(h,k)\n

    &r=\frac{\delta^2f}{\delta x^2}\quad s=\frac{\delta^2f}{\delta x\delta y}=\frac{\delta^2f}{\delta y\delta x}\quad t=\frac{\delta^2 f}{\delta y^2}\n
    
    &\text{si } f(x_0+h,y_0+k) \ge f(x_0,y_0)\quad \forall(h,k)\Rightarrow (x_0,y_0)\text{ est un min}\n

    &\text{si } f(x_0+h,y_0+k) \le f(x_0,y_0)\quad \forall(h,k)\Rightarrow (x_0,y_0)\text{ est un max}\n
\end{split}
$$

$$
\begin{split}
    q(h,k)&=rh^2+2hk+tk^2\n
    
    &=r\pembrace{h^2+\frac{2shk}{r}+\frac{tk^2}{r}}\n
    
    &=r\pembrace{\pembrace{h+\frac{sk}{r}}^2-\frac{s^2k^2}{r^2}+\frac{tk^2}{r}}\n

    &=r\pembrace{\pembrace{h+\frac{sk}{r}}^2+k^2\pembrace{\frac{t}{r}-\frac{s^2}{r^2}}}\n

    &=r\pembrace{\pembrace{h+\frac{sk}{r}}^2+k^2\pembrace{\frac{rt-s^2}{r^2}}}\n
\end{split}
$$
| s | r  | t  | q  | conclusion |
|:-:|:--:|:--:|:--:|:----------:|
| 0 | >0 | >0 | >0 |max local   |
| 0 | <0 | <0 | <0 |min local   |
| 0 | >0 | <0 | ?  |point selle |
| 0 | <0 | >0 | ?  |point selle |  

| s  | r  | t | s²-rt| q   | conclusion  |
|:--:|:--:|:-:|:----:|:---:|:-----------:|
| ≠0 | >0 |   | <0   | >0  | min local   |
| ≠0 | <0 |   | <0   | <0  | max local   |
| ≠0 | ?  |   | >0   | ≠0? | point selle |
| ≠0 | =0 |   | ?    | =0  | dégénéré    |
| ≠0 | >0 |   | =0   | >0  | min local   |
| ≠0 | <0 |   | =0   | <0  | max local   |

$$
\begin{split}
    &\text{def dune diff total exacte : }\\
    
    &\embrace{
        &\ \oint_{\Gamma^+}d\omega=0\\
        &\ \text{si }d\omega\text{ est une F.d fermée}\\
        &\ \omega=Pdx+Qdx\\
        &\ \Rightarrow \frac{\delta p}{\delta y}=\frac{\delta Q}{\delta x}
    }{|}{.}\n

    &\text{Thm de Green-Riemann}\\

    &\embrace{
        &\iint_D\pembrace{\frac{\delta P}{\delta y}-\frac{\delta Q}{\delta x}}dxdy=\oint_{\delta D^+}Pdx+Qdy
    }{|}{.}\n

    &\text{Thm d'Ostrograsky}\\
    
    &\embrace{
        &\iiint_V div\vec{F}=\oiint\vec{F}\cdot\vec{dS}\\
        &\phantom{\iiint_V}div\vec{F}=\lim_{V_S\rightarrow0}\iint_S\vec{F}ds\n
        &\Rightarrow div\vec{F}= \frac{\delta Fx}{\delta x}+\frac{\delta Fy}{\delta y}+\frac{\delta Fz}{\delta z}
    }{|}{.}
\end{split}
$$

$$
\begin{split}
    &D = \aembrace{(x,y)\in\R^2\ |\ x\ge0,\ y\ge0,\ x^{\frac23}+y^{\frac23}\lt1}\n
    
\end{split}
$$
![img](https://i.imgur.com/GhZB8DH.png)
$$
\begin{split}
    &\embrace{
        &x=rcos^3\theta\\
        &y=rsin^3\theta
    }{\{}{.}\quad\quad f(x,y)=xy\n

    &\embrace{
        &\frac{\delta x}{\delta r}\quad \frac{\delta x}{\delta \theta}\\
        &\frac{\delta y}{\delta r}\quad \frac{\delta y}{\delta \theta}
    }{|}{|}=\embrace{
        &cos^3\theta\quad-3rcos^2\theta sin\theta\\
        &sin^3\theta\quad+3rsin^2\theta cos\theta
    }{|}{|}\n
    &=3rsin^2\theta cos^4\theta+3rcos^2\theta sin^4\theta\n
    
    &=3r\cembrace{cos^4\theta sin^2\theta +sin^4\theta cos^2\theta}\n

    &=3r sin^2\theta cos^2\theta\quad *\underbrace{\pembrace{cos^2\theta+sin^2\theta}}_{=1}\n

    &=\iint r^2cos^3\theta sin^3\theta 3r sin^2\theta cos^2\theta \ dr d\theta\n

    &=\iint r^3 cos^5\theta sin^5\theta \ dr d\theta\n

    &\text{c chiant donc on skip...}\n

    &=\frac1{80}
\end{split}
$$