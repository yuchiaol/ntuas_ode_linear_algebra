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

(week8)=

# Week8 - Columns and rows of matrix A

## The geometry of linear equations
Consider the two below equations. We want to solve x and y.
\begin{eqnarray*}
2x - y &=& 0 \\\\
-x + 2y &=& 3
\end{eqnarray*}

We can write them in matrix form:
\begin{eqnarray*}
\begin{bmatrix}
2 & -1 \\
-1 & 2
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
=
\begin{bmatrix}
0 \\
3
\end{bmatrix}
\end{eqnarray*}

- row picture

- column picture (linear combination of columns)
\begin{eqnarray*}
x
\begin{bmatrix}
2 \\
-1
\end{bmatrix}
+
y
\begin{bmatrix}
-1 \\
2
\end{bmatrix}
=
\begin{bmatrix}
0 \\
3
\end{bmatrix}
\end{eqnarray*}

Row picture shows more intuitive depictions, at least, in three dimensional questions. For example:
\begin{eqnarray*}
2x-y &=& 0 \\\\
-x+2y-z &=& -1 \\\\
-3y+4z &=& 4
\end{eqnarray*}

In matrix form:
\begin{eqnarray*}
\begin{bmatrix}
2 & -1 & 0 \\
-1 & 2 & -1 \\
0 & -3 & 4
\end{bmatrix}
\begin{bmatrix}
x \\
y \\
z
\end{bmatrix}
=
\begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}
\end{eqnarray*}






