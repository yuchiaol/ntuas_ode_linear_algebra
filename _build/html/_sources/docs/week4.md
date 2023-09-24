---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

(week4)=

# Week4 -  fundamental equation of mechanics

\begin{eqnarray*}
&mx''& = &-kx& - &cx'&\\
&\uparrow& &\uparrow& &\uparrow&\\
&\text{Force (Newton)}& &\text{spring (Hooke)}& &\text{dash pot/damping}&
\end{eqnarray*}

\begin{eqnarray*}
\Longrightarrow mx''+cx'+kx=0\\\\
\Longrightarrow x''+ \frac{c}{m}x'+ \frac{k}{m}x=0
\end{eqnarray*}

## Second order linear (homogeneous) ODEs
- to find two independent solutions (homogeneous solutions)
- general form: 
\begin{eqnarray*}
\frac{d^{2}y}{dt^{2}}+a\frac{dy}{dt}+By=0, \text{ given } y(0)=1, y'(0)=0.
\end{eqnarray*}
- basic method guess and plug in the exponential solution:
\begin{eqnarray*}
\text{try } y(t)&=&e^{rt}\\\\ 
\rightarrow r^{2}e^{rt} + Are^{rt} &+& Be^{rt} = 0\\\\
\rightarrow r^{2} + Ar &+& B = 0 \text{characteristic equation}.
\end{eqnarray*}

- we can solve r:
\begin{eqnarray*}
r=\frac{-A\pm \sqrt{A^{2}-4B}}{2}
\end{eqnarray*}

- the plot for possible solutions y(t):
```{figure} /_static/figures/overdamp.png
:scale: 50%
:name: overdamp
```

## Case1: two real roots (overdamping)

## Case2: two equal roots (critical damping)

## Case 3: complex roots (undamped/underdamped)









