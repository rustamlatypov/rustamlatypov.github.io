---
title: "Adaptive Massively Parallel Connectivity in Optimal Space"
date: 2023-06-17
author: ["Rustam Latypov", "Jakub Łącki", "Yannic Maus", "Jara Uitto"]
summary: We study the problem of finding connected components in the Adaptive Massively Parallel Computation (AMPC) model. We show that when we require the total space to be linear in the size of the input graph the problem can be solved in $O(\log^* {n})$ rounds in forests (with high probability) and $2^{O(\log^*{n})}$ expected rounds in general graphs.
venue: SPAA 23
editPost:
    URL: "https://spaa.acm.org/spaa-2023/"
    Text: "ACM Symposium on Parallelism in Algorithms and Architectures (SPAA 2023)"

---

##### Links

+ [Conference version](https://doi.org/10.1145/3558481.3591103)
+ [ArXiv version](https://arxiv.org/abs/2302.04033)
+ [Video](https://doi.org/10.1145/3558481.3591103)

---

##### Abstract

We study the problem of finding connected components in the Adaptive Massively Parallel Computation (AMPC) model. We show that when we require the total space to be linear in the size of the input graph the problem can be solved in $O(\log^* {n})$ rounds in forests (with high probability) and $2^{O(\log^*{n})}$ expected rounds in general graphs. This improves upon an existing $O(\log \log_{m/n} n)$ round algorithm.

For the case when the desired number of rounds is constant we show that both problems can be solved using $\Theta(m + n \log^{(k)} n)$ total space in expectation (in each round), where $k$ is an arbitrarily large constant and $\log^{(k)}{}$ is the $k$-th iterate of the $\log_2$ function. This improves upon existing algorithms requiring $\Omega(m + n \log n)$ total space.

---

##### Citation

```latex
@inproceedings{latypov2023adaptive,
  author =	{Latypov, Rustam and Łącki, Jakub and Maus, Yannic and Uitto, Jara},
  title =	{{Adaptive Massively Parallel Connectivity in Optimal Space}},
  booktitle =	{Proceedings of the 35th ACM Symposium on Parallelism in Algorithms and Architectures (SPAA)},
  publisher =	{Association for Computing Machinery},
  address =	{New York, NY, USA},
  year =	{2023},
  doi =		{10.1145/3558481.3591103},
  url =		{https://doi.org/10.1145/3558481.3591103},
  eprint =	{2302.04033},
  archivePrefix = {arXiv}
}
```
