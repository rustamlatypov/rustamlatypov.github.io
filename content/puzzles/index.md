---
title: "Puzzles"
hidemeta: true
hidetitle: true
showToc: false
disableAnchoredHeadings: true

---

A curated collection of my favorite puzzles. None of these are my own creation, but rather heard about from friends and colleagues. I want to give credit to Giovanna Kobus, Marc Fuchs, Zahra Parsaeian, and Roger Wattenhofer. My definition of a good puzzle is that it's quick to explain, its solution doesn't require any heavy machinery, and the solution can be explained in under two minutes.

---

**Three points on a circle.** Three points are randomly chosen on a circle. What is the probability that the triangle with the vertices at the three points has the center of the circle in its interior?

<details>
<summary>Show answer</summary>

Let $P_1$, $P_2$, and $P_3$ be the points of interest. Let us decompose the random process of choosing $P_1$ and $P_2$ as follows. For both points, let us randomly choose a diameter of the circle, and then flipping a fair coin to determine at which endpoint does the point end up at.

Consider that $P_3$ is drawn randomly, and for $P_1$ and $P_2$ the random diameters are drawn, but it is not yet determined at which endpoints do the points end up. Now, the only possibility for the center to be contained in the triangle is that the furthermost ends (relative to the location of $P_3$) of both diameters are chosen. This probability is $1/4$.

</details>

<br>

**Horse competition.** Given 25 horses, you want to know which are the 3 fastest. However, every competition is limited to 5 horses. After a competition, you only learn the relative performance of the horses involved, and not their absolute speed. What is the "minimum" number of competitions you need to find the 3 fastest horses? Assume that no two horses are equally fast and for sure, they have the same performance in every race.

<details>
<summary>Show answer</summary>

Divide the horses into 5 groups of 5 horses and run a competition for every group. Denote with $t_{i,j}$ the horse that belonged to group $i$ and finished in place $j$. Now run a competition with horses $t_{i,1}$ for all $i\in \{1,5\}$. Assume w.l.o.g. that horse $t_{1,1}$ finished first, $t_{2,1}$ second, $t_{3,1}$ third, etc. We know that horse $t_{1,1}$ is the absolute fastest horse among all 25 horses.

The only possible second and third fastest horses are among $t_{1,2}$, $t_{1,3}$, $t_{2,1}$, $t_{2,2}$ $t_{3,1}$, so we run a competition among them.

</details>
