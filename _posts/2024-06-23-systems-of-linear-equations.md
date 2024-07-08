---
title: Systems of Linear Equations
sidebar:
  nav: docs-en
aside:
  toc: true
key: 2024062301_en
tags: Linear_Algebra
lang: en
---

# Systems of Linear Equations

A **linear equation** in the variables $x_1, \ldots, x_n$ is an equation that can be written in the form

$$ a_1x_1 + a_2x_2 + \cdots + a_nx_n = b $$

where $b$ and the **coefficients** $a_1, \ldots, a_n$ are real or complex numbers, usually known in advance. 

A **system of linear equations** consists of a collection of one or more linear equations involving the same set of variables. For example, a system of $m$ linear equations in $n$ variables can be written as: 

$$
\begin{aligned}
    a_{11}x_{1} + a_{12}x_{2} + \cdots + a_{1n}x_{n} &= b_{1} \\
    a_{21}x_{1} + a_{22}x_{2} + \cdots + a_{2n}x_{n} &= b_{2} \\
    &\vdots \\
    a_{m1}x_{1} + a_{m2}x_{2} + \cdots + a_{mn}x_{n} &= b_{m}
\end{aligned}
$$

For example,

$$
\begin{aligned}
	x_1 - 2x_2 &= -1 \\
	-x_1 + 3x_2 &= 3
\end{aligned}
$$

A system of linear equations has

1. no solution, or
2. exactly one solution, or
3. infinitely many solutions. 

The reasoning behind these three possibilities lies in the nature of linear equations and the geometric interpretation of their solutions:

1. No Solution: Parallel lines that never meet.
2. Exactly One Solution: Intersecting lines at one unique point.
3. Infinitely Many Solutions: Coincident lines that overlap completely.

These scenarios exhaust all the possibilities for the relationships between two or more linear equations in a plane. Thus, a system of linear equations cannot have, for example, exactly two solutions, as that would require the lines to intersect at exactly two points, which is not possible for linear (straight) lines.

A system of linear equations is said to be **consistent** if it has either one solution or infinitely many solutions; a system is **inconsistent** if it has no solution.r equations is said to be **consistent** if it has either one solution or infinitely many solutions; a system is **inconsistent** if it has no solution.

# Matrix Notation

Such a system can be represented in matrix form as $A \mathbf{x} = \mathbf{b}$, where $A$ is an $m \times n$ matrix of coefficients, $\mathbf{x}$ is a column vector of the variables, and $\mathbf{b}$ is a column vector of the constants:

$$
A = \begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{pmatrix}, \quad
\mathbf{x} = \begin{pmatrix}
x_1 \\
x_2 \\
\vdots \\
x_n
\end{pmatrix}, \quad
\mathbf{b} = \begin{pmatrix}
b_1 \\
b_2 \\
\vdots \\
b_m
\end{pmatrix}
$$

The solution to a system of linear equations is the set of all possible values of the variables that satisfy all of the equations simultaneously. This can be achieved using various methods such as Gaussian elimination, matrix inversion, or iterative methods.

# Reference

* Stewart, J. (2018). *Calculus: Early Transcendentals*.