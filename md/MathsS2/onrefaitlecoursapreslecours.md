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

# Suites

# 1. Topologie de $\R$

## Def


- L'application d : 
$$
\R \times \R\rightarrow\R^+ \\ 
(x,y)\rightarrow d(x,y)\\
d(x,y)=\abs{y-x} \text{est la distance canonique de }\R\\
\text{La boule }B(a)=\aembrace{x\in\R\ | \abs{x-a}\lt r} \text{ est l'intervalle}\\
$$
- Voisinage:
$$
\mathcal{V}\text{ est un voisinage de a ssi}\\
\exist \alpha\gt0\quad \embrace{a-\alpha;a+\alpha}{]}{[}\subset \mathcal{V}
$$
* ouvert
$$
    \Omega \text{ est un ouvert dans $\R$ ssi est voisinage de chacun de ses parents.}
$$
* fermé 
$$
\text{F est un fermé dans $\R$ ssi le complémentaire de F est ouvert}\\
\text{(Un point est un fermé, Un ensemble fini de points est un fermé)}
$$

* Ex  
$$
A = \cembrace{0,3}\\
\text{est un voisinage de $\frac12$ car}\\
\embrace{\frac12-\frac14\ ;\ \frac12+\frac14}{]}{[}\subset A
$$
<br/><br/>

$$
\text{Tout  intervalle ouvert I $]a,b[$ est un ouvert}\\
\text{si $x_0$ plus près de a que de b}\\
\embrace{x_0-\frac{\varepsilon}2\ ;\ x_0+\frac{\varepsilon}2}{]}{[}\subset\ ]a,b[\\
\text{mais $[a,b]$ n'est pas ouvert car aucun }\\
\text{intervalle n'est centré en a ou b}
$$

* Compact
    $$
    \text{Un intervalle compact est un intervalle fermé et borné}\\
    \text{$[a,b]$ est un compact, mais pas $[a;+\infty[$ ; $]-\infty;b]$ ; $]-\infty;+\infty[$}
    $$


* Adhésion
$$
A\subset\R\quad a\in\R\\
\text{$a$ est adhérent à $A$ ssi tout voisinage de $a$}\\
\text{a un point commun avec $A$}\\
\text{l'ensemble des points adhérents de $A$ est noté $\overline{A}$}\\
A\subset\overline{A}\n

\text{si $A\subset B\subset\overline{A}$}\\
\text{On dit que $B$ est dense dans $A$}\n

\text{$\mathbb{Q}$ est dense dans $\R$}\\
\text{$\overline{A}$ est le plus petit fermé contenant $A$}\n

\text{Tout point de $A$ est adhérent à $A$ mais il peut exister des points}\\
\text{$a \notin A$ qui soient adhérents à $A$}
A = \aembrace{1,\frac12,\frac13,\dots}
$$

* Points particuliers
$$
\text{Pour tout point adhérent $x$ à un intervalle $A$ de $\R$ il y a 2 possibilités}
$$
1.
$$
\text{Dans tout voisinage de $x$ il y a une infinité de points de $A$}\\
\text{$x$ est un point d'accumulation}
$$
2.
$$
\text{Dans un voisinage de $x$ il n'y a aucun point de $A$ autre que $x$}\\
\text{$x$ est un point isolé}
$$

* Majorants/Minorants
$$
A\subset\R\\
\text{$M$ est un majorant de A}\\
\text{ssi } \forall a\in A\quad a\le M\\
\text{$m$ est un minorant de A}\\
\text{ssi } \forall a\in A\quad a\ge m\n

\text{$b_s=$borne supérieure}\equiv\text{le plus petit des majorants}\\
\text{$b_i=$borne inférieure}\equiv\text{le plus grand des minorants}\\
\Rightarrow\quad \embrace{&b_s=\sup A\\&b_i=\inf A}{|}{.}
$$

# 2. Suites de nombres réels

## Def
* Suite
    
    Une suite de nombre réels est une application de $\N$ dans $\R$
    $$
    \left.\begin{split}
    (u_n)_{n\in\N}\quad\embrace{
        &\N\rightarrow\R\\ 
        &n\rightarrow u_n=f(n)}{.}{.}\n
    \end{split}\right.
    $$
    $(u_n)$ : la suite
    
    $u_n$ : le terme général

* Convergence de Suite $(u_n)$
    
    limite L d'une suite convergente
    $\forall\varepsilon\gt0,\exist\ \eta_0\in\N$
    $\left\{\forall n\gt n_0\Rightarrow\ |u_n-L|\lt\varepsilon\right\}$
    $$
    u_n =\frac1n+\frac{(-1)^n}{2^n}\n
    \embrace{
        &n=1\quad1+\frac{-1}2=\frac12=0,5\\
        &n=2\quad\frac12+\frac14=\frac34=0,75\\
        &n=3\quad\frac13-\frac1{2^3}=\frac13-\frac18=\frac5{24}
    }{|}{.}
    $$
    * Théorème
        
        - Toute suite de nombres réels croissante et majorée possède une limite (converge)

        - Toute suite de nombres réels décroissante et minorée converge
* Théorème de Bolzano-Weierstrass
    
    Toute infinité de points coincés entre a et b s'accumule pour tout point

    Toute partie bornée $P$ de $\R$ comportant une infinité de points possède au moins un point d'accumulation

* Suite extraite
    
    $(u_n)$ : suite

    $(V_n) = (u_{\alpha(n)})$ : suite extraite de $(u_n)$

    Toute suite extraite d'une suite convergente converge vers la même limite L

* Intervalles emboités

    $I_n=[a_n,b_n]$ Suite décroissante d'intervalles

    $|b_n-a_n|\ \rightarrow0$ pour $n\rightarrow0$

    Ces intervalles ont en commun le seul point limite L

* Suite adjacente
    $(u_n),(v_n)$ sont adjacentes ssi
    $$
        \embrace{
        \ &\forall n\in\N\quad v_n\ge u_n\n
        &(u_n)\text{ est croissante}\\
        &(v_n)\text{ est décroissante}\n
        &\lim_{n\rightarrow\infty}\abs{v_n-u_n}=0}{|}{.}
    $$