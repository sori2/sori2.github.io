---
title: Vector
sidebar:
  nav: docs-en
aside:
  toc: true
key: 20240702_en
tags: Linear_Algebra
lang: en
---

# Vector

물리학에서 벡터(Vector)는 크기와 방향을 모두 가진 물리량을 의미합니다. 이러한 벡터는 다양한 물리적 상황을 설명하는 데 사용됩니다. 예를 들어, 힘, 속도, 가속도 등은 모두 벡터로 표현할 수 있습니다. 벡터는 방향을 가지고 있기 때문에, 단순히 크기만으로는 설명할 수 없는 여러 현상을 명확히 표현할 수 있습니다.

벡터는 두 가지 중요한 특징을 가지고 있습니다:

1. **크기 (Magnitude)**: 벡터의 크기는 벡터의 길이 또는 세기라고 할 수 있습니다. 이는 단순한 수치로 나타낼 수 있습니다.
2. **방향 (Direction)**: 벡터의 방향은 벡터가 향하고 있는 방향을 나타냅니다. 이는 주로 각도로 표현됩니다.

벡터는 그 크기와 방향만이 중요하며, 벡터가 어디에 위치했는지는 중요하지 않습니다. 다시 말해, 공간상의 위치가 다르더라도 크기와 방향이 동일하다면 두 벡터는 동일한 벡터로 간주됩니다. 이는 벡터의 중요한 성질 중 하나로, 이를 통해 우리는 벡터를 자유롭게 이동시키면서도 동일한 벡터로 취급할 수 있습니다.



# 벡터 공간

벡터 공간(Vector Space)은 선형대수학에서 매우 중요한 개념으로, 특정한 연산들이 정의된 집합입니다. 벡터 공간을 정의하는 8가지 조건을 흔히 선형대수학의 8공리라고 합니다. 이 공리들은 벡터 공간의 원소(즉, 벡터)들이 어떻게 더해지고 스칼라와 어떻게 곱해지는지를 규정합니다. 벡터 공간 $V$가 다음과 같은 8가지 공리를 만족할 때, $V$의 원소를 벡터(Vector)라고 부릅니다:

1. Associativity of vector addition

   $$
   \forall \mathbf{u}, \mathbf{v}, \mathbf{w} \in V, \quad (\mathbf{u} + \mathbf{v}) + \mathbf{w} = \mathbf{u} + (\mathbf{v} + \mathbf{w})
   $$

2. Commutativity of vector addition

   $$
   \forall \mathbf{u}, \mathbf{v} \in V, \quad \mathbf{u} + \mathbf{v} = \mathbf{v} +\mathbf{u}
   $$

3. Identity element of addition

   $$
   \exists \mathbf{0} \in V \text{ such that } \forall \mathbf{u} \in V, \quad \mathbf{u} + \mathbf{0} = \mathbf{u}
   $$

4. Inverse elements of vector addition

   $$
   \forall \mathbf{0} \in V,\quad  \exist -\mathbf{u} \in V \text{ such that } \mathbf{u} + (-\mathbf{u}) = \mathbf{0}
   $$

5. Associativity of Scalar Multiplication

   $$
   \forall a, b \in F \text{ and } \mathbf{u} \in V, \quad a(b\mathbf{u}) = (ab)\mathbf{u}
   $$

6. Identity element of scalar multiplication

   $$
   \forall \mathbf{u} \in V, \quad 1\mathbf{u} = \mathbf{u}
   $$

7. Distributivity of scalar multiplication with respect to vector addition
   $$
   \forall a \in F \text{ and } \mathbf{u}, \mathbf{v} \in V, \quad a(\mathbf{u} + \mathbf{v}) = a\mathbf{u} + a\mathbf{v}
   $$
   
8. Distributivity of scalar multiplication with respect to vector addition

   $$
   \forall a, b \in F \text{ and } \mathbf{u} \in V, \quad (a + b)\mathbf{u} = a\mathbf{u} + b\mathbf{u}
   $$