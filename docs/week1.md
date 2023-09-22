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

(week1)=

# Week1 - overview of ODEs

## Overview of ordinary differential equations (ODEs)
- linear -> superposition
- nonlinear -> cannot solve
- constant coefficients are nice.

## First order linear ODEs
- general form: $\frac{dy}{dt} = ay + q(t)$ or $\frac{dy}{dt} = p(t)y + q(t)$
- $\frac{dy}{dt}$ means rate of change.

### Examples of first order ODE. 
solve and assume $y(0)=1$.
1. $\frac{dy}{dt}=y$ -> $y(t)=e^{t}$
2. $\frac{dy}{dt}=-y$ -> $y(t)=e^{-t}$
3. $\frac{dy}{dt}=2ty$ -> $y(t)=e^{t^{2}}$
4. $\frac{dy}{dt}=y^{2}$ -> $y(t)=\frac{1}{1-t}$


## Second order linear ODEs
- $\frac{d^{2}y}{dt^{2}} = -ky$, $\frac{d^{2}y}{dt^{2}}$ indicates acceleration or curvature.
- $my^{''}+by^{'}+ky=f(t)$, where $by^{'}$ implies dampling.

## System of $n$ equations
- $\frac{d\vec{y}}{dt}=A\vec{y}$, where $A$ is a $n\times n$ matrix
- $\frac{d^{2}\vec{y}}{dt^{2}}=-S\vec{y}$

## Numerical solutions
- MATLAB ode45
- neural network to solve ODEs
- ChatGPT to solve ODEs (BE CAREFULL!)

## Partial differential euqations (PDEs)
- heat equation: $\frac{\partial u}{\partial t}=\frac{\partial^{2} u}{\partial x^{2}}$
- wave equation: $\frac{\partial^{2} u}{\partial t^{2}}=\frac{\partial^{2} u}{\partial x^{2}}$
- Laplace equation: $\frac{\partial^{2} u}{\partial x^{2}}+\frac{\partial^{2} u}{\partial y^{2}}=0$

## The calculus you need
- derivitives of functions: $x^{n}, \sin{x}, \cos{x}, e^{x}, \ln{x}$
- rules for derivatives:
	- sum rule
	- product rule
	- quotient rule
	- chain rule: $\frac{dy}{dt}=\frac{dy}{dx}\frac{dx}{dt}$
- fundamental theorem of calculus:

$$
  \int_{a}^{b} \frac{dy}{dx}\,dx = y(b) - y(a)
$$

$$
  \frac{d}{dx}\int_{a}^{x} f(s)\,ds = f(x)
$$

### An example, use all rules
 

