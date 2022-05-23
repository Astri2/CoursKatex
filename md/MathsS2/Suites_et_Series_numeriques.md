# Suites Séries numériques


Soit $(U_n)\quad n\in\N$

Et $S_p=\sum^Pu_n$

<br/>

Propriété :

Si $\sum u_n$ converge, alors $\lim_{n\rightarrow\infty}u_n=0$
On pose $S=\lim_{p\rightarrow\infty}S_p=\sum_{n=1}^\infty$ 

<br/>
Rappel:

$\sum_{n=0}^Pa^n = \frac{1-a^{P+1}}{1-a}$

<br/>
Série géométrique:

$\sum a^n\rightarrow\frac1{1-a}\quad|a|\lt1$

<br/>
Application:

* $u_n=(\frac13)^n$

    $S=\frac1{1-\frac13}=\frac32$

* $u_n=\frac{2^{2n}}{5^n}=(\frac45)^n$

  $S\rightarrow\frac1{1-\frac45}=5$

* $u_n = \frac1{n!}$
  
  $S = 1 + \frac1{1!}+\frac1{2!}+\frac1{3!}+\dots+$

  Pour $n\ge 1$, $\frac1{n!}\le\frac2{n^2}$

  $(u_n) = \frac2{n^2} \equiv \int_1^\infty f(x)dx$ CVG avec $f(x)=\frac2{x^2}$

  $\Rightarrow \sum\frac1{n!}$ CVG

* $u_n=\frac{n^2+1}{n!}$, sachant que $\sum^\infty\frac1{n!}=e$
  
  $S_p = \sum^Pu_n$

  $S_p=\sum^P\frac{n^2+1}{n!}=\sum^P\frac{n^2}{n!}+\sum^P\frac1{n!}$

  $S_p=\sum^P\frac{n}{(n-1)!}+\sum^P\frac1{n!}$

  $S_p=\sum^P\frac{n-1+1}{(n-1)!}+\sum^P\frac1{n!}$

  $S_p=\sum^P\frac1{(n-2)!}+\frac1{(n-1)!}+\sum^P\frac1{n!}$

  $S_p=\sum_{n=0}^P\frac{1}{n!}+\sum_{n=1}^P\frac1{(n-1)!}+\sum_{n=2}^P\frac1{(n-2)!}$

  Soit $(n-1) = m$ et $(n-2) =l$

  $S_p=\sum_{n=0}^P\frac1{n!}+\sum_{m=0}^P\frac1{m!}+\sum_{l=0}^P\frac1{l!}$

  on sait que $\sum^\infty\frac1{n!}=e$ donc $\boxed{\lim_{P\rightarrow\infty}S_n=3e}$

<br/>

En mettant $u_n$ sous forme $u_n=f(n+1)-f(n)$

calculer $S=\lim_{P\rightarrow\infty}\sum^Pu_n$

* $u_n=\frac1{n(n+1)}$

  $u_n=\frac{(n+1)-n}{n(n+1)}=\frac1n-\frac1{n+1}$

  $u_n = f(n+1)-f(n) = -\frac1{n+1}+\frac1n$

  par identification, $f(n) = \frac1n$

  $S_p=\sum_{n=1}^P\frac1{n(n+1)}=\sum_{n=1}^P\frac1n-\sum_{n=1}^P\frac1{n+1}$

  Soit $m=n+1$

  $S_p=\sum_{n=1}^P\frac1n-\sum_{m=2}^{P+1}\frac1m$

  $S_p =  1 + \frac12 +\dots+\frac1P\quad-\quad\frac12+\dots+\frac1P+\frac1{p+1}$

  $\boxed{S_p=1-\frac1{P+1}}\quad$Converge

* $u_n = \frac1{n(n+1)(n+2)}$

  $u_n=\frac{(n+2)-(n+1)}{n(n+1)(n+2)}$

  $u_n=\frac1{n(n+1)}-\frac1{n(n+2)}$

  $u_n=\frac1n-\frac1{n+1}-\frac{(n+2-n)}{2n(n+2)}$

  $u_n=\frac1n-\frac1{2n}+\frac1{2(n+2)}$

  $u_n=\frac1{2n}-\frac1{n+1}-\frac1{n(n+2)}$

  $S_p=\frac12\sum_{n=1}^P\frac1n-\sum_{n=1}^P\frac1{n+1}-\frac12\sum_{n=1}^P\frac1{n+2}$

  $S_p=\frac12\sum_1^P\frac1N-\frac12\sum_{q=3}^{p+2}\frac1q-\sum_{m=2}^{P+1}\frac1m$

  $S_p=\frac12(1+\frac12+...+\frac1P)\ -\ \frac12(\frac13+...+\frac1P+\frac1{P+1}+\frac1{P+2})$ 
  
    $\quad\quad\quad-\ (\frac12+\frac13+...+\frac1{P+1})$

  $S_p=\frac12+\frac14-\frac1{2(P+1)}-\frac1{2(P+2)}-\sum_{n=1}^P\frac1{n+1}$