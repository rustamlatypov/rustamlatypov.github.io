---
title: "Exponential Speedup over Locality in MPC with Optimal Memory"
date: 2022-10-25
author: ["Alkida Balliu", "Sebastian Brandt", "Manuela Fischer", "Rustam Latypov", "Yannic Maus", "Dennis Olivetti", "Jara Uitto"]
summary: In this work, we initiate the study of LCL problems in the low-space Massively Parallel Computation (MPC) model. In particular, on forests, we provide a method that, given the complexity of an LCL problem in the LOCAL model, automatically provides an exponentially faster algorithm for the low-space MPC setting that uses optimal global memory, that is, truly linear.
venue: DISC 22
editPost:
    URL: "https://www.disc-conference.org/wp/disc2022/"
    Text: "International Symposium on Distributed Computing (DISC 2022)"

---

##### Links

+ [Conference version](https://doi.org/10.4230/LIPIcs.DISC.2022.9)
+ [Journal version](https://doi.org/10.1007/s00446-025-00477-9)
+ [ArXiv version](https://arxiv.org/abs/2208.09453)

Invited to the Special Issue of DISC 2022.

---

##### Abstract

Locally Checkable Labeling (LCL) problems are graph problems in which a solution is correct if it satisfies some given constraints in the local neighborhood of each node. Example problems in this class include maximal matching, maximal independent set, and coloring problems. A successful line of research has been studying the complexities of LCL problems on paths/cycles, trees, and general graphs, providing many interesting results for the LOCAL model of distributed computing. In this work, we initiate the study of LCL problems in the low-space Massively Parallel Computation (MPC) model. In particular, on forests, we provide a method that, given the complexity of an LCL problem in the LOCAL model, automatically provides an exponentially faster algorithm for the low-space MPC setting that uses optimal global memory, that is, truly linear.

While restricting to forests may seem to weaken the result, we emphasize that all known (conditional) lower bounds for the MPC setting are obtained by lifting lower bounds obtained in the distributed setting in tree-like networks (either forests or high girth graphs), and hence the problems that we study are challenging already on forests. Moreover, the most important technical feature of our algorithms is that they use optimal global memory, that is, memory linear in the number of edges of the graph. In contrast, most of the state-of-the-art algorithms use more than linear global memory. Further, they typically start with a dense graph, sparsify it, and then solve the problem on the residual graph, exploiting the relative increase in global memory. On forests, this is not possible, because the given graph is already as sparse as it can be, and using optimal memory requires new solutions.

---

##### Citation

```latex
@InProceedings{balliu_et_al:LIPIcs.DISC.2022.9,
  author = {Balliu, Alkida and Brandt, Sebastian and Fischer, Manuela and Latypov, Rustam and Maus, Yannic and Olivetti, Dennis and Uitto, Jara},
  title = {{Exponential Speedup over Locality in MPC with Optimal Memory}},
  booktitle = {36th International Symposium on Distributed Computing (DISC 2022)},
  pages = {9:1--9:21},
  series = {Leibniz International Proceedings in Informatics (LIPIcs)},
  ISBN = {978-3-95977-255-6},
  ISSN = {1868-8969},
  year = {2022},
  volume = {246},
  editor = {Scheideler, Christian},
  publisher = {Schloss Dagstuhl -- Leibniz-Zentrum f{\"u}r Informatik},
  address = {Dagstuhl, Germany},
  URL = {https://drops.dagstuhl.de/entities/document/10.4230/LIPIcs.DISC.2022.9},
  URN = {urn:nbn:de:0030-drops-172003},
  doi = {10.4230/LIPIcs.DISC.2022.9},
  annote = {Keywords: Distributed computing, Locally checkable labeling problems, Trees, Massively Parallel Computation, Sublinear memory}
}
```
