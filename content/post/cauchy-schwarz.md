---
title: "Cauchy-Schwarz Inequality and Proof"
date: 2025-08-25
summary: "A concise statement and proof of the Cauchy-Schwarz inequality."
hideSummary: false
---

## Example Table

| Column 1 | Column 2 | 
|----------|----------|
| Row 1    | Data     |
| Row 2    | Data     |


## Cauchy-Schwarz Inequality

For any vectors $\mathbf{u}, \mathbf{v}$ in an inner product space,

$$
|\langle \mathbf{u}, \mathbf{v} \rangle| \leq \|\mathbf{u}\| \cdot \|\mathbf{v}\|
$$

---

## Proof

Consider, for any $\lambda \in \mathbb{R}$:
$$
\langle \mathbf{u} - \lambda \mathbf{v}, \mathbf{u} - \lambda \mathbf{v} \rangle \geq 0
$$
Expanding:
$$
\langle \mathbf{u}, \mathbf{u} \rangle - 2\lambda \langle \mathbf{u}, \mathbf{v} \rangle + \lambda^2 \langle \mathbf{v}, \mathbf{v} \rangle \geq 0
$$
This quadratic in $\lambda$ has discriminant
$$
D = [2\langle \mathbf{u}, \mathbf{v} \rangle]^2 - 4 \langle \mathbf{u}, \mathbf{u} \rangle \langle \mathbf{v}, \mathbf{v} \rangle \leq 0
$$
which implies
$$
|\langle \mathbf{u}, \mathbf{v} \rangle|^2 \leq \langle \mathbf{u}, \mathbf{u} \rangle \langle \mathbf{v}, \mathbf{v} \rangle
$$
Taking square roots yields the result.

---

## Applications
- Bounding dot products
- Proving the triangle inequality
- Estimating integrals

---

## Example
Let $\mathbf{u} = (1,2,3)$, $\mathbf{v} = (4,5,6)$.

$$
|1\cdot4 + 2\cdot5 + 3\cdot6| \leq \sqrt{1^2+2^2+3^2} \cdot \sqrt{4^2+5^2+6^2}
$$