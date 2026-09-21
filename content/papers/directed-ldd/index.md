---
title: "Near-Optimal Directed Low-Diameter Decompositions"
date: 2025-06-30
author: ["Karl Bringmann", "Nick Fischer", "Bernhard Haeupler", "Rustam Latypov"]
summary: In this work, we make further advancements in the study of directed LDDs. We reveal a natural and intuitive (in hindsight) connection to Expander Decompositions, and leveraging this connection along with additional techniques, we establish the existence of an LDD with an edge-cutting probability of $O(\frac{1}{D} \cdot \log n \log\log n)$.
venue: ICALP 25
editPost:
    URL: "https://conferences.au.dk/icalp2025"
    Text: "International Colloquium on Automata, Languages, and Programming (ICALP 2025)"

---

##### Links

+ [Conference version](https://doi.org/10.4230/LIPIcs.ICALP.2025.35)
+ [ArXiv version](https://arxiv.org/abs/2502.05687)

---

##### Abstract

Low Diameter Decompositions (LDDs) are invaluable tools in the design of combinatorial graph algorithms. While  historically they have been applied mainly to undirected graphs, in the recent breakthrough for the negative-length Single Source Shortest Path problem, Bernstein, Nanongkai, and Wulff-Nilsen [FOCS '22] extended the use of LDDs to directed graphs for the first time. Specifically, their LDD deletes each edge with probability at most $O(\frac{1}{D} \cdot \log^2 n)$, while ensuring that each strongly connected component in the remaining graph has a (weak) diameter of at most $D$.

In this work, we make further advancements in the study of directed LDDs. We reveal a natural and intuitive (in hindsight) connection to Expander Decompositions, and leveraging this connection along with additional techniques, we establish the existence of an LDD with an edge-cutting probability of $O(\frac{1}{D} \cdot \log n \log\log n)$. This improves the previous bound by nearly a logarithmic factor and closely approaches the lower bound of $\Omega(\frac{1}{D} \cdot \log n)$. With significantly more technical effort, we also develop two efficient algorithms for computing our LDDs: a deterministic algorithm that runs in time $\widetilde{O}(m \cdot \text{poly}(D))$ and a randomized algorithm that runs in near-linear time $\widetilde{O}(m)$.

We believe that our work provides a solid conceptual and technical foundation for future research relying on directed LDDs, which will undoubtedly follow soon.

---

##### Citation

```latex
@InProceedings{bringmann_et_al:LIPIcs.ICALP.2025.35,
  author = {Bringmann, Karl and Fischer, Nick and Haeupler, Bernhard and Latypov, Rustam},
  title = {{Near-Optimal Directed Low-Diameter Decompositions}},
  booktitle = {52nd International Colloquium on Automata, Languages, and Programming (ICALP 2025)},
  pages =	{35:1--35:18},
  series = {Leibniz International Proceedings in Informatics (LIPIcs)},
  ISBN = {978-3-95977-372-0},
  ISSN = {1868-8969},
  year = {2025},
  volume = {334},
  editor = {Censor-Hillel, Keren and Grandoni, Fabrizio and Ouaknine, Jo\"{e}l and Puppis, Gabriele},
  publisher = {Schloss Dagstuhl -- Leibniz-Zentrum f{\"u}r Informatik},
  address = {Dagstuhl, Germany},
  URL = {https://drops.dagstuhl.de/entities/document/10.4230/LIPIcs.ICALP.2025.35},
  URN = {urn:nbn:de:0030-drops-234125},
  doi = {10.4230/LIPIcs.ICALP.2025.35},
  annote = {Keywords: Low Diameter Decompositions, Expander Decompositions, Directed Graphs}
}
```
