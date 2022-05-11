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

Thm de Green-Riemann
$$
\begin{split}
    &\int_{\delta D}Pdx+Qdy=\iint_D\pembrace{\frac{\delta Q}{\delta x}-\frac{\delta P}{\delta y}}dxdy\n
    &\text{on veut:}\\
    &\embrace{
        &\frac{\delta Q}{\delta x}-\frac{\delta P}{\delta y}\n
        &\text{On pose:}\n
        &P(x,y)=\frac{-y}{\phantom{-}2}\quad\frac{\delta P}{\delta y} = \frac{-1}{2}\n
        &Q(x,y)=\phantom{-}\frac{x}{2}\quad\frac{\delta Q}{\delta x}=\frac{1}{2}

    }{|}{.}
\end{split}
$$

$$
\begin{split}
    &\text{Aide de D = }\iint_D dxdy = \int_{\delta D^+}=\frac{-y}{2}dx+\frac{x}{2}dy\n

    &\boxed{
        \iint_D dxdy=\frac12\int_{\delta D^+}xdy-ydx\n
    }\n

\end{split}
$$

Ex5 b) : Calculer l'aide de D

$$
\begin{split}
    &\text{<schéma cornet>}\n
    &\text{Aide(D)}=\frac12\int_{\theta_1}^{\theta_2}f^2(\theta)d\theta\n
    &\Gamma_1^+
    \ \ \embrace{
        &x=rcos\theta_1\\ 
        &y=rsin\theta_1\\ 
        &r\in\cembrace{0,f(\theta_1)}
    }{\{}{.}\quad
    \Gamma_2^+
    \ \ \embrace{
        &x=f(\theta)cos\theta\\ 
        &y=f(\theta)sin\theta\\ 
        &r\in\cembrace{\theta_1,\theta_2}
    }{\{}{.}\quad
    \Gamma_3^+
    \ \ \embrace{
        &x=rcos\theta_2\\ 
        &y=rsin\theta_2\\ 
        &r\in\cembrace{f(\theta_2),0}
    }{\{}{.}\n
    
    &\iint_D dxdy = \int_{\Gamma_1^+}+\int_{\Gamma_2^+}+\int_{\Gamma_3^+} = I_1+I_2+I_3\n

    &I_1=I_3=0\n

    &I_2=\frac12 \int_{\theta_1}^{\theta_2}f(\theta)cos\theta\cembrace{f'(\theta)sin\theta+f(\theta)cos\theta}d\theta\\
    &\quad\quad-f(\theta)sin\theta\cembrace{f'(\theta)cos\theta+f(\theta)(-sin\theta)}d\theta\n

    &=\frac12\int_{\theta_1}^{\theta_2}f^2(\theta)(cos^2\theta+sin^2\theta)d\theta\n

    &\text{Aide(D)}=\frac12\int_{\theta_1}^{\theta_2}f^2(\theta)d\theta
\end{split}
$$


# Ex6

$$
\begin{split}
    &\omega=\underbrace{2\pembrace{x+y^2}}_{P(x,y)}dx+\underbrace{\pembrace{4xy+3y^2}}_{Q(x,y)}dy\n

    &\embrace{&\frac{\delta P}{\delta y}=4y\\&\frac{\delta Q}{\delta x}=4y}{\{}{.}\quad\Rightarrow\text{la forme différentielle est fermée}\n

    &\text{<schema triangle>}\n

    &\int_{\gamma^+}=\int_{AB}\omega+\int_{BC}\omega+\int_{CA}\omega\n

    &AB:\\
    &\embrace{
        &\embrace{&x\in\cembrace{0,1}\\&y=0}{\{}{.}\quad \embrace{&x=t\\&y=0}{\{}{.}\quad \embrace{&dx=dt\\&dy=0}{\{}{.}\n

        &\int_0^12tdt= 2\cembrace{\frac{t^2}{2}}_{0}^{1}=2*\frac12=1
    }{|}{.}\n
    &BC:\\
    
    &\embrace{
        &\embrace{&x=1-t\\&y=t}{\{}{.}\quad \embrace{&dx=-dt\\&dy=dt}{\{}{.}\\

        &t\in\cembrace{0,1}\n
        
        &\int_0^12\pembrace{(1-t)+t^2}(-dt)+(4(1-t)t+3t^2)dt\\

        &\int_0^1(-2(1-t+t^2)+4t-4T^2+3t^2)dt\\

        &\int_0^1(-2+2t-2t^2+4t-t^2)dt\\

        &\int_0^1-3t^2+6t-2=-3[\frac{t^3}{3}]_0^1+6[\frac{t^2}{2}]_0^1-2[t]_0^1\\
        
        &\quad\quad=-1+6/2-2=0
    }{|}{.}\n

    &CA:\\
    &\embrace{
        &\embrace{&y=t\\&x=0}{\{}{.}\quad\embrace{dy=dt\\ \ }{\{}{.}\\
        &\ t\in\cembrace{0,1}
    }{|}{.}\n

    &I=\int_0^1 3t^2dt\\
    &\phantom{I} = 3\cembrace{\frac{t^3}{3}}_0^1=0-(1)^3=-1
\end{split}
$$

# Ex7 a)

$$
\begin{split}
    &I=\iint_D xydxdy\\
    &D=\aembrace{(x,y)\in\R^2\ |\ x\ge0,\ y\ge0,\ x+y\le1}\n

    &I=\int_0^1\int_0^1xydydx\n
    &I=\int_0^1x\int_0^{1-x}ydydx\n
    &I=\int_0^1x\cembrace{\frac{y^2}2}_0^{1-x}dx\n
    &I=\int_0^1x\pembrace{\frac{(1-x)^2}{2}}dx=\frac12\int_0^1x(1+x^2-2x)dx\n
    &I=\frac12\int_0^1(x+x^3-2x^2)dx\n
    &I=\frac12 \cembrace{\frac{x^2}{2}+\frac{x^4}{4}-2\frac{x^2}{3}}_{0}^{1}\n
    &I=\frac12\cembrace{\frac12+\frac14-\frac23}\n
    &I=\frac12\cembrace{\frac{9-8}{12}}=\frac{1}{24}\n
\end{split}
$$

# Ex8 b)

$$
\begin{split}
    &J = \int_{\Gamma^+}\frac{y^3}{P(x,y)}dx+\frac{x^3}{Q(x,y)}dy\n
    
    &\embrace{&\frac{\delta}{\delta y}P(x,y)=3y^2\\&\frac{\delta}{\delta x}Q(x,y)=3x^2}{\{}{.}\quad\text{la forme différentielle n'est ¯\\ \_(ツ)\_/¯}\n

    &\embrace{&x=acos\theta\\&y=bsin\theta}{\{}{.}\quad\quad \embrace{&dx=-asin\theta d\theta\\&dy=bcos\theta d\theta}{\{}{.}\n

    &J=\int_0^{2\pi}(-b^3sin^3\theta asin\theta+a^3cos^3\theta bcos\theta)d\theta\n

    &J=\int_0^{2\pi}\pembrace{a^3bcos^4\theta-ab^3sin^4\theta}d\theta\n

    &\text{abandon du prof}
\end{split}
$$


# de retour sur l'elipse

$$
\begin{split}
    &\iint_D(2x^3-y)dxdy\\
    
    &D=\aembrace{(x,y)\in\R^2\ |\ x\ge0,\ y\ge0,\ \frac{x^2}{a^2}+\frac{y^2}{b^2}\le1}\n

    &\text{changement de var}\\
    
    &\quad \embrace{&x=arcos\theta\\&y=brsin\theta}{\{}{.}\n
    
    &J_{\phi}=
        \embrace{
            &\frac{\delta x}{\delta r}\frac{\delta x}{\delta\theta}\\
            &\frac{\delta y}{\delta r}\frac{\delta y}{\delta\theta}
        }{|}{|}=
        \embrace{
            &acos\theta\quad-arsin\theta\\
            &bsin\theta\quad \phantom{-}brcos\theta
        }{|}{|}\n
    &|Det J_{phi}| = |abr*(cos^2\theta+sin^2\theta)|=|abr|\n

    &J=\int_0^1\int_0^{\frac{\pi}2}(2(arcos\theta)^3-brsin\theta)*|det J_{\phi}|d\theta dr\n

    &\phantom{J}=\int_0^1\int_0^{\frac{\pi}2}(2a^3r^3cos¨3\theta-brsin\theta)abrd\theta dr\n

    &\phantom{J}=\int_0^1\int_0^{\frac{\pi}2}2a^4br^4cos^3\theta d\theta dr\n
    &\phantom{J}-\int_0^1\int_0^{\frac{\pi}2}ab^2r^2sin\theta d\theta dr = I_1-I_2\n

    &I_2=ab^2\int_0^1r^2dr\int_0^{\frac{\pi}2}sin\theta d\theta\n

    &I_2=ab^2 \cembrace{\frac{r^3}3}_{0}^{1} \cembrace{-cos \theta}_{0}^{\frac{\pi}2}\n

    &I_2=ab^2\frac13*\underbrace{\cembrace{-cos\frac{\pi}2-(-cos\theta)}}_{0-(-1)=1}\n

    &I_2=\frac{ab^2}{3}\n

    &I_1=2a^4b\int_0^1r^4dr\int_0^{\frac{\pi}2} cos^3\theta d\theta\n

    &I_1=2a^4b \cembrace{\frac{r^5}5}_{0}^{1}\int_0^{\frac{\pi}2}cos^3\theta d\theta\n

    &I_1=\frac{2a^4b}{5}\int_0^{\frac{\pi}2}cos^3\theta d\theta\n

    &\quad\embrace{\int_0^{\frac{\pi}2}cos^3\theta d\theta = \cembrace{\frac13sin3\theta}_{0}^{\frac{\pi}2}+ \cembrace{sin^3\theta}_{0}^{\frac{\pi}2}=\frac23}{|}{.}\n

    &I_1= \frac{4a^4b}{15}\n

    &I = I_1-I_2=\boxed{\frac{4a^4b}{15}-\frac{ab^2}{3}}
\end{split}
$$

# Volume de l'ellipsoide

$$
\begin{split}
    \frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}\le1\n

    &\embrace{
        &V_{sphere}=\frac43\pi\ r^3\\
        &V_{ellipsoide}=\frac43\pi\ abc
    }{|}{.}\n

    &\embrace{
        &x=arsin\theta\ cos\phi\\
        &y=brsin\theta\ sin\phi\\
        &z=crcos\theta
    }{\{}{.}\quad\quad \embrace{
        &r\in [0,1]\\
        &\theta\in[0,\pi]\\
        &\phi\in[0,2\pi]
    }{.}{.}\n

    &det J_{\phi}=abc\ r^2sin\theta\n
    &V=\iiint_Vdxdydz\n
    &V=abc \underbrace{\int_0^1\int_0^\pi\int_0^{2\pi}r^2sin\theta\ d\theta_ d\phi\ dr}_{\frac43\pi}\n
    &V= \frac43\pi\ abc
\end{split}
$$
