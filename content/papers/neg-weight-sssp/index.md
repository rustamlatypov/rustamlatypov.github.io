---
title: "A Simple Parallel Algorithm with Near-Linear Work for Negative-Weight Single-Source Shortest Path"
date: 2025-01-15
author: ["Nick Fischer", "Bernhard Haeupler", "Rustam Latypov", "Antti Roeyskoe", "Aurelio Sulser"]
summary: We give the first parallel algorithm with optimal $\tilde{O}(m)$ work for the classical problem of computing Single-Source Shortest Paths in general graphs with negative-weight edges.
venue: SOSA 25
editPost:
    URL: "https://epubs.siam.org/doi/10.1137/1.9781611978315"
    Text: "SIAM Symposium on Simplicity in Algorithms (SOSA 2025)"

---

##### Links

+ [Conference version](https://doi.org/10.1137/1.9781611978315.17)
+ [ArXiv version](https://arxiv.org/abs/2410.20959)

---

##### Abstract

We give the first parallel algorithm with optimal $\tilde{O}(m)$ work for the classical problem of computing Single-Source Shortest Paths in general graphs with negative-weight edges.

In graphs without negative edges, Dijkstra's algorithm solves the Single-Source Shortest Paths (SSSP) problem with optimal $\tilde O(m)$ work, but is inherently sequential. A recent breakthrough by [Bernstein, Nanongkai, Wulff-Nilsen; FOCS '22] achieves the same for general graphs. Parallel shortest path algorithms are more difficult and have been intensely studied for decades. Only very recently, multiple lines of research culminated in parallel algorithms with optimal work $\tilde O(m)$ for various restricted settings, such as approximate or exact algorithms for directed or undirected graphs without negative edges. For general graphs, the best known algorithm by [Ashvinkumar, Bernstein, Cao, Grunau, Haeupler, Jiang, Nanongkai, Su; ESA '24] still requires $m^{1+o(1)}$ work.

This paper presents a randomized parallel algorithm for SSSP in general graphs with near-linear work $\tilde O(m)$ and state-of-the-art span $n^{1/2 + o(1)}$. We follow a novel bottom-up approach leading to a particularly clean and simple algorithm. Our algorithm can be seen as a near-optimal parallel black-box reduction from SSSP in general graphs to graphs without negative edges. In contrast to prior works, the reduction in this paper is both parallel and essentially without overhead, only affecting work and span by polylogarithmic factors.

---

##### Citation

```latex
@InProceedings{doi:10.1137/1.9781611978315.17,
  author = {Nick Fischer and Bernhard Haeupler and Rustam Latypov and Antti Roeyskoe and Aurelio L. Sulser},
  title = {{A Simple Parallel Algorithm with Near-Linear Work for Negative-Weight Single-Source Shortest Path}},
  booktitle = {2025 Symposium on Simplicity in Algorithms (SOSA)},
  pages = {216-225},
  doi = {10.1137/1.9781611978315.17},
  URL = {https://epubs.siam.org/doi/abs/10.1137/1.9781611978315.17},
  eprint = {https://epubs.siam.org/doi/pdf/10.1137/1.9781611978315.17}
}

```
