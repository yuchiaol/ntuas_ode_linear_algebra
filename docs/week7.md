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

(week7)=

# Week7 - variation of parameters

## The fundamental set of solutions amd Wronskian
Consider linear ODE:
\begin{eqnarray*}
&\text{   }& y''+p(t)y'+q(t)y=0 \\\\
y_{1}(t) \text{ and } &y_{2}(t)& \text{ form a fudamental set of solutions (fss) if:} \\\\
&1.& y_{1}, y_{2} \text{ are solutions of the ODE.} \\\\
&2.& \text{every solution } y(t) \text{ of the ODE can be written as:}\\\\
&\text{    }& y(t) = c_{1}y_{1}(t) + c_{2}y_{2}(t)
\end{eqnarray*}

````{prf:theorem}
:label: my-theorem_vp1
Two solutions form a fss if the determinat

\begin{eqnarray*}
W(t) = 
\begin{vmatrix}
     y_{1}(t) & y_{2}(t) \\
     y_{1}'(t) & y_{2}'(t) 
\end{vmatrix}
\neq 0
\end{eqnarray*}
W(t) is called Wronskian.

````

````{prf:example}
:label: my-example_vp1
Consider the ODE:
\begin{eqnarray*}
y''+y=0
\end{eqnarray*}
Show that
\begin{eqnarray*}
y_{1}(t)=\sin{}(t), y_{2}(t)=\cos{}(t)
\end{eqnarray*}
form a fss of this ODE.
1. they are solutions to the ODE.
2. 
\begin{eqnarray*}
W(t) =
\begin{vmatrix}
     \sin{}(t) & \cos{}(t) \\
     \cos{}(t) & -\sin{}(t)
\end{vmatrix}
= -\sin{}^{2}(t) - \cos{}^{2}(t) = -1
\neq 0
\end{eqnarray*}

````

## Variation of parameters
Consider the ODE:
\begin{eqnarray*}
1y''+B(t)y'+C(t)y=f(t).
\end{eqnarray*}

Suppose we have two homogeneous solutions:
\begin{eqnarray*}
y_{1}(t), y_{2}(t)
\end{eqnarray*}

The idea is to construct the particular solution as the form of
\begin{eqnarray*}
y_{p}(t)=c_{1}(t)y_{1}(t) + c_{2}(t)y_{2}(t), \\\\
c_{1}(t), c_{2}(t) \text{ are called the varying parameters.}
\end{eqnarray*}

if
\begin{eqnarray*}
c_{1}'(t)y_{1}(t) &+& c_{2}'(t)y_{2}(t) = 0 \\\\
c_{1}'(t)y_{1}'(t) &+& c_{2}'(t)y_{2}'(t) = f(t) \\\\
\Longrightarrow 
W(t) &=&
\begin{vmatrix}
     y_{1}(t) & y_{2}(t) \\
     y_{1}'(t) & y_{2}'(t)
\end{vmatrix}
\neq 0 \\\\
&\Longrightarrow& y_{1}(t), y_{2}(t) \text{ form a fss}
\end{eqnarray*}

then
\begin{eqnarray*}
y_{p}(t) &=& y_{1}\int{\frac{W_{1}}{W}dt} +  y_{2}\int{\frac{W_{2}}{W}dt} \\\\
W_{1} &=& 
\begin{vmatrix}
     0 & y_{2}(t) \\
     f(t) & y_{2}'(t)
\end{vmatrix} \\\\
W_{2} &=&
\begin{vmatrix}
     y_{1}(t) & 0 \\
     y_{1}'(t) & f(t)
\end{vmatrix} \\\\
\end{eqnarray*}

So the particular solution is:
\begin{eqnarray*}
y_{p}(t) = y_{1}(t)\int{\frac{-y_{2}(t)f(t)}{W}dt} +  y_{2}(t)\int{\frac{y_{1}(t)f(t)}{W}dt}
\end{eqnarray*}





