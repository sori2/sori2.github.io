---
title: Basic Set Theory
sidebar:
  nav: docs-en
aside:
  toc: true
key: 2024062202_en
tags: Probability
lang: en
---

# What is a set?

A **set** is a fundamental concept in mathematics, representing a collection of **distinct objects**, considered as an object in its own right. This means that $\\{1, 2, 3\\}$ is a set, but $\\{2, 2, 3\\}$ is not because $2$ appears twice in the second collection.

The objects within a set are called *elements*. Sets are usually denoted by capital letters such as $A$, $B$, $C$, etc. To indicate that set $A$ contains element $x$, we write $x \in A$. Sets are also defined by listing their elements within curly braces. For example, $A = \\{1, 2, 3\\}$ is a set containing the elements 1, 2, and 3.

The order and repetition of elements in a set do not matter; only the inclusion of elements is important. Therefore, $\\{1, 2, 3\\}$ and $\\{3, 2, 1\\}$ are the same set.

# Basic Set Theory

## Intersection

The **intersection of events** $A$ and $B$, denoted $A ∩ B$, is the collection of all outcomes that are elements of both of the sets $A$ and $B$. It corresponds to combining descriptions of the two events using the word “**and.**” Let $C = A ∩ B$.



### Example

Consider two events in a 6-sided die roll:

- $A$: The event that an even number is rolled, $A = \\{2, 4, 6\\}$.
- $B$: The event that a number greater than 3 is rolled, $B = \\{4, 5, 6\\}$.

The intersection of $A$ and $B$ is:

$$
A∩B=\{4,6\}
$$

This represents the outcomes that are both even and greater than 3.

## Union

The **union of events** $A$ and $B$, denoted $A ∪ B$, is the collection of all outcomes that are elements of one or the other of the sets $A$ and $B$, or of both of them. It corresponds to combining descriptions of the two events using the word “**or.**” $C = A ∪ B$



### Example

Consider the same events from the previous example:

- $A$: The event that an even number is rolled, $A = \\{2, 4, 6\\}$.
- $B$: The event that a number greater than 3 is rolled, $B = \\{4, 5, 6\\}$.

The union of $A$ and $B$ is:

$$
A∪B=\{2,4,5,6\}
$$

This represents the outcomes that are either even, greater than $3$, or both.



## Complements

The **complement of an event** $A$ in a sample space $S$, denoted $A^{\prime}$ (or $A^\complement$), is the collection of all outcomes in $S$ that are not elements of the set $A$, It corresponds to negating any description in words of the event $A$.



### Example

Consider 6-sided die and 4-sided die and $A$ be an event that you roll $2$. What is $A^{\prime}$?

- Sample space: $S = \\{1, 2, 3, 4, 5, 6\\}$.
- Event $A$: Rolling a 2, $A = \\{2\\}$.

The complement of $A$ is:

$$
A^{\prime} = \{1,3,4,5,6\}
$$

This represents the outcomes where a $2$ is not rolled.



## Subtraction

For two sets $A$ and $B$, the **difference** (or **relative complement**) of $A$ and $B$, denoted $A \setminus B$, is the set of all elements that are in $A$ but not in $B$. Formally,

$$
A\setminus B = A\cap B^{\prime}
$$

 

## Mutually Exclusive Events

Events $A$ and $B$ are **mutually exclusive** if they have no elements in common. i.e.,

$$
A\cap B = \emptyset
$$

$\emptyset$ is the notation of the empty set, $\emptyset = \\{\\}$.

- for any event $A$, $A$ and $A^{\prime}$ are mutually exclusive.

### Example

Consider to toss a coin once. Let $A$ be an event that the coin lands on heads and $B$ be an event that the coin lands on tails. It is clear that the two events $A$ and $B$ cannot occur at the same time. In other words, $A ∩ B = ∅$. $A$ and $B$ **are mutually exclusive.**



## Properties of Set Operations

### Commutative Laws

$$
\begin{align}

A\cup B=B\cup A \\

A\cap B = B\cap A

\end{align}
$$

### Associative Laws

$$
\begin{align}

(A ∪ B) ∪ C = A ∪ (B ∪ C) \\

(A ∩ B) ∩ C = A ∩ (B ∩ C)

\end{align}
$$



### Distributive Laws

$$
\begin{align}

A ∩ (B ∪ C) = (A ∩ B) ∪ (A ∩ C) \\

A ∪ (B ∩ C) = (A ∪ B) ∩ (A ∪ C)

\end{align}
$$



### De Morgan's Laws

$$
\begin{align}

(A ∪ B)^{\prime} = A^{\prime} ∩ B^{\prime} \\

(A ∩ B)^{\prime} = A^{\prime} ∪ B^{\prime}

\end{align}
$$

# Reference

* Ross, S. (2010). A First Course in Probability (8th ed.). Pearson.