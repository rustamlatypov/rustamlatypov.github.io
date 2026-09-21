---
title: "Fast Dynamic Programming in Trees in the MPC Model"
date: 2023-06-17
author: ["Chetan Gupta", "Rustam Latypov", "Yannic Maus", "Shreyas Pai", "Simo Särkkä", "Jan Studený", "Jukka Suomela", "Jara Uitto", "Hossein Vahidi"]
summary: We present a deterministic algorithm for solving a wide range of dynamic programming problems in trees in $O(\log D)$ rounds in the massively parallel computation model (MPC), with $O(n^\delta)$ words of local memory per machine, for any given constant $0 < \delta < 1$. Our algorithm can solve many classical graph optimization problems such as maximum weight independent set, maximum weight matching, minimum weight dominating set, and minimum weight vertex cover.
venue: SPAA 23
editPost:
    URL: "https://spaa.acm.org/spaa-2023/"
    Text: "ACM Symposium on Parallelism in Algorithms and Architectures (SPAA 2023)"

---

##### Links

+ [Conference version](https://doi.org/10.1145/3558481.3591098)
+ [ArXiv version](https://arxiv.org/abs/2305.03693)

---

##### Abstract

We present a deterministic algorithm for solving a wide range of dynamic programming problems in trees in $O(\log D)$ rounds in the massively parallel computation model (MPC), with $O(n^\delta)$ words of local memory per machine, for any given constant $0 < \delta < 1$. Here $D$ is the diameter of the tree and $n$ is the number of nodes---we emphasize that our running time is independent of $n$.

Our algorithm can solve many classical graph optimization problems such as maximum weight independent set, maximum weight matching, minimum weight dominating set, and minimum weight vertex cover. It can also be used to solve many accumulation tasks in which some aggregate information is propagated upwards or downwards in the tree---this includes, for example, computing the sum, minimum, or maximum of the input labels in each subtree, as well as many inference tasks commonly solved with belief propagation. Our algorithm can also solve any locally checkable labeling problem (LCLs) in trees. Our algorithm works for any reasonable representation of the input tree; for example, the tree can be represented as a list of edges or as a string with nested parentheses or tags. The running time of $O(\log D)$ rounds is also known to be necessary, assuming the widely-believed $2$-cycle conjecture.

Our algorithm strictly improves on two prior algorithms:
- Bateni, Behnezhad, Derakhshan, Hajiaghayi, and Mirrokni [ICALP'18] solve problems of these flavors in $O(\log n)$ rounds, while our algorithm is much faster in low-diameter trees. Furthermore, their algorithm also uses randomness, while our algorithm is deterministic.
- Balliu, Latypov, Maus, Olivetti, and Uitto [SODA'23] solve only locally checkable labeling problems in $O(\log D)$ rounds, while our algorithm can be applied to a much broader family of problems.

---

##### Citation

```latex
@InProceedings{10.1145/3558481.3591098,
  author = {Gupta, Chetan and Latypov, Rustam and Maus, Yannic and Pai, Shreyas and S{\"a}rkk{\"a}, Simo and Studen{\'y}, Jan and Suomela, Jukka and Uitto, Jara and Vahidi, Hossein},
  title = {{Fast Dynamic Programming in Trees in the MPC Model}},
  year = {2023},
  isbn = {9781450395458},
  publisher = {Association for Computing Machinery},
  address = {New York, NY, USA},
  url = {https://doi.org/10.1145/3558481.3591098},
  doi = {10.1145/3558481.3591098},
  booktitle = {Proceedings of the 35th ACM Symposium on Parallelism in Algorithms and Architectures},
  pages = {443–453},
  numpages = {11},
  keywords = {accumulation, aggregation, dynamic programming, graphical models, lcl, locally checkable labeling, massively parallel model, mpc, statistical inference, trees},
  location = {Orlando, FL, USA},
  series = {SPAA '23}
}
```
