---
title: L'Hôpital's rule
sidebar:
  nav: docs-en
aside:
  toc: true
key: 2024062802_en
tags: Calculus
lang: en

---

# L'Hôpital's Rule

L'Hôpital's Rule is extremely useful for calculating limits that are difficult or impossible to evaluate using other methods. An indeterminate form is a situation where the limit cannot be directly applied to determine the value. Indeterminate forms include $\frac{0}{0}$, $\frac{\pm\infty}{\pm\infty}$, $0\times\infty$, $\infty-\infty$, $0^0$, and $1^{\infty}$. Most limits where L'Hôpital's Rule is applied are of the forms $\frac{0}{0}$ and $\frac{\pm\infty}{\pm\infty}$.

L'Hôpital's Rule is stated as follows:

$$
\lim_{x\to c}\frac{f(x)}{g(x)}=\lim_{x\to c}\frac{f^{\prime}(x)}{g^{\prime}(x)}
$$

L'Hôpital's Rule can be applied under the following conditions:

- **Indeterminate Form**:
  The limit must initially be in the form $\frac{0}{0}$ or $\frac{\pm\infty}{\pm\infty}$. For other indeterminate forms like $0 \times \infty$, $\infty - \infty$, $0^0$, $1^\infty$, and $\infty^0$, algebraic manipulation may be needed to transform them into $\frac{0}{0}$ or $\frac{\pm\infty}{\pm\infty}$ before applying L'Hôpital's rule.
- **Continuity and Differentiability**:
  The functions $f(x)$ and $g(x)$ must be continuous and differentiable near the point $c$ (excluding possibly at $c$ itself).

- **Non-Zero Derivative**:
  The derivative $g^{\prime}(x)$ must not be zero in an open interval around $c$.

L'Hôpital's rule says that the limit of a quotient of functions is equal to the limit of the quotient of their derivatives, provided that the given conditions are satisfied.



## Proof of L'Hôpital's Rule

We are assuming that $\lim_{x\to c}f(x)=0$ and $\lim_{x\to c}g(x)=0$. Let

$$
L=\lim_{x\to c}\frac{f^{\prime}(x)}{g^{\prime}(x)}
$$

First, we need to show that $\lim_{x\to c}\frac{f(x)}{g(x)}=L$. Define

$$
F(x) = 
\begin{cases} 
f(x) & \text{if } x \neq c \\
0 & \text{if } x = c 
\end{cases}
\quad
G(x) = 
\begin{cases} 
g(x) & \text{if } x \neq c \\
0 & \text{if } x = c 
\end{cases}
$$

The auxiliary functions $F$ and $G$ help extend $f(x)$ and $g(x)$ to be continuous at $c$, making the application of the Cauchy's Mean Value Theorem more straightforward.
{:.info}

Since $f$ is continuous on $\\{x \in I \mid x \neq c\\}$, we can see that the function $F$ is continuous on the interval $I$.
$$
\lim_{x\to c}F(x)=\lim_{x\to c}f(x)=0=F(c)
$$

Similarly, $G$ is also continuous on the interval $I$. Let $x \in I$ and $x > a$. Then the functions $F$ and $G$ are continuous on the closed interval $[a, x]$ and differentiable on the open interval $(a, x)$. Additionally, $G^{\prime}(x) \neq 0$ (since $G^{\prime}(x) = g^{\prime}(x)$ and $g(x) \neq 0$).


Therefore, by **Cauchy's Mean Value Theorem**, there exists some $y$ such that $c < y < x$ which satisfies the following equation:

$$
\frac{F^{\prime}(y)}{G^{\prime}(y)}=\frac{F(y)-F(c)}{G(y)-G(c)}=\frac{F(y)}{G(y)}
$$

Now, if we let $x \to c^+$, then $y \to c^+$ (since $c < y < x$), so

$$
\lim_{x\to c^+}\frac{f(x)}{g(x)}=\lim_{x\to c^+}\frac{F(x)}{G(x)}=\lim_{y\to c^+}\frac{F^{\prime}(y)}{G^{\prime}(y)}=\lim_{y\to c^+}\frac{f^{\prime}(y)}{g^{\prime}(y)}=L
$$

A similar argument shows that the left-hand limit is also $L$. Therefore,

$$
\lim_{x\to c}\frac{f(x)}{g(x)}=L
$$

So far, we have considered the case where $c$ is finite. How do we prove it when $c$ is infinite? This can be addressed by the substitution $x = 1/t$.

$$
\lim_{x\to\infty}\frac{f(x)}{g(x)}=\lim_{t\to0^+}\frac{f(1/t)}{g(1/t)}
$$

Here, we can apply L'Hôpital's Rule.

$$
\begin{aligned}
\lim_{t\to0^+}\frac{f(1/t)}{g(1/t)}&=\lim_{t\to0^+}\frac{f^{\prime}(1/t)(-1/t^2)}{g^{\prime}(1/t)(-1/t^2)} \\
&=\lim_{t\to0^+}\frac{f^{\prime}(1/t)}{g^{\prime}(1/t)}=\lim_{x\to\infty}\frac{f^{\prime}(x)}{g^{\prime}(x)}
\end{aligned}
$$

This completes the proof of L'Hôpital's Rule.



# Reference

* Stewart, J. (2018). *Calculus: Early Transcendentals*.