---
title: "Three points on a circle"
hidemeta: true
summary: Three points are randomly chosen on a circle. What is the probability that the triangle with the vertices at the three points has the center of the circle in its interior?

---
##### Problem

Three points are randomly chosen on a circle. What is the probability that the triangle with the vertices at the three points has the center of the circle in its interior?

##### Solution

Let $P_1$, $P_2$, and $P_3$ be the points of interest. Let us decompose the random process of choosing $P_1$ and $P_2$ as follows. For both points, let us randomly choose a diameter of the circle, and then flipping a fair coin to determine at which endpoint does the point end up at.

Consider that $P_3$ is drawn randomly, and for $P_1$ and $P_2$ the random diameters are drawn, but it is not yet determined at which endpoints do the points end up. Now, the only possibility for the center to be contained in the triangle is that the furthermost ends (relative to the location of $P_3$) of both diameters are chosen. This probability is $1/4$.
