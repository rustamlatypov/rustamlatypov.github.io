---
title: "Optimal Deterministic Massively Parallel Connectivity on Forests"
date: 2023-01-22
author: ["Alkida Balliu", "Rustam Latypov", "Yannic Maus", "Dennis Olivetti", "Jara Uitto"]
summary: We give an algorithm that identifies connected components in $O(\log D)$ deterministic rounds. The total memory required is $O(n+m)$ words, where $m$ is the number of edges in the input graph, which is optimal as it is only enough to store the input graph. We complement our upper bound results by showing that $\Omega(\log D)$ time is necessary even for component-unstable algorithms, conditioned on the widely believed 1 vs. 2 cycles conjecture.
venue: SODA 23
editPost:
    URL: "https://epubs.siam.org/doi/book/10.1137/1.9781611977554"
    Text: "ACM-SIAM Symposium on Discrete Algorithms (SODA 2023)"

---

##### Links

+ [Conference version](https://doi.org/10.1137/1.9781611977554.ch99)
+ [ArXiv version](https://arxiv.org/abs/2211.03530)
+ [Video](https://dl.acm.org/doi/suppl/10.1145/3558481.3591103/suppl_file/SPAA23-fp234.mp4)

---

##### Abstract

We show fast deterministic algorithms for fundamental problems on forests in the challenging low-space regime of the well-known Massive Parallel Computation (MPC) model. A recent breakthrough result by Coy and Czumaj [STOC'22] shows that, in this setting, it is possible to deterministically identify connected components on graphs in $O(\log D + \log\log n)$ rounds, where $D$ is the diameter of the graph and $n$ the number of nodes. The authors left open a major question: is it possible to get rid of the additive $\log\log n$ factor and deterministically identify connected components in a runtime that is completely independent of $n$?

We answer the above question in the affirmative in the case of forests. We give an algorithm that identifies connected components in $O(\log D)$ deterministic rounds. The total memory required is $O(n+m)$ words, where $m$ is the number of edges in the input graph, which is optimal as it is only enough to store the input graph. We complement our upper bound results by showing that $\Omega(\log D)$ time is necessary even for component-unstable algorithms, conditioned on the widely believed 1 vs. 2 cycles conjecture. Our techniques also yield a deterministic forest-rooting algorithm with the same runtime and memory bounds.

Furthermore, we consider Locally Checkable Labeling  problems (LCLs), whose solution can be verified by checking the $O(1)$-radius neighborhood of each node. We show that any LCL problem on forests can be solved in $O(\log D)$ rounds with a canonical deterministic algorithm, improving over the $O(\log n)$ runtime of Brandt, Latypov and Uitto [DISC'21]. We also show that there is no algorithm that solves all LCL problems on trees asymptotically faster.

---

##### Citation

```latex
@inproceedings{balliu2023optimal,
  author =	{Balliu, Alkida and Latypov, Rustam and Maus, Yannic and Olivetti, Dennis and Uitto, Jara},
  title =	{{Optimal Deterministic Massively Parallel Connectivity on Forests}},
  booktitle =	{Proceedings of the 2023 Annual ACM-SIAM Symposium on Discrete Algorithms (SODA)},
  pages =	{2589--2631},
  publisher =	{Society for Industrial and Applied Mathematics},
  year =	{2023},
  doi =		{10.1137/1.9781611977554.ch99},
  url =		{https://doi.org/10.1137/1.9781611977554.ch99},
  eprint =	{2211.03530},
  archivePrefix = {arXiv}
}
```
