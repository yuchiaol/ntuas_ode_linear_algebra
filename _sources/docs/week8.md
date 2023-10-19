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
\underbrace{\begin{bmatrix}
2 & -1 \\
-1 & 2
\end{bmatrix}}_{A}
\underbrace{\begin{bmatrix}
x \\
y
\end{bmatrix}}_{\vec{x}}
=
\underbrace{\begin{bmatrix}
0 \\
3
\end{bmatrix}}_{\vec{b}}
\end{eqnarray*}

- row picture

- column picture (linear combination of columns)
\begin{eqnarray*}
x
\underbrace{\begin{bmatrix}
2 \\
-1
\end{bmatrix}}_{\vec{col1}}
+
y
\underbrace{\begin{bmatrix}
-1 \\
2
\end{bmatrix}}_{\vec{col2}}
=
\underbrace{\begin{bmatrix}
0 \\
3
\end{bmatrix}}_{\vec{b}}
\end{eqnarray*}

Row picture shows more intuitive depictions, at least, in three dimensional questions. For example:
\begin{eqnarray*}
2x-y &=& 0 \\\\
-x+2y-z &=& -1 \\\\
-3y+4z &=& 4
\end{eqnarray*}

In matrix form:
\begin{eqnarray*}
\underbrace{\begin{bmatrix}
2 & -1 & 0 \\
-1 & 2 & -1 \\
0 & -3 & 4
\end{bmatrix}}_{A}
\underbrace{\begin{bmatrix}
x \\
y \\
z
\end{bmatrix}}_{\vec{x}}
=
\underbrace{\begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}}_{\vec{b}}
\end{eqnarray*}

- row picture

- column picture
\begin{eqnarray*}
x
\underbrace{\begin{bmatrix}
2 \\
-1 \\
0
\end{bmatrix}}_{\vec{col1}}
+
y
\underbrace{\begin{bmatrix}
-1 \\
2 \\
3
\end{bmatrix}}_{\vec{col2}}
+
z
\underbrace{\begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}}_{\vec{col3}}
=
\underbrace{\begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}}_{\vec{b}}
\end{eqnarray*}

We can solve this system. If we change the vector on right hand side:
\begin{eqnarray*}
x
\underbrace{\begin{bmatrix}
2 \\
-1 \\
0
\end{bmatrix}}_{\vec{col1}}
+
y
\underbrace{\begin{bmatrix}
-1 \\
2 \\
3
\end{bmatrix}}_{\vec{col2}}
+
z
\underbrace{\begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}}_{\vec{col3}}
=
\underbrace{\begin{bmatrix}
1 \\
1 \\
-3
\end{bmatrix}}_{\vec{b}}
\end{eqnarray*}
can we still solve it? So a more general questions is: 
1. can we solve Ax = b fpr every b?
2. do the linear combinations of the collumns fill 3-D space?

For this matrix A, yes because A is nonsingular or invertible!

## Ax is a linear combination of columns of A


## Elimination with matrices










