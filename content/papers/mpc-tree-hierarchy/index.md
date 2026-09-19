---
title: "Brief Announcement: Memory Efficient Massively Parallel Algorithms for LCL Problems on Trees"
date: 2021-10-04
author: ["Sebastian Brandt", "Rustam Latypov", "Jara Uitto"]
summary: We establish scalable Massively Parallel Computation (MPC) algorithms for a family of fundamental graph problems on trees. We give a general method that, for a wide range of LCL problems, turns their message passing counterparts into exponentially faster algorithms in the sublinear MPC model.
venue: DISC 21
editPost:
    URL: "https://www.disc-conference.org/wp/disc2021/"
    Text: "International Symposium on Distributed Computing (DISC 2021)"

---

##### Links

+ [Conference version](https://doi.org/10.4230/LIPIcs.DISC.2021.50)
+ [ArXiv version](https://arxiv.org/abs/2112.09479)

---

##### Abstract

We establish scalable Massively Parallel Computation (MPC) algorithms for a family of fundamental graph problems on trees. We give a general method that, for a wide range of LCL problems, turns their message passing counterparts into exponentially faster algorithms in the sublinear MPC model. In particular, we show that any LCL on trees that has a deterministic complexity of $O(n)$ in the LOCAL model can be sped up to $O(\log n)$ (high-complexity regime) in the sublinear MPC model and similarly $n^{o(1)}$ to $O(\log \log n)$ (intermediate-complexity regime). We emphasize that we work on bounded degree trees and all of our algorithms work in the sublinear MPC model, where local memory is $O(n^\delta)$ for $\delta < 1$ and global memory is $O(m)$.

For the high-complexity regime, one key ingredient is a novel \textit{pointer-chain} technique and analysis that allows us to solve any solvable LCL on trees with a sublinear MPC algorithm with complexity $O(\log n)$. For the intermediate-complexity regime, we adapt the approach by Chang and Pettie [FOCS'17], who gave a canonical algorithm for solving LCL problems on trees in the LOCAL model. For the special case of 3-coloring trees, which is a natural LCL problem, we provide a conditional $\Omega(\log \log n)$ lower bound, implying that solving LCL problems on trees with deterministic LOCAL complexity $n^{o(1)}$ requires $\Theta(\log \log n)$ deterministic time in the sublinear MPC model when using a natural family of component-stable algorithms.

---

##### Citation

```latex
@InProceedings{brandt_et_al:LIPIcs.DISC.2021.50,
  author =	{Brandt, Sebastian and Latypov, Rustam and Uitto, Jara},
  title =	{{Brief Announcement: Memory Efficient Massively Parallel Algorithms for LCL Problems on Trees}},
  booktitle =	{35th International Symposium on Distributed Computing (DISC 2021)},
  pages =	{50:1--50:4},
  series =	{Leibniz International Proceedings in Informatics (LIPIcs)},
  ISBN =	{978-3-95977-210-5},
  ISSN =	{1868-8969},
  year =	{2021},
  volume =	{209},
  editor =	{Gilbert, Seth},
  publisher =	{Schloss Dagstuhl -- Leibniz-Zentrum f{\"u}r Informatik},
  address =	{Dagstuhl, Germany},
  URL =		{https://drops.dagstuhl.de/opus/volltexte/2021/14852},
  URN =		{urn:nbn:de:0030-drops-148521},
  doi =		{10.4230/LIPIcs.DISC.2021.50}
}
```
