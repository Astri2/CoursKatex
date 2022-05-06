# Théorème de Flux-Divergence Ostrogradsky
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

$$
\oiint \vec{F}.\vec{ds} = \iiint_Vdiv\vec{F}\ dV\n\n
<schema 1>\n\n

\embrace{
    &\text{Définition de la divergence d'un vecteur } \vec{F}\n
    
    &div\vec{F}= \lim_{V_S\rightarrow\ 0}\oiint_S\vec{F}.\vec{ds}\\
    &\hspace{2cm}\frac{S\quad }{\quad V_S}\\
    
    &\hspace{2cm}V_S=\delta^3\n

    &<schema 2>\n
    
    &F_y(y+\frac{\delta}2)\delta^2-F_y(y-\frac{\delta}2)\delta^2\\
    
    &\ = \frac{F_y(y+\frac{\delta}2)-F_y(y-\frac{\delta}2)}{\delta}\delta^3\xrightarrow[\delta\rightarrow0]{}\frac{\delta F_y}{\delta y}\\
    
    &\text{on repète ça sur les trois axes:}\\
    
    &\ \Rightarrow 
    \boxed{div\vec{F} =\frac{\delta F_x}{\delta x}+\frac{\delta F_y}{\delta y}+\frac{\delta F_z}{\delta z}}
}{|}{.}
$$

## <u>Ex:</u> Vérifier le théorème d'ostrogradsky
$$
\vec{F}(x,y,z)=\pembrace{x\\y\\z}\hspace{1cm} \embrace{&\text{Sur un volume cubique}\\&\text{centré sur O de côté 2R}}{.}{.}\n

\begin{split}
    &\vec{\nabla}.\vec{F} = \frac{\delta x}{\delta x} + \frac{\delta y}{\delta y} + \frac{\delta y}{\delta y} = 1+1+1=3\n
    
    &V=8R^3\hspace{1cm}\iiint div\vec{F}=3*8R^3\n
    
    &\oiint \vec{F}.\vec{ds}= \int_{-R}^R\int_{-R}^R y\ dzdx=y\ 4R^2
\end{split}
$$