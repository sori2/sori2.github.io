---
title: Gamma Distribution
sidebar:
  nav: docs-en
aside:
  toc: true
key: 2024062701_en
tags: Probability
lang: en
---

# Gamma Function

The definition of the Gamma distribution requires the Gamma function from calculus. For $\alpha > 0$, it has been proven that the following integral exists and is positive:

$$
\int_{0}^{\infty}y^{\alpha-1}e^{-y} \, dy
$$

This integral is called the **Gamma function** and is denoted as follows:

$$
\Gamma(\alpha)=\int_{0}^{\infty}y^{\alpha-1}e^{-y} \, dy
$$

When $\alpha=1$

$$
\Gamma(1)=\int_{0}^{\infty}e^{-y} \, dy=1
$$

When $\alpha > 1$, Using integration by parts, we can derive the recursive property of the Gamma function:

$$
\begin{aligned}
\Gamma(\alpha) &= \int_0^\infty y^{\alpha-1} e^{-y} \, dy \\
&= \left. -y^{\alpha-1} e^{-y} \right|_0^\infty + \int_0^\infty (\alpha-1)y^{\alpha-2} e^{-y} \, dy \\
&= (\alpha-1) \int_0^\infty y^{\alpha-2} e^{-y} \, dy \\
&= (\alpha-1) \Gamma(\alpha-1)
\end{aligned}
$$

Therefore, for any positive integer $\alpha>1$

$$
\Gamma(\alpha)=(\alpha-1)(\alpha-2)\cdots(3)(2)\Gamma(1)=(\alpha-1)!
$$

Since $\Gamma(1) = 1$, we can write $0! = 1$. The Gamma function is sometimes referred to as the factorial function because of this relationship.



# Gamma Distribution

## Gamma Distribution

A continuous random variable $X$ follows a **gamma distribution** with parameters $\alpha>0$ and $\beta > 0$ if its probability density function is: 

$$
f_X(x)=
\begin{cases}
\frac{x^{\alpha-1}e^{-x/\beta}}{\Gamma(\alpha)\beta^{\alpha}}& \text{for } 0 < x < \infty \\
0 & \text{otherwise}
\end{cases}
$$

In this case, $X$ follows a $\Gamma(\alpha, \beta)$ distribution.

To verify that $f_X(x)$ is a valid PDF, we first confirm that $f_X(x) > 0$ for all $x > 0$. Next, to show that the integral of $f_X(x)$ equals 1, we use the variable transformation $z = x/\beta$ and $dz = (1/\beta) \, dx$ in the following derivation:

$$
\begin{aligned}
\int_{0}^{\infty} f_X(x) \, dx &= \int_{0}^{\infty} \frac{ x^{\alpha-1} e^{-x/\beta}}{\Gamma(\alpha)\beta^\alpha} \, dx \\
&= \frac{1}{\Gamma(\alpha)\beta^\alpha}\int_{0}^{\infty}(\beta z)^{\alpha-1}e^{-z}\beta \, dz \\
&= \frac{1}{\Gamma(\alpha)\beta^\alpha}\cdot\Gamma(\alpha)\beta^\alpha\\
&= 1
\end{aligned}
$$

Thus, it is proven that $f_X(x)$ is a valid probability density function (PDF).



## Gamma Properties

To find the mgf of $X$, we use a similar variable transformation in the following derivation:

$$
\begin{aligned}
M_X(t) &= \int_{0}^{\infty} e^{tx}\frac{ x^{\alpha-1} e^{-x/\beta}}{\Gamma(\alpha)\beta^\alpha} \, dx \\
&= \int_{0}^{\infty} \frac{1}{\Gamma(\alpha)\beta^\alpha} x^{\alpha-1} e^{-x(\frac{1}{\beta}-t)} \, dx \\
\end{aligned}
$$

Here, we use the substitution $\beta^\ast = (\frac{1}{\beta} - t)^{-1}$, ($\beta=\beta^\ast(1-\beta t),\  \beta^\ast > 0, \ t < \frac{1}{\beta}$)

$$
\begin{aligned} M_X(t) &= \int_{0}^{\infty} e^{tx} \frac{x^{\alpha-1} e^{-x/\beta}}{\Gamma(\alpha) \beta^\alpha} \, dx \\ &= \int_{0}^{\infty} \frac{1}{\Gamma(\alpha) (\beta^* (1 - \beta t))^\alpha} x^{\alpha-1} e^{-x/\beta^*} \, dx \\ &= \frac{1}{(1 - \beta t)^\alpha} \int_{0}^{\infty} \underbrace{\frac{1}{\Gamma(\alpha) (\beta^*)^\alpha} x^{\alpha-1} e^{-x/\beta^*}}_{ \text{PDF of } \Gamma(\alpha, \beta^*)} \, dx \\ &= \frac{1}{(1 - \beta t)^\alpha}, \quad \text{for } t < \frac{1}{\beta} \end{aligned}
$$

Note that the technique of making the form of an equation in an integral into pdf is often used.

Now,

$$
\begin{aligned}
{M_X}^\prime(t) &= (-\alpha)(1-\beta t)^{-\alpha-1}(-\beta) \\
{M_X}^{\prime\prime}(t) &= (-\alpha)(\alpha-1)(1-\beta t)^{-\alpha-2}(-\beta)^2
\end{aligned}
$$

Therefore, we obtain the following from the gamma distribution.

$$
\begin{aligned}
\mu={M_X}^{\prime}(0) &= \alpha\beta \\
\sigma^2 ={M_X}^{\prime\prime}(0)-{M_X}^{\prime}(0) &= \alpha\beta^2
\end{aligned}
$$

Let $X \sim \text{Gamma}(\alpha, \beta)$.

- The **mean** is  

  $$
  \mu = E(X) = \alpha\beta
  $$

- The **variance** is 

  $$
  \sigma^2 = \operatorname{Var}(X) = \alpha\beta^2
  $$

- The **moment generating function is** 

  $$
  M(t)=\frac{1}{(1 - \beta t)^\alpha}
  $$

  for $t <1/\beta$.

## Additive Property of Gamma Distributed Variables
If $X_1, X_2, \ldots, X_n$ follow the distribution $X_i \sim \text{Gamma}(\alpha_i, \beta)$ for $i=1,2,\ldots,n$, then,

$$
Y = \sum_{i=1}^{n} X_i \sim \text{Gamma}\left(\sum_{i=1}^{n} \alpha_i, \beta\right)
$$



The proof is as follows.

Using the given independence and the mgf of the Gamma distribution, for $t < 1/\beta$, we have:

$$
M_Y(t) =  \prod_{i=1}^{n} M_{X_i}(t)=\prod_{i=1}^{n} (1 - \beta t)^{-\alpha_i} = (1 - \beta t)^{-\sum_{i=1}^{n} \alpha_i}
$$

This is the mgf of the $\text{Gamma}\left(\sum_{i=1}^{n} \alpha_i, \beta\right)$ distribution.


#  Reference

* Ross, S. (2010). *A First Course in Probability (8th ed.)*. Pearson.
* Hogg, R. V., McKean, J. W., & Craig, A. T. (2020). *Introduction to mathematical statistics*. Pearson. 
