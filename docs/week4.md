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
\rightarrow r^{2} + Ar &+& B = 0 \text{ characteristic equation}.
\end{eqnarray*}

- we can solve r:
\begin{eqnarray*}
r=\frac{-A\pm \sqrt{A^{2}-4B}}{2}
\end{eqnarray*}

## Case1: two real roots (overdamping)
\begin{eqnarray*}
r_{1} \neq r_{2} \rightarrow y(t)=c_{1}e^{r_{1}t}+c_{2}e^{r_{2}t}
\end{eqnarray*}

- example

\begin{eqnarray*}
y''+4y'+3y=0, y(0)=1, y'(0)=0
\end{eqnarray*}

The characteristic equation is
\begin{eqnarray*}
r^{2}&+&4r+3=0\\\\
&\Longrightarrow& (r+3)(r+1)=0 \rightarrow r=-3, -1\\\\
&\Longrightarrow& y(t)=c_{1}e^{-3t}+c_{2}e^{-t}
\end{eqnarray*}

Use initial conditions
\begin{eqnarray*}
y(0)&=&1=c_{1}+c_{2}, \\\\
y'(0)&=&0=-3c_{1}-c_{2}\\\\
&\Longrightarrow& c_{1}=\frac{-1}{2}, c_{2}=\frac{3}{2}\\\\
&\Longrightarrow& y(t)=\frac{-1}{2}e^{-3t}+\frac{3}{2}e^{-t}
\end{eqnarray*}


- the plot for possible solutions y(t):
```{figure} /_static/figures/overdamp.png
:scale: 50%
:name: overdamp
```

## Case2: two equal roots (critical damping)

## Case 3: complex roots (undamped/underdamped)









