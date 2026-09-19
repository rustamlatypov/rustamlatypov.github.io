---
title: "Conditionally Optimal Parallel Coloring of Forests"
date: 2023-10-10
author: ["Christoph Grunau", "Rustam Latypov", "Yannic Maus", "Shreyas Pai", "Jara Uitto"]
summary: We show the first conditionally optimal deterministic algorithm for $3$-coloring forests in the low-space massively parallel computation (MPC) model. Our algorithm runs in $O(\log \log n)$ rounds and uses optimal global space.
venue: DISC 23
editPost:
    URL: "https://www.disc-conference.org/wp/disc2023/"
    Text: "International Symposium on Distributed Computing (DISC 2023)"

---

##### Links

+ [Conference version](https://doi.org/10.4230/LIPIcs.DISC.2023.23)
+ [ArXiv version](https://arxiv.org/abs/2308.00355)

---

##### Abstract

We show the first conditionally optimal deterministic algorithm for $3$-coloring forests in the low-space massively parallel computation (MPC) model. Our algorithm runs in $O(\log \log n)$ rounds and uses optimal global space. The best previous algorithm requires $4$ colors [Ghaffari, Grunau, Jin, DISC'20] and is randomized, while  our algorithm are inherently deterministic.

Our main technical contribution is an $O(\log\log n)$-round algorithm to compute a partition of the forest into  $O(\log n)$ ordered layers such that every node has at most two neighbors in the same or higher layers. Similar decompositions are often used in the area and we believe that this result is of independent interest. Our results also immediately yield conditionally optimal deterministic algorithms for maximal independent set and maximal matching for forests, matching the state of the art [Giliberti, Fischer, Grunau, SPAA'23]. In contrast to their solution, our algorithms are not based on derandomization, and are arguably simpler.

---

##### Citation

```latex
@InProceedings{grunau_et_al:LIPIcs.DISC.2023.23,
  author =	{Grunau, Christoph and Latypov, Rustam and Maus, Yannic and Pai, Shreyas and Uitto, Jara},
  title =	{{Conditionally Optimal Parallel Coloring of Forests}},
  booktitle =	{37th International Symposium on Distributed Computing (DISC 2023)},
  pages =	{23:1--23:20},
  series =	{Leibniz International Proceedings in Informatics (LIPIcs)},
  ISBN =	{978-3-95977-301-0},
  ISSN =	{1868-8969},
  year =	{2023},
  volume =	{281},
  editor =	{Oshman, Rotem},
  publisher =	{Schloss Dagstuhl -- Leibniz-Zentrum f{\"u}r Informatik},
  address =	{Dagstuhl, Germany},
  URL =		{https://drops.dagstuhl.de/entities/document/10.4230/LIPIcs.DISC.2023.23},
  URN =		{urn:nbn:de:0030-drops-191494},
  doi =		{10.4230/LIPIcs.DISC.2023.23},
  annote =	{Keywords: massively parallel computation, coloring, forests, optimal}
}
```
