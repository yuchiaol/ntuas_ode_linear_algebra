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

(week6)=

# Week6 - exponential response formula (ERF)
This method gives us guide to find the nonhomogeneous (particular) solutions for exponential-type forcing or source term.
Consider the second order ODE:
\begin{eqnarray*}
A''+by'+cy &=& e^{\alpha x}, \alpha \in \mathbb{C} \\\\
&=& e^{(a+i\omega)x}\\\\
\Longrightarrow (D^{2}+AD+B)y &=& P(D)y = e^{\alpha x}
\end{eqnarray*}

The exponential input can be in the form of
\begin{eqnarray*}
e^{ax}, \sin{}(\omega x), \cos{}(\omega x), e^{ax}\sin{}(\omega x), e^{ax}\cos{}(\omega x)
\end{eqnarray*}


````{prf:example}
:label: my-example_erf1
\begin{eqnarray*}
P(D)e^{\alpha x} = P(\alpha)e^{\alpha x}
\end{eqnarray*}
````

````{prf:theorem}
:label: my-theorem_erf1
Exponential-input theorem

\begin{eqnarray*}
y_{p} = \frac{e^{\alpha x}}{p(\alpha)} \text{ solves } P(D)y=e^{\alpha x}
\end{eqnarray*}
````

````{prf:proof}
if 
\begin{eqnarray*}
P(D)y_{p} = e^{\alpha x},
\end{eqnarray*}
then
\begin{eqnarray*}
P(D)\frac{e^{\alpha x}}{p(\alpha)} = \frac{1}{p(\alpha)}P(D)e^{\alpha x} = \frac{1}{p(\alpha)}P(\alpha)e^{\alpha x} = e^{\alpha x}
\end{eqnarray*}

````





