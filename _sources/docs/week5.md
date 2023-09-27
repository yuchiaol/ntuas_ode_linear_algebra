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

(week5)=

# Week5 - method of undetermined coefficients
This method gives us guide to find the nonhomogeneous (particular) solutions.
Consider the general form of second order ODE:
\begin{eqnarray*}
A''+by'+cy = q(t)
\end{eqnarray*}
We guess the form of nonhomogeneous (particular) solutions based on the form of q(t):
\begin{eqnarray*}
q(t) &\rightarrow& y_{p}(t)\\\\
t, 1 &\rightarrow& a+bt\\\\
e^{st} &\rightarrow& Ye^{st} \text{(if resonance: } Yt^{n}e^{st})\\\\
te^{st} &\rightarrow& (a+bt)e^{st}\\\\
\sin{}(\omega t), \cos{}(\omega t) &\rightarrow& M\cos{}(\omega t) + N\sin{}(\omega t)\\\\
t\cos{}(\omega t) &\rightarrow& (a+bt)\cos{}(\omega t) + (c+dt)\sin{}(\omega t)\\\\
e^{i\omega t}, e^{-i\omega t} &\rightarrow& Ye^{-i\omega t}
\end{eqnarray*}


````{prf:example}
:label: my-example3
\begin{eqnarray*}
y''+5y'+6y=e^{4t}
\end{eqnarray*}

1. homogeneous solution:
\begin{eqnarray*}
r^2+5r+6=0 \rightarrow r = -2, -3\\\\
\Longrightarrow y_{h}(t) = c_{1}e^{-2t}+c_{2}e^{-3t}
\end{eqnarray*}

2. nonhomogeneous/particular solution by guessing the form of source/input term.
We have one undetermined coefficient Y.
\begin{eqnarray*}
y_{p}(t) &=& Ye^{4t} \rightarrow 16Y+20Y+6Y = 1 \rightarrow Y=\frac{1}{42} \\\\
&\Longrightarrow& y_{p}(t) = \frac{1}{42}e^{4t}
\end{eqnarray*}

3. general/complete solution:
\begin{eqnarray*}
y(t) = c_{1}e^{-2t}+c_{2}e^{-3t} + \frac{1}{42}e^{4t}
\end{eqnarray*}

````






