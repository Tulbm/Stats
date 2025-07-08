---
{"dg-publish":true,"permalink":"/academics/math/differential-equations/solutions-to-first-order-d-es/","created":"2024-09-13T14:37:39.942-04:00","updated":"2025-07-08T11:02:52.830-04:00"}
---

[[Academics/MATH/Differential Equations/Solution to DEs\|Solution to DEs]] specifically for first order


# Direction Fields
Graphs that give us all possible solutions to a DE
![](https://i.imgur.com/vs6nprr.png)

![](https://i.imgur.com/rvHAgKz.png)
Each line is a possible solution to the DE

And the [[Academics/MATH/Differential Equations/Solution to DEs#Initial Value Problems\|initial conditios]] will decide which one we want to use

A constant solution $y=a$ is called an equilibrium solution

A equilibrium solution can be **unstable** or **asymptotically stable** depending on the behavior of the solutions next to them
- asymptotically stable = all nearby solutions approach $a$
- unstable = all nearby solutions move away from $a$


If every solution is constant, they're simply all called stable
![](https://i.imgur.com/uwYHYNK.png)


[[Academics/MATH/Differential Equations/Autonomous DEs\|Autonomous DEs]]


# Substitution
Used in DEs like:
$$
y'=\frac{5x+6y}{2x-9y}
$$
- rational and every term has a in/dependent variable

Substituting $y(x)=v(x)x$
$\frac{dy}{dx}=v'x+v$
Then
$$
v'x+v = DE \text{ with what we set for v on}
$$
We then isolate $v'$ and can [[Academics/MATH/Differential Equations/Direct Integration\|integrate]] to find the value of v

Then convert back to terms of y


