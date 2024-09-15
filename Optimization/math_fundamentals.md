---
title: "A primer on Optimization"
author: "Prescriptive Analytics"
date: "2024"
---

# Optimization of Functions

## 1. Single Variable Optimization

For a function $f(x)$, the goal of optimization is to find the point(s) where $f(x)$ reaches a maximum or minimum. The critical points are found by solving:

$$
f'(x) = 0
$$

### Steps:
1. **Differentiate** the function $f(x)$.
2. **Solve** $f'(x) = 0$ for $x$.
3. **Check** the second derivative $f''(x)$:
   - If $f''(x) > 0$, the critical point is a local minimum.
   - If $f''(x) < 0$, the critical point is a local maximum.

---

## 2. Optimization of Two-Variable Function with Constraints

For a function  $f(x, y)$ subject to an equality constraint $g(x, y) = 0$, we use **Lagrange multipliers** to find the extrema. The Lagrange function is:

$$
\mathcal{L}(x, y, \lambda) = f(x, y) - \lambda g(x, y)
$$

### Steps:
1. Form the **Lagrange function**.
2. Differentiate with respect to $x$, $y$, and $\lambda$:

$$
\frac{\partial \mathcal{L}}{\partial x} = 0, \quad \frac{\partial \mathcal{L}}{\partial y} = 0, \quad \frac{\partial \mathcal{L}}{\partial \lambda} = 0
$$

3. Solve the system of equations to find the optimal $x$, $y$, and $\lambda$.

---

## 3. Linear Programming

Linear programming (LP) is used to optimize a linear objective function subject to a set of linear equality and inequality constraints.

### General Form:

Maximize:

$$
Z = C_1 X_1 + C_2 X_2 + \cdots + C_n X_n
$$

Subject to:

$$
a_{11}X_1 + a_{12}X_2 + \cdots + a_{1n}X_n = b_1
$$

$$
a_{21}X_1 + a_{22}X_2 + \cdots + a_{2n}X_n = b_2
$$

$$
\vdots
$$

$$
a_{m1}X_1 + a_{m2}X_2 + \cdots + a_{mn}X_n = b_m
$$

Where:

- $X_1$, $X_2$, $\dots$, $X_n$ $\geq 0$
- $b_1$, $b_2$, $\dots$, $b_m$ $\geq 0$

### Steps:
1. **Define** the objective function.
2. **Set up** the constraints.
3. Use algorithms like the **Simplex Method** or **Interior Point Methods** to find the optimal values of $X_1$, $X_2$, $\dots$, $X_n$.

---

This summarizes the key techniques in single-variable, multi-variable constrained optimization, and linear programming. Most of our efforts will be geared towards translating business problems into linear programming formulation!

## Why Not Use Lagrange Multipliers for Linear Programming?

While Lagrange multipliers are useful for constrained optimization, they aren't typically used for **linear programming (LP)**. Here’s why:

### 1. Nature of Functions and Constraints

- **Lagrange Multiplier**: Designed for **nonlinear** problems with differentiable objective functions and equality constraints.

- **Linear Programming**: Involves **linear** objective functions and **inequality** constraints. LP solutions are found at the **vertices** of the feasible region, not where gradients align as in the Lagrange method.

### 2. Handling Inequality Constraints

- **Lagrange**: Primarily handles **equality constraints**. Extending to inequality constraints (via KKT conditions) is complex.
- **LP**: Methods like **Simplex** and **Interior Point** handle inequalities naturally and efficiently.

### 3. Efficiency

- **Lagrange**: Solving the system of equations derived from Lagrange multipliers can be computationally expensive for large-scale problems.
- **LP**: **Simplex** and **Interior Point Methods** are highly optimized for solving linear systems quickly, especially for large LP problems.

### 4. Vertex Solutions vs. Interior Solutions

- **Lagrange**: Finds **interior solutions** where gradients of the objective function and constraints align.
- **LP**: Optimal solutions often lie at the **vertices** of the feasible region, which are better handled by LP-specific methods like **Simplex**.

### Conclusion

Lagrange multipliers are suited for nonlinear problems, whereas linear programming methods like **Simplex** are designed to efficiently solve LP problems, especially when inequality constraints and vertex solutions are involved.