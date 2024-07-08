---
title: Bayes' Theorem
sidebar:
  nav: docs-en
aside:
  toc: true
key: 2024063002_en
tags: Probability
lang: en
---

# Law of Total Probability

If the events $A_1,A_2,\dots,A_k$ constitute a **partition** of the sample space $S$ such that ${P(A_i)}\neq0$ for $i=1,2,...,k$. That is, $A_i$ are **mutually exclusive** and **exhaustive**. then for any event $B$ of $S$,

$$
P(B)=\sum_{i=1}^{k}P(A_{i}\cap B)=\sum_{i=1}^{k}P(A_{i})P(B\mid A_{i})
$$

The proof is as follows:

Let the $k$ events $A_1,A_2,\dots,A_k$ constitute a partition of the sample space $S$. That is, $A_i$ are mutually exclusive and exhaustive:

$$
A_i\cap A_j=\emptyset,\text{ for }i\not=j\text{ and }S=A_{1}\cup A_{2} \cup\cdots\cup A_k
$$

Now, if $B$ is an event, then $B$ can be written as the union of $k$ mutually exclusive events, namely:

$$
\begin{aligned}
B &= B\cap S \\
&= B\cap\left(\bigcup_{i=1}^kA_i\right) \\
&=(B\cap A_1)\cup(B\cap A_2)\cup\cdots\cup(B\cap A_k)
\end{aligned}
$$

Then,

$$
\begin{aligned}
P(B)  &= P[(B\cap A_1)\cup(B\cap A_2)\cup\cdots\cup(B\cap A_k)] \\
&= P(B\cap A_1) + P(B\cap A_2) + \dots + P(B\cap A_k)\\
&=\sum_{i=1}^{k}P(A_{i}\cap B) \\
&=\sum_{i=1}^{k}P(A_{i})P(B\mid A_{i})
\end{aligned}
$$


# Bayes' theorem

Let the $m$ events $A_1,A_2,...,A_m$ constitute a **partition** of the sample space $S$. That is, $A_i$ are **mutually exclusive** and **exhaustive**. In addition, $P(A_i)>0$. Then for any event $B$ with $P(B)>0$,

$$
P(A_{k}\mid B)=\frac{P(A_{k}\cap B)}{P(B)}=\frac{P(A_k)P(B\mid A_k)}{\sum_{i=1}^{m}P(A_{i})P(B\mid A_{i})}
$$

The importance of Bayes' theorem lies in its ability to infer the probability of an event based on prior experience and current evidence. It allows us to update our initial beliefs about an event in an objective manner with new information, thereby improving our understanding.

Let's review the simple form of Bayes' theorem:

$$
P(A \mid B) = \frac{P(A)P(B \mid A)}{P(B)}
$$

Bayes' theorem can be interpreted as follows:

- $P(A \mid B)$: **Posterior**. The updated probability of event $A$ after event $B$ has occurred. This is the final probability we seek to determine.
- $P(A)$: **Prior**. The probability of event $A$ before event $B$ occurs.
- $P(B \mid A)$: **Likelihood**. The probability of event $B$ given that event $A$ has occurred. To properly understand the likelihood, one must understand Bayesian statistic, which will be explained in a later post.
- $P(B)$: **Evidence** or **Normalizing Constant**. It adjusts the scale of the probability. Probabilities must be between $0$ and $1$, and the total probability of all possible events must sum to $1$. Thus, the probability values need to be normalized to ensure that the total sum of the probability distribution is $1$.


#  Reference

* Ross, S. (2010). *A First Course in Probability (8th ed.)*. Pearson.
* Hogg, R. V., McKean, J. W., & Craig, A. T. (2020). *Introduction to mathematical statistics*. Pearson. 
* Walpole, R. E. (2014). *Probability and statistics for Engineers & Scientists*. Pearson. 