---
title: "Adaptive Massively Parallel Coloring in Sparse Graphs"
date: 2024-06-17
author: ["Rustam Latypov", "Yannic Maus", "Shreyas Pai", "Jara Uitto"]
summary: In this work, we study the vertex-coloring problem in sparse graphs parameterized by their arboricity $\alpha$, a standard measure for sparsity. We give deterministic algorithms that in constant, or almost constant, time give $\text{poly} \alpha$ and $O(\alpha)$-colorings, where $\alpha$ can be arbitrarily smaller than $\Delta$.
venue: PODC 24
editPost:
    URL: "https://www.podc.org/podc2024/"
    Text: "ACM Symposium on Principles of Distributed Computing (PODC 2024)"

---

##### Links

+ [Conference version](https://doi.org/10.1145/3662158.3662821)
+ [ArXiv version](https://arxiv.org/abs/2402.13755)

---

##### Abstract

Classic symmetry-breaking problems on graphs have gained a lot of attention in models of modern parallel computation. The Adaptive Massively Parallel Computation (AMPC) is a model that captures the central challenges in data center computations. Chang et al. [PODC'2019] gave an extremely fast, constant time, algorithm for the $(\Delta + 1)$-coloring problem, where $\Delta$ is the maximum degree of an input graph of $n$ nodes. The algorithm works in the most restrictive low-space setting, where each machine has $n^{\delta}$ local space for a constant $0 < \delta < 1$.

The standard approaches for $(\Delta + 1)$-coloring are ignorant about the graph topology in the following sense: They exploit the property that any partial coloring can be extended to a feasible $(\Delta + 1)$-coloring of the whole graph. For most graphs, the chromatic number is much smaller than $\Delta + 1$ and we would like to find colorings with fewer colors. However, as soon as we have fewer than $\Delta + 1$ colors, it might not be possible to complete partial colorings.

In this work, we study the vertex-coloring problem in sparse graphs parameterized by their arboricity $\alpha$, a standard measure for sparsity. We give deterministic algorithms that in constant, or almost constant, time give $\text{poly} \alpha$ and $O(\alpha)$-colorings, where $\alpha$ can be arbitrarily smaller than $\Delta$. A strong and standard approach to compute arboricity-dependent colorings is through the Nash-Williams forest decomposition, which gives rise to an (acyclic) orientation of the edges such that each node has a small out-degree.

Our main technical contribution is giving efficient deterministic algorithms to compute these orientations and showing how to leverage them to find colorings in low-space AMPC. A key technical challenge is that the color of a node may depend on almost all of the other nodes in the graph and these dependencies cannot be stored on a single machine. Nevertheless, our novel and careful exploration technique yields the orientation, and the arboricity-dependent coloring, with a sublinear number of adaptive queries per node.

---

##### Citation

```latex
@InProceedings{10.1145/3662158.3662821,
  author = {Latypov, Rustam and Maus, Yannic and Pai, Shreyas and Uitto, Jara},
  title = {{Adaptive Massively Parallel Coloring in Sparse Graphs}},
  year = {2024},
  isbn = {9798400706684},
  publisher = {Association for Computing Machinery},
  address = {New York, NY, USA},
  url = {https://doi.org/10.1145/3662158.3662821},
  doi = {10.1145/3662158.3662821},
  booktitle = {Proceedings of the 43rd ACM Symposium on Principles of Distributed Computing},
  pages = {508–518},
  numpages = {11},
  keywords = {graph coloring, adaptive massively parallel computation},
  location = {Nantes, France},
  series = {PODC '24}
}
```
