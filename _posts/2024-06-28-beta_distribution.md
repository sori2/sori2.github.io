---
title: Beta Distribution
sidebar:
  nav: docs-en
aside:
  toc: true
key: 2024062801_en
tags: Probability
lang: en
---

# Beta Function

For $\alpha, \beta > 0$, the Beta function is defined as follows:

$$
\mathrm{B}(\alpha, \beta) = \int_{0}^{1} x^{\alpha-1} (1-x)^{\beta-1} \, dx
$$

The Beta function can be expressed in terms of the Gamma function:

$$
\mathrm{B}(\alpha,\beta) = \frac{\Gamma(\alpha)\Gamma(\beta)}{\Gamma(\alpha+\beta)}
$$

The proof is as follows:

$$
\begin{align*}
\Gamma(\alpha) \Gamma(\beta) &= \int_{0}^{\infty} x^{\alpha-1} e^{-x} \, dx \cdot \int_{0}^{\infty} y^{\beta-1} e^{-y} \, dy \\
&= \int_{0}^{\infty} \int_{0}^{\infty} x^{\alpha-1} y^{\beta-1} e^{-(x+y)} \, dx \, dy \\
\end{align*}
$$

Next, we perform the substitution $x = zt$ and $y = z(1-t)$. Now, we calculate the Jacobian determinant $J$ for the transformation from $(x, \, y)$ to $(z, \, t)$:

$$
J = \frac{\partial(x,\, y)}{\partial(z,\, t)} = \begin{vmatrix}
\frac{\partial x}{\partial z} & \frac{\partial x}{\partial t} \\
\frac{\partial y}{\partial z} & \frac{\partial y}{\partial t}
\end{vmatrix} = \begin{vmatrix}
t & z \\
1 - t & -z
\end{vmatrix} = -z
$$

Therefore, the integral becomes:

$$
\begin{aligned}
\Gamma(\alpha) \Gamma(\beta) &= \int_{0}^{\infty} \int_{0}^{\infty} x^{\alpha-1} y^{\beta-1} e^{-(x+y)} \, dx \, dy \\
&= \int_{0}^{1} \int_{0}^{\infty} (zt)^{\alpha-1} (z(1-t))^{\beta-1} e^{-z} |J| \, dz \, dt \\
&= \int_{0}^{1} \int_{0}^{\infty} z^{\alpha-1} t^{\alpha-1} z^{\beta-1} (1-t)^{\beta-1} e^{-z} z \, dz \, dt \\
&= \int_{0}^{1} \int_{0}^{\infty} z^{\alpha+\beta-1} t^{\alpha-1} (1-t)^{\beta-1} e^{-z} \, dz \, dt \\
&= \int_{0}^{1} t^{\alpha-1} (1-t)^{\beta-1} \, dt\cdot \int_{0}^{\infty} z^{\alpha+\beta-1} e^{-z} \, dz \\
&= \mathrm{B}(\alpha, \beta) \Gamma(\alpha + \beta)
\end{aligned}
$$

Thus, we obtain the desired result:

$$
\mathrm{B}(\alpha, \beta) = \frac{\Gamma(\alpha)\Gamma(\beta)}{\Gamma(\alpha+\beta)}
$$

## Binomial Coefficient and Beta Function

Just as the factorial is generalized by the Gamma function, the Beta function can be seen as a generalization of the binomial coefficient.

$$
\binom{n}{k} = \frac{1}{(n + 1)\mathrm{B}(n - k + 1, k + 1)}
$$

The proof is as follows:

We start by using the definition of the binomial coefficient:

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!},\quad \text{for } 0\le k \le n.
$$

Using the relationship between the Gamma function and factorials, we can express the binomial coefficient in terms of Gamma functions:

$$
\binom{n}{k} = \frac{\Gamma(n+1)}{\Gamma(k+1)\Gamma(n-k+1)}
$$

Next, we use the identity that expresses the Beta function in terms of the Gamma function:

$$
\mathrm{B}(\alpha, \beta) = \frac{\Gamma(\alpha)\Gamma(\beta)}{\Gamma(\alpha+\beta)}
$$

In this case, we set $\alpha = n-k+1$ and $\beta = k+1$. Then, we have:

$$
\mathrm{B}(n-k+1, k+1) = \frac{\Gamma(n-k+1)\Gamma(k+1)}{\Gamma((n-k+1) + (k+1))} = \frac{\Gamma(n-k+1)\Gamma(k+1)}{\Gamma(n+2)}
$$

Rewriting the denominator $\Gamma(n+2)$ in terms of factorials, we get:

$$
\mathrm{B}(n-k+1, k+1) = \frac{\Gamma(n-k+1)\Gamma(k+1)}{(n+1)!}
$$

Substituting this into the expression for the binomial coefficient, we obtain:

$$
\binom{n}{k} = \frac{\Gamma(n+1)}{\Gamma(k+1)\Gamma(n-k+1)} = \frac{n!}{\Gamma(k+1)\Gamma(n-k+1)} \cdot \frac{\mathrm{B}(n-k+1, k+1)}{\mathrm{B}(n-k+1, k+1)}
$$

Simplifying this, we obtain the desired result:

$$
\binom{n}{k} = \frac{1}{(n+1)\mathrm{B}(n-k+1, k+1)}
$$

# Beta Distribution

## Beta Distribution

A continuous random variable $X$ follows a **beta distribution** with parameters $\alpha>0$ and $\beta > 0$ if its probability density function is: 

$$
f_X(x)=
\begin{cases}
\frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}x^{\alpha-1}(1-x)^{\beta-1}& \text{for } 0 < x < 1 \\
0 & \text{otherwise}
\end{cases}
$$

In this case, $X$ follows a $\mathrm{B}(\alpha, \beta)$ distribution.

To verify that $f_X(x)$ is a valid PDF, we first confirm that $f_X(x) > 0$ for all $x > 0$. Next, to show that the integral of $f_X(x)$ equals 1,

$$
\begin{aligned}
\int_{0}^{1} f_X(x) \, dx &= \int_{0}^{1} \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}x^{\alpha-1}(1-x)^{\beta-1} \, dx \\
&= \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}\int_{0}^{\infty}x^{\alpha-1}(1-x)^{\beta-1} \, dx \\
&= \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}\cdot\frac{\Gamma(\alpha)\Gamma(\beta)}{\Gamma(\alpha+\beta)}\\
&= 1
\end{aligned}
$$

Thus, it is proven that $f_X(x)$ is a valid probability density function (PDF).



## Beta Properties

Suppose that $X∼\text{Beta}(α,β)$. Then for $k>-\alpha$,

$$
\begin{aligned}
E(X^k) &= \int_0^1x^kf_X(x)\, dx \\
&= \int_0^1 \frac{\Gamma(\alpha + \beta)}{\Gamma(\alpha)\Gamma(\beta)} x^{k+\alpha-1} (1-x)^{\beta-1} \, dx \\
&= \frac{\Gamma(\alpha + \beta)}{\Gamma(\alpha)}\cdot\frac{\Gamma(\alpha + k)}{\Gamma(\alpha + \beta+k)}\int_0^1\underbrace{\frac{\Gamma(\alpha + \beta+k)}{\Gamma(\alpha+k)\Gamma(\beta)} x^{k+\alpha-1} (1-x)^{\beta-1}}_{ \text{PDF of } \mathrm{B}(\alpha+k, \beta)} \, dx\\
&= \frac{\Gamma(\alpha + \beta) \Gamma(\alpha + k)}{\Gamma(\alpha + \beta + k) \Gamma(\alpha)}=\frac{\mathrm{B}(\alpha+k, b)}{\mathrm{B}(\alpha, b)}
\end{aligned}
$$

From this, we can easily derive the mean and variance of the Beta distribution.

If $X$ is a Beta random variable with parameters $\alpha$ and $\beta$, then the following holds:

$$
\begin{aligned}
E(X) &= \frac{\mathrm{B}(\alpha+1, b)}{\mathrm{B}(\alpha, b)} \\
&=\frac{\Gamma(\alpha + \beta) \Gamma(\alpha + 1)}{\Gamma(\alpha + \beta + 1) \Gamma(\alpha)} \\
&= \frac{\Gamma(\alpha + \beta) \alpha\Gamma(\alpha)}{(\alpha+\beta)\Gamma(\alpha + \beta) \Gamma(\alpha)} \\
&= \frac{\alpha}{\alpha+\beta}
\end{aligned}
$$

Similarly, the following holds.

$$
\begin{aligned}
E(X^2) &= \frac{\mathrm{B}(\alpha+2, b)}{\mathrm{B}(\alpha, b)} \\
&= \frac{\mathrm{B}(\alpha+2, b)}{\mathrm{B}(\alpha+1, b)}\cdot\frac{\mathrm{B}(\alpha+1, b)}{\mathrm{B}(\alpha, b)} \\
&= \frac{(\alpha+1)\alpha}{(\alpha+\beta+1)(\alpha+\beta)}
\end{aligned}
$$

By the equation $\operatorname{Var}(X) = E(X^2) - (E(X))^2$, we obtain the following.

$$
\begin{aligned}
\operatorname{Var}(X)&=\frac{(\alpha+1)\alpha}{(\alpha+\beta+1)\alpha+\beta}-\left(\frac{\alpha}{\alpha+\beta}\right)^2 \\
&=\frac{\alpha\beta}{(\alpha+\beta)^2(\alpha+\beta+1)}
\end{aligned}
$$

Let $X \sim \text{Beta}(\alpha, \beta)$.

- The **mean** is  

  $$
  \mu = E(X) = \frac{\alpha}{\alpha+\beta}
  $$

- The **variance** is 

  $$
  \sigma^2 = \operatorname{Var}(X) = \frac{\alpha\beta}{(\alpha+\beta)^2(\alpha+\beta+1)}
  $$

#  Reference

* Ross, S. (2010). *A First Course in Probability (8th ed.)*. Pearson.
* Hogg, R. V., McKean, J. W., & Craig, A. T. (2020). *Introduction to mathematical statistics*. Pearson. 