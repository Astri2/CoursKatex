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
%     \left(#1\right)
% }
% \global\newcommand{\cembrace}[1]{
%     \embrace{#1}{[}{]}
% }
% \global\newcommand{\bembrace}[1]{
%     \embrace{#1}{|}{|}
% }
% \global\newcommand{\vec}[1]{\overrightarrow{#1}}
% \global\newcommand{\abss}[1]{
%     \cembrace{#1}
% }
$$

# Exercices sur les intégrales impropres

Calculer, si possible:

* $I=\int_1^\infty\frac{a^x}{1+a^{2x}}dx$ avec $a\gt0$

    $$
    I=\int_1^\infty\frac{a^x}{1+a^{2x}}dx \quad a\gt0\n
    t=a^x\n
    \ln t=x\ln a\n
    x=\frac{\ln t}{\ln a}\quad\Rightarrow\quad dx=\frac1{\ln a}\frac{dt}{t}
    $$
    Disjonction de cas :
    * si $a\gt1$
        $$
        I = \int_a^0\frac{t}{1+t^2}\frac1{\ln a}\frac{dt}{t}\n
        I=\frac1{\ln a}\int_a^0\frac1{1+t^2}dt\n
        I = \frac1{\ln a} \cembrace{\arctg t}_{a}^{0}
        I = \frac1{\ln a}\pembrace{\frac\pi2-\arctg a}
        $$
    * si $a=1$
        $$
        I = \int_1^\infty\frac{1^x}{1+1^{2x}}\n
        I = \int_1^\infty\frac12dx
        $$

    * si $a\lt1$
        $$
        I=-\int_0^a\frac1{1+t^2}\frac{dt}{\ln a}\n
        I=\frac{-1}{\ln a}\cembrace{\arctg t}_0^a\n
        I=\frac{-1}{\ln a}\cembrace{\arctg a-\arctg 0}\n
        I = -\frac{\arctg a}{\ln a}
        $$

* $I_n=\int_0^\infty t^ne^{-t^2}$
    $$
    f(t)=t^ne^{-t^2}\text{ est continue sur }\R\n
    \embrace{
        &\lim_{t\rightarrow\infty}t^ne^{-t^2}=0\\
        &\lim_{t\rightarrow\infty}t^ne^{-t}=0
    }{|}{.}\n
    $$

    1)
        $$
        \lim_{n\rightarrow\infty}t^{n+2}t^{-2}=0\n
        \exist A\gt0\n
        t^{n+2}t^{-2} \lt 1
        \Leftrightarrow t^nt^{-2}\lt\frac1{t^2}\n
        \Rightarrow I_n \le \underbrace{\int_0^{\infty}\frac1{t^2}dt}_{CVG}\quad\boxed{CVG}\n\n
        I_0=\int_0^\infty e^{-t^2}dt=\frac{\sqrt{\pi}}2\n
        I_1=\int_0^\infty te^{-t^2}dt=\cembrace{-\frac12e^{-t^2}}_{0}^{\infty}=\frac12\n\n
        I_n=\int_°^\infty t^ne^{-t^2}dt\n
        I_n=\int_°^\infty t^{n-1}*te^{-t^2}dt\n
        \embrace{\ &u=t^{n-1}\quad u'=(n-1)t^{n-2}\\
        &v'=te^{-t^2}\quad v=-\frac12e^{-t^2}}{|}{.}\n
        I_n=\underbrace{\cembrace{t^{n-1}*(-\frac12e^{-t^2})}_{0}^{\infty}}_{=0}+\int_0^\infty\frac12e^{-t^2}(n-1)t^{n-2}dt\n
        I_n=\frac12(n-1)\int_0^\infty t^{n-2}e^{-t^2}dt\n
        I_n=\frac{n-1}2I_{n-2}\n\n
        \begin{split}
        &I_2=\frac12*I_0=\frac{\sqrt{\pi}}4\n
        &I_3=1*I_1=\frac12\n
        &I_4=\frac32*I_2=\frac{3\sqrt{\pi}}8\n
        &I_5=2*I_3=1\n
        &I_6=\frac52*\frac{3\sqrt{\pi}}8\n
        &I_7=3*I_5=3\n
        &I_9=4*I_7=12\n
        \text{donc : }\\
        &I_{2p+1} = f_1(p)*I_1\n
        &I_{2p}=f_2(p)*I_0
        \end{split}
        $$
* $I=\int_0^\infty x\cos^4x_ dx$
    $$
    I=\int_0^\infty x\cos^4x\ dx\n
    I\le \int_0^\infty \bembrace{x\cos^4x}dx\le\underbrace{\int_0^\infty x\ dx}_{DVG}\n
    I=\int_0^\infty\frac{\cos^4x}{x^2}dx\n
    I\le\int_0^\infty\bembrace{\frac{\cos^4x}{x^2}}dx\le\underbrace{\int_0^\infty\frac1{x^2}dx}_{CVG}\quad\boxed{CVG}

    $$

* $I=\int_0^\infty \frac{x^n}{1+x^2}dx$
    $$
    I=\int_0^\infty \frac{x^n}{1+x^2}dx\n
    \embrace{
        &u=x^2\quad\quad\rightarrow u'=nx^{n-1}\\
        &v'=\frac1{1+x^2}\rightarrow v=\arctg x
    }{|}{.}\n
    I_n=\underbrace{\cembrace{x^n\arctg x}_{0}^{\infty}}_\infty\n
    I_n\quad n\le2\quad \boxed{DVG}\n\n
    I_0=\int_0^\infty \frac1{1+x^2}dx\n
    I_0=\cembrace{\arctg x}_{0}^{\infty}\n
    I_0=\frac\pi2\n\n

    I_1:\quad \frac{x}{1+x^2}\xrightarrow[x\rightarrow\infty]{}\frac1x\quad\Rightarrow\boxed{DVG}
    $$
