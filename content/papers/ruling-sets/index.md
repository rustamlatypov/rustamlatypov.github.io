---
title: "Near-Optimal Distributed 2-Ruling Sets on Graphs with Low Arboricity"
date: 2026-09-09
author: ["Malte Baumecker", "Rustam Latypov", "Yannic Maus", "Jara Uitto"]
summary: We present almost optimal distributed algorithms for finding $2$-ruling sets in the classical LOCAL model. Our main contribution is a randomized algorithm that w.h.p. computes a $2$-ruling set on any $n$-node graph with bounded arboricity in $O(\log \log n)$ rounds.
venue: DISC 26
editPost:
    URL: "https://www.disc-conference.org/wp/disc2026/"
    Text: "International Symposium on Distributed Computing (DISC 2026)"

---

##### Links

+ [Conference version](https://doi.org/10.4230/LIPIcs.DISC.2026.15)
+ [ArXiv version](https://arxiv.org/abs/2606.11974)

---

##### Abstract

Given a graph $G=(V,E)$, a $\beta$-ruling set is a subset of nodes $S\subseteq V$ that is independent, and each node in $V$ is at distance at most $\beta$ from some node in $S$. In this paper, we present almost optimal distributed algorithms for finding $2$-ruling sets in the classical LOCAL model. Our main contribution is a randomized algorithm that w.h.p. computes a $2$-ruling set on any $n$-node graph with bounded arboricity in $O(\log \log n)$ rounds. In fact, the algorithm works up to arboricity $O(\log\log n)$, improves exponentially over the prior state of the art that can be achieved by combining [Barenboim, Elkin, Pettie, Schneider; JACM'16], [Ghaffari; SODA'16], and [Bisht, Kothapalli and Pemmaraju; PODC'14], and nearly matches the lower bound of $\Omega(\log \log n / \log \log \log n)$ [Balliu, Brandt, Kuhn, Olivetti; FOCS'20]. The domination parameter $\beta=2$ is optimal for algorithms with runtime $\log^{o(1)}n$:  on graphs with arboricity $2$, there is a lower bound of $\Omega(\sqrt{\log n})$ rounds for MIS (i.e., $\beta = 1$) [Khoury, Schild; FOCS'25].

Additionally, we obtain improved algorithms for larger arboricity. For general graphs with arboricity $\alpha$, we present a randomized algorithm that computes a $2$-ruling set in $\widetilde{O}(\log^{5/8} \alpha +\log^{5/3} \log n)$ rounds. This improves exponentially over the state of the art for a large range of non-constant arboricity.

Our techniques extend beyond distributed computing. We present an $O(\log \log \log n)$-round algorithm in the low-space Massively Parallel Computation (MPC) model that w.h.p. computes a $2$-ruling set on any graph with arboricity up to $2^{\text{poly}(\log \log n)}$, improving exponentially over the state of the art from [Kothapalli, Pai, Pemmaraju; FSTTCS'20] combined with [Fischer, Giliberti, Grunau; SPAA'23].

---

##### Citation

```latex
@InProceedings{baumecker_et_al:LIPIcs.DISC.2026.15,
  author =	{Baumecker, Malte and Latypov, Rustam and Maus, Yannic and Uitto, Jara},
  title =	{{Near-Optimal Distributed 2-Ruling Sets on Graphs with Low Arboricity}},
  booktitle =	{40th International Symposium on Distributed Computing (DISC 2026)},
  pages =	{15:1--15:25},
  series =	{Leibniz International Proceedings in Informatics (LIPIcs)},
  ISBN =	{978-3-95977-454-3},
  ISSN =	{1868-8969},
  year =	{2026},
  volume =	{397},
  editor =	{Moses Jr., William K. and Censor-Hillel, Keren},
  publisher =	{Schloss Dagstuhl -- Leibniz-Zentrum f{\"u}r Informatik},
  address =	{Dagstuhl, Germany},
  URL =		{https://drops.dagstuhl.de/entities/document/10.4230/LIPIcs.DISC.2026.15},
  URN =		{urn:nbn:de:0030-drops-281213},
  doi =		{10.4230/LIPIcs.DISC.2026.15},
  annote =	{Keywords: 2-ruling set, LOCAL model, CONGEST model, MPC model}
}
```
