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

Below exponential inputs can are all special cases
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
P(D)\frac{e^{\alpha x}}{P(\alpha)} = \frac{1}{P(\alpha)}P(D)e^{\alpha x} = \frac{1}{P(\alpha)}P(\alpha)e^{\alpha x} = e^{\alpha x}
\end{eqnarray*}

````

````{prf:example}
:label: my-example_erf2
\begin{eqnarray*}
y''-y'+2y=10e^{-x}\sin{}(x)
\end{eqnarray*}

We first complixy the ODE, solve the particular solution, and find its imaginary part:
\begin{eqnarray*}
\tilde{y_{p}}'' - \tilde{y_{p}}' + 2\tilde{y_{p}} &=& 10e^{(-1+i)x} \\\\
P(D) = (D^{2} - D + 2) &\rightarrow& P(\alpha) = \alpha^{2}-\alpha+2
\end{eqnarray*}

\begin{eqnarray*}
(D^{2} - D + 2)\tilde{y_{p}} &=& 10e^{(-1+i)x} \\\\
\Longrightarrow \tilde{y_{p}} = \frac{10e^{(-1+i)x}}{(-1+i)^{2}-(-1+i)+2} &=& \frac{10e^{(-1+i)x}}{3-3i} = \frac{5}{3}(1+i)e^{(-1+i)x}.
\end{eqnarray*}

So the particular solution is:
\begin{eqnarray*}
y_{p} = \mathfrak{Im}(\tilde{y_{p}}) = \frac{5}{3}e^{-x}(\sin{}(x)+\cos{}(x)) = \frac{5}{3}e^{-x}\sqrt{2}(\cos{}(x-\frac{\pi}{4}))
\end{eqnarray*}

````

````{prf:theorem}
:label: my-theorem_erf2
Exponential-shift theorem

\begin{eqnarray*}
P(D)e^{ax}u(x) = e^{ax}P(D+a)u(x)
\end{eqnarray*}
````

````{prf:proof}
Consider
\begin{eqnarray*}
P(D)e^{ax}u(x) &=& (D^{2}+AD+B)e^{ax}u(x) \\\\
&=& D^{2}(e^{ax}u)+AD(e^{ax}u)+B(e^{ax}u) \\\\
&=& D(D(e^{ax}u))+AD(e^{ax}u)+B(e^{ax}u) \\\\
&=& D(ae^{ax}u+e^{ax}Du) + A(ae^{ax}u+e^{ax}Du) + B(e^{ax}u) \\\\
&=& e^{ax}(a^{2}u+aDu+aDu+D^{2}u+aAu+ADu+Bu) \\\\
&=& e^{ax}(D^{2}u+2aDu+a^{2}u+A(Du+au)+Bu) \\\\
&=& e^{ax}((D+a)^{2}u+A(D+a)u+Bu) \\\\
&=& e^{ax}P(D+a)u(x)
\end{eqnarray*}

````












