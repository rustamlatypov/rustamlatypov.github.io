---
title: "Horse competition"
hidemeta: true
summary: Given 25 horses, you want to know which are the 3 fastest. However, every competition is limited to 5 horses. After a competition, you only learn the relative performance of the horses involved, and not their absolute speed. What is the "minimum" number of competitions you need to find the 3 fastest horses? Assume that no two horses are equally fast and for sure, they have the same performance in every race.

---
##### Problem

Given 25 horses, you want to know which are the 3 fastest. However, every competition is limited to 5 horses. After a competition, you only learn the relative performance of the horses involved, and not their absolute speed. What is the "minimum" number of competitions you need to find the 3 fastest horses? Assume that no two horses are equally fast and for sure, they have the same performance in every race.

##### Solution

Divide the horses into 5 groups of 5 horses and run a competition for every group. Denote with $t_{i,j}$ the horse that belonged to group $i$ and finished in place $j$. Now run a competition with horses $t_{i,1}$ for all $i\in \{1,5\}$. Assume w.l.o.g. that horse $t_{1,1}$ finished first, $t_{2,1}$ second, $t_{3,1}$ third, etc. We know that horse $t_{1,1}$ is the absolute fastest horse among all 25 horses.

The only possible second and third fastest horses are among $t_{1,2}$, $t_{1,3}$, $t_{2,1}$, $t_{2,2}$ $t_{3,1}$, so we run a competition among them.
