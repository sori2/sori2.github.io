---
title: "Naive Bayes Classifier"
categories: [Machine_Learning]
tag: [Machine_Learning]
toc: true
toc_sticky: true
author_profile: true

---

# Naive Bayes Classifier

The Naive Bayes classifier is a type of supervised learning algorithm based on **Bayes' theorem**. This probabilistic machine learning algorithm uses Bayes' theorem to predict the class to which a particular data point belongs. The algorithm is simple yet powerful, and is widely used in text classification tasks such as spam email filtering, sentiment analysis, and document classification.

The Naive Bayes classifier works by calculating the probability that a given data point belongs to a specific class, and then selecting the class with the highest probability. Here, Bayes' theorem is used to select the class. The Naive Bayes classifier simplifies calculations by assuming that all features are **conditionally independent** of each other. This assumption is used to handle the combinatorial explosion and sample sparsity problems when solving Bayes' theorem. Although this assumption may not hold strictly in reality, the Naive Bayes classifier performs well in many practical applications. The term "*naive*" comes from this assumption of conditional independence. The Naive Bayes classifier uses the following form of Bayes' theorem:

$$
P(c \mid \mathbf{x}) = \frac{P(\mathbf{x} \mid c)P(c)}{P(\mathbf{x})}
$$

Given $N$ classification labels $\mathcal{Y} = \\{c_1, c_2, \dots, c_N\\}$, $c$ is the class (label) we want to predict, and $\mathbf{x} = (x_1,x_2, \dots, x_n)$ is a vector composed of $n$ features. Therefore, $P(c \mid \mathbf{x})$ represents the probability that the given feature vector $\mathbf{x}$ belongs to class $c$. This is the value we ultimately want to predict. The denominator $P(\mathbf{x})$ is independent of $c$ and has the same value for all classes, so it can be treated as a constant when comparing class probabilities. Therefore, $P(\mathbf{x})$ does not need to be considered, and we only need to consider the following:

$$
P(c \mid \mathbf{x}) \propto P(\mathbf{x} \mid c)P(c)
$$

Simplifying the right-hand side, we get:

$$
\begin{aligned}
P(\mathbf{x} \mid c)P(c) &= P(x_1,x_2, \dots, x_n \mid c)P(c) \\
&= \frac{P(c, x_1, \dots, x_n)}{P(c)} \cdot P(c) \\
&= P(c, x_1, \dots, x_n) \\
&= P(c)P(x_1 \mid c)P(x_2 \mid c, x_1) \cdots P(x_n \mid c, x_1,x_2, \dots, x_{n-1})
\end{aligned}
$$

The Naive Bayes classifier is based on naive conditional independence assumptions. That is, each feature $x_i$ is **conditionally independent** of every other feature $x_j$ for $i \neq j$. This means that

$$
P(x_i \mid x_j, c) = P(x_i \mid c)
$$

and so the joint model can be expressed as

$$
\begin{aligned}
P(x_1,x_2, \dots, x_n, c) &= P(c)P(x_1 \mid c)P(x_2 \mid c) \cdots P(x_n \mid c) \\
&= P(c)\prod_{i=1}^n P(x_i \mid c)
\end{aligned}
$$

Therefore,

$$
P(c \mid \mathbf{x}) = \frac{1}{Z}P(c)\prod_{i=1}^n P(x_i \mid c)
$$

Note: The normalizing constant $Z$ corresponds to $P(\mathbf{x})$, which is an independent scaling factor for the class $c$. That is, a constant if the values of the feature variables are known.

The goal of the Naive Bayes classifier can be expressed as:

$$
h_{nb}(\mathbf{x}) = \underset{c \in \mathcal{Y}}{\mathrm{argmax}} \, P(c) \prod_{i=1}^n P(x_i \mid c)
$$

Here, $h_{nb}(\mathbf{x})$ represents the class with the highest probability using the Naive Bayes classifier for the given feature vector $\mathbf{x}$.

# Reference

* Murty, M. N., & Devi, V. S. (2011). *Pattern Recognition: an Algorithmic approach*. Springer , Universities Press.
- Zhou, Z. (2021). *Machine learning*. Springer Nature.