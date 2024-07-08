---
title: "Chi-Square Distribution"
categories: [Probability]
tag: [Probability]
toc: true
toc_sticky: true
author_profile: true
---

# Chi-Square Distribution

## Chi-Square Distribution

The Chi-Squared distribution, denoted as $\chi^2(r)$, is a special case of the Gamma distribution with $\alpha = r/2$ and $\beta = 2$. It is widely used in statistics, particularly in hypothesis testing and in constructing confidence intervals.

$$
f_X(x)=
\begin{cases}
\frac{1}{\Gamma(r/2)2^{r/2}}{x^{r/2-1}e^{-x/2}}& \text{for } 0 < x < \infty \\
0 & \text{otherwise}
\end{cases}
$$

The parameter $r$ is known as the degrees of freedom, which must be a positive integer. The degrees of freedom typically correspond to the number of independent random variables being summed.

## Chi-Square Properties

Let $X$ have a $\chi^2(r)$ distribution with $r\in(0,\infty)$ degree of freedom. If $k > -(r/2)$, then $E(X^k)$ exists and can be calculated as follows:

$$
\frac{2^k \Gamma\left(\frac{r}{2} + k\right)}{\Gamma\left(\frac{r}{2}\right)}
$$

The proof is as follows.

By performing the change of variable $u = x/2$ in the following integral, we get:

$$
E(X^k) = \int_{0}^{\infty} \frac{1}{\Gamma(r/2) 2^{r/2}} x^{(r/2) + k - 1} e^{-x/2} \, dx
$$

This results in:

$$
\begin{aligned}
E(X^k) &= \int_{0}^{\infty} \frac{1}{\Gamma(r/2) 2^{r/2}} (2u)^{(r/2) + k - 1} e^{-u} \cdot 2 \, du \\
&= \int_{0}^{\infty} \frac{1}{\Gamma(r/2) 2^{r/2}} 2^{(r/2) + k - 1} u^{(r/2) + k - 1} e^{-u} \cdot 2 \, du \\
&= \int_{0}^{\infty} \frac{1}{\Gamma(r/2) 2^{r/2}} 2^{(r/2) + k} u^{(r/2) + k - 1} e^{-u} \, du \\
&= \frac{2^{(r/2) + k}}{\Gamma(r/2) 2^{r/2}} \int_{0}^{\infty} u^{(r/2) + k - 1} e^{-u} \, du \\
&= \frac{2^k \Gamma\left(\frac{r}{2} + k\right)}{\Gamma\left(\frac{r}{2}\right)}
\end{aligned}
$$

Thus, we obtain the desired result for $k > -(r/2)$,  all moments of the $\chi^2(r)$ distribution exist, and the $k$-th moment is given by:

$$
E(X^k) = \frac{2^k \Gamma\left(\frac{r}{2} + k\right)}{\Gamma\left(\frac{r}{2}\right)}
$$

The basic statistics are as follows.
Let $X\sim \chi^2(r)$. ($X \sim \text{Gamma}(\alpha=r/2,\ \beta=2)$)

- The **mean** is  
  
  $$
  \mu = E(X) = r
  $$

- The **variance** is 
  
  $$
  \sigma^2 = \operatorname{Var}(X) = 2r
  $$

- The **moment generating function is** 
  
  $$
  M(t)=\frac{1}{(1 - 2 t)^{r/2}}
  $$
  
  for $t <1/2$.

## Additive Property of Chi-Square Distributed Variables

Since the chi-square distribution is a sub-distribution of the gamma distribution, the additive property of the gamma distribution is also established in the chi-square distribution

If $X_1, X_2, \ldots, X_n$ follow the distribution $X_i\sim \chi^2(r)$ for $i=1,2,\ldots,n$, then,

$$
Y = \sum_{i=1}^{n} X_i \sim \chi^2(r)\left(\sum_{i=1}^{n} r_i\right)
$$

# References

* Ross, S. (2010). *A First Course in Probability (8th ed.)*. Pearson.
* Hogg, R. V., McKean, J. W., & Craig, A. T. (2020). *Introduction to mathematical statistics*. Pearson. 