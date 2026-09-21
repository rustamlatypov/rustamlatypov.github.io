---
title: "Puzzles"
hidemeta: true
hidetitle: true
showToc: false
disableAnchoredHeadings: true

---

A curated collection of my favorite puzzles. None of these are of my own creation. I've heard about them through friends and colleagues, and want to give credit to Giovanna Kobus, Marc Fuchs, Zahra Parsaeian, and Roger Wattenhofer, to name a few.

My definition of a good puzzle is that the problem and its solution can be stated in under two minutes, without any heavy machinery.

---


**Edge-coloring.** Show that edge-coloring complete graphs on $n$ nodes ($n$ odd) requires $n$ colors.

<details>
<summary>Show answer</summary>
<div style="height: 0.5em"></div>

Consider a complete graph with $n$ nodes and consequently $n(n-1)/2$ edges. Observe that we can only color $(n-1)/2$ edges with a single color, since each time we color an edge, we prevent exactly two nodes from having an incident edge with that same color. Since the total number of edges is $n(n-1)/2$, we require at least $n$ colors, proving the claim.

</details>

<br>

**8-cycles.** Show that any graph with no 4-cycles contains at most $n^4$ 8-cycles.

<details>
<summary>Show answer</summary>

Label all nodes with unique labels from $\{1,2,\dots,n\}$. Consider an 8-cycle, and a list of labels of its every second node. We claim that such a list corresponds to exactly one unique 8-cycle. Otherwise, there exists two distinct 8-cycles that share every second node, but differ at at least one node, implying the existence of a 4-cycle. Since the number of such lists is bounded by $n^4$, the claim follows.

</details>

<br>

**Odd degree nodes.** Show that in any graph, there is an even number of odd degree vertices.

<details>
<summary>Show answer</summary>

The degree sum over all vertices is even by the handshaking lemma. The degree sum over all even degree vertices is also even. Due to parity, the number of odd degree vertices must be even.

</details>

<br>

**Egg problem.** Consider a $n$ story building and an egg that breaks only if you drop it from a story higher than $k$. Using two eggs, find $k$ in $O(\sqrt{n})$ trials.

<details>
<summary>Show answer</summary>

A linear algorithm would be trying every story in increasing order starting from story 1. We can reduce it to $\sqrt{n}$ time by trying stories $\sqrt{n},2\sqrt{n},\dots,n$ until the egg breaks at some $i\sqrt{n}$, and then apply the linear algorithm for stories $[(i-1)\sqrt{n},\sqrt{n}]$.

</details>

<br>

**Graph burning.** Graph burning is a simple model for the spread of social influence in networks. The objective is to measure how quickly a fire (e.g., a piece of fake news) can be spread in a network. The burning process takes place in discrete rounds. In each round, a new fire breaks out at a selected vertex and burns it. Meanwhile, the old fires extend to their neighbors and burn them. Show that

1. paths can be burnt in $\lceil n^{1/2} \rceil$ rounds.
2. trees can be burnt in $2\lceil n^{1/2} \rceil$ and $\lceil (2n)^{1/2} \rceil$ rounds (separate algorithms).
3. any graph can be burnt in $2\lceil n^{1/2} \rceil$ and $\lceil (2n)^{1/2} \rceil$ rounds (separate algorithms).

<details>
<summary>Show answer</summary>

1. Let $k = \lceil n^{1/2} \rceil$. Consider the burning sequence $\{v_i \mid i = 1 + 2(k-i)\}$. After $k$ rounds, node $v_i$ will have burnt at least $1 + 2(k-i)$ nodes, which by design have not been burnt previously. The total number of burnt nodes is

    $$\sum_{i=1}^k 1 + 2(k-i) = k + \sum_{i=1}^k 2(k-i) = k + k(k-1) = k^2 = \lceil n^{1/2} \rceil^2 \geq n.$$

2. The $2 \lceil n^{1/2} \rceil$ algorithm employs a recursive approach. Let $k = \lceil n^{1/2} \rceil$. Let us first root the tree $T$. In the first round, consider a leaf with the maximum depth and its $k$:th ancestor $u$. Burn node $u$ and recurse on the remaining tree $T \setminus T_u$ (burnt nodes can be thought of as removed). Every tree $T_u$ we set aside contains at least $k$ nodes, all of which are going to burn in $k$ rounds. The number of round is hence bounded by $2k$ since the tree contains at most $k^2$ nodes and we have to wait for the last $T_u$ tree to burn.

    The $\lceil (2n)^{1/2} \rceil$ algorithm is surprisingly simple. Consider the Euler tour representation of the tree, which consists of a sequence of length $2n$, where every node appears twice. Define the burning sequence as if we were applying the path burning algorithm to the Euler tour representation. By using this burning sequence on the actual tree, we get a running time of at most $\lceil (2n)^{1/2} \rceil$. Note that if the node we want to burn in some round is already burnt, we can skip one round.

3. Follows directly from 2 by burning the spanning tree of the graph.

</details>

<br>

**Two numbers.** Consider a game show where an adversary has chosen two distinct numbers $a,b$ from between $0$ and $100$ (inclusive). You can ask him to reveal the value of one number after which, the aim is to choose the largest of the two numbers. You can either choose the number you have been revealed, or gamble on the other number being larger and choose it. Devise a strategy such that the probability of succeeding is $> 1/2$.

<details>
<summary>Show answer</summary>

Pick the revealed number $x$ at random, and chose the revealed number with probability $x/100$. Let $p_1=a/100$ and $p_2=b/100$. The probability of choosing $a$ is

$$p_1/2 + 1/2(1-p_2) = 1/2 + 1/2 (p_1-p_2)$$

and similarly $b$ is

$$p_2/2 + 1/2(1-p_1) = 1/2 + 1/2 (p_2-p_1).$$

</details>

<br>

**Point cover.** And adversary chooses 10 points from an infinite two dimensional plane. Show that you can cover all 10 points with non-overlapping unit disks.

<details>
<summary>Show answer</summary>

A tiling of the plain with non-intersecting unit disks covers $\pi/2\sqrt{3} = 0.9069 > 0.9$ of the plain (one unit disk covers $\pi/2\sqrt{3}$ of a hexagon). If we place a tiling on the plain at random, every point is covered with probability $> 0.9$. In expectation, we cover $> 9$ points, and hence there exists a placement that covers 10 points.

</details>

<br>

**Complementation.** Given any graph $G=(V,E)$, devise an $O(n^4)$ algorithm for finding the number of unique trees attainable by applying complementation. Complementing a node $v \in V$ is defined as replacing all edges $\{v,u\}\in E$ with $\{v,u\} \not\in E$ for all $u\in V$.

<details>
<summary>Show answer</summary>

Pick two arbitrary nodes $v,u \in V$. We want to check whether or not there exists a attainable unique tree such that $v$ is a leaf and $u$ is its unique neighbor. For nodes $v,u$, define operation $\mathcal{A}$ as complementing all nodes $w \in V \setminus u$ such that $\{v,w\} \in E$. If $\{v,u\} \in E$: (1) perform $\mathcal{A}$ and check if the graph is a unique tree; (2) complement $v$ and $u$, perform $\mathcal{A}$, and check. If $\{v,u\} \not\in E$: (3) complement $v$, perform $\mathcal{A}$, and check; (4) complement $u$, perform $\mathcal{A}$, and check.

Performing each case takes $O(n)$, and checking whether or not a graph is a tree takes $O(n^2)$. Since there are $O(n^2)$ pairs of vertices $v,u$, this scheme yields a runtime of $O(n^4)$.

</details>

<br>

**Chessboard cover.** Consider a classic $8 \times 8$ chessboard. Block the diagonally opposite corner squares. Is it possible to cover the remaining board using dominos? A domino covers two adjacent squares (not diagonally). Can also be formulated for an $n \times n$ board, regardless whether $n$ is even or odd. A formulation using graph theory is also possible. Consider a $n \times n$ grid with missing diagonally opposite corner nodes. Does there exist a perfect matching?

<details>
<summary>Show answer</summary>

No. The blocked squares are of the same color. Hence, w.l.o.g. there are 30 white squares and 32 black squares. Since a domino always covers one white and one black square, the board cannot be covered. The above logic works for an even $n$. For an odd $n$, there are an odd number of squares to cover, which clearly does not work. For a grid, just consider a two coloring and then use the same logic.

</details>

<br>

**Weighing balls.** There are twelve balls, eleven weigh exactly the same amount, but one of them is slightly lighter or heavier, you must figure out which. You can use a see-saw three times. Easier version is with nine balls, one being heavier, and using the see-saw only two times.

<details>
<summary>Show answer</summary>

Enumerate the balls from 1 to 12, and split them into 3 groups of four: group 1 is $1,2,3,4$, group 2 is $5,6,7,8$ and group 3 is $9,10,11,12$. Weigh group 1 and group 2. There are two distinct cases.

- $=$: The ball we are looking for is in group 3. Weigh 9 and 10.
    - $=$: The answer is either 11 or 12. Weigh 9 and 11. If equal, the answer is 12. Otherwise, the answer is 11.
    - $>$: Weigh 9 and 11. If equal, the answer is 10. Otherwise, the answer is 9.
- $>$: Define group 4 as $1,2,5$ and group 5 as $3,4,6$. Weigh group 4 and group 5.
    - $=$: The answer is either 7 or 8. Weigh 1 and 7. If equal, the answer is 8. Otherwise, the answer is 7.
    - $>$: This means that the ball we are looking for has not switched sides compared to the initial weighing. On the left we have $1,2$ and on the right 6. Weigh 1 and 2. If equal, the answer is 6. Otherwise, we know it is the heavier of the two balls (1 or 2).
    - $<$: The same logic as above, except we know that the ball we are looking has switched sides. On the left we have 5 and on the right $3,4$. Weigh 3 and 4. If equal, the answer is 5. Otherwise, we know it is the heavier of the two balls (3 or 4).

The answer to the easier version is to split into 3 groups of three. By weighing any two groups, we know which group has the the ball we are looking for. After which we weigh any two balls in said group, giving us the answer.

</details>

<br>

**Poisonous wine bottle.** Consider having 1000 wine bottles, out of which one is poisonous. You have to determine which bottle is poisonous. In order to do so, you are allowed to create 10 different drinks (each drink can be a unique mix of the bottles) and give them to 10 prisoners. The prisoners drink them simultaneously, and if their drink contains poison, they die.

<details>
<summary>Show answer</summary>

This is a classic encoding problem. Enumerate the bottles from 0 to 999 and consider their binary representation, which contains at most 10 bits. Enumerate the drinks from 1 to 10 and consider them to be a binary string of 10 bits. For every bottle, do the following. Poor bottle number $x$ into drink $y$ if the $y$:th bit of the binary representation of $x$ is 1. The prisoners that die uniquely determine the poisonous bottle number, in binary.

</details>

<br>

**Save the princess.** A princess swims in a perfectly circular pond. There is a witch at the shore, afraid of water, that plans to catch the princess when getting out. The land speed of the witch is four times as high as the water speed of the princess. Once the princess reaches the shore without the witch in its immediate neighborhood, it can hide and escape. Can the princess reach the shore safely if it starts in the middle of the pond? The size of the pond is irrelevant.

<details>
<summary>Show answer</summary>

Yes, the princess can reach the shore! Assume that the pond has radius $r$. While the princess is strictly within radius $r/4$ of the center of the pond, she is radially faster than the witch. In other words, while staying in this small radius the princess can reach the "opposite side" of the witch. Once the princess reaches that opposite point, she will swim straight to the shore. The remaining distance is $3r/4$. The witch on the other hand has a distance of $\pi r$, for which he needs $\pi r/4$ time. Since $3 < \pi$ the princess is faster.

If you wonder how much faster than the princess the witch may be, so that the princess will still reach the shore, the answer is $< \pi + 1 \approx 4.1416$.

Another, more optimal strategy, is as follows. Assume the lake has center $(0,0)$ and radius $r$, the witch is at $(-r,0)$, the speed ratio is $k$, the princess is at $(r/k,0)$. When the witch starts moving (w.l.o.g.) counterclockwise, then the princess should head toward $(r/k,r\sqrt{1-1/k^2})$ instead of $(1,0)$. The princess will always be on the same side of the lake as the witch, so she won't reverse the direction. The princess will escape as long as $\pi+\arccos(1/k) > k \sqrt{1-1/k^2}$, which works out to approximately $k < 4.6033$.

</details>

<br>

**Four cards.** You have to win a game against an opponent. Before the game starts you are blindfolded. There are four cards placed on a square table, one card at each corner. The initial configuration of the cards is chosen by the opponent, arbitrarily and unknown to you. Your goal is to have all four cards face up. In each move you can select any subsets of the four cards, which are then flipped simultaneously by the opponent. After your move, if all four cards are face up, you win. If not, the opponent may rotate the table by an amount of his choice (90, 180, 270, or 360 degrees). What is the strategy for winning in at most 15 moves?

<details>
<summary>Show answer</summary>

As always, you should first think about a simplified version of the game. In this case the simple version has only two cards, on opposite sides of a stick; the opponent may or may not turn the stick. The solution is simple. First turn both cards, then turn one card (which does not matter), then turn both cards.

For four cards the problem is a bit more intricate. Indeed you have to distinguish four configurations:

1. FOUR: all four cards are face down.
2. OPPOSITE: two cards in opposite corners are face down, the two other cards (also in opposite corners) are face up.
3. TWO: two cards on one half of the table are face down, the two other cards on the other half are face up.
4. SINGLE: A single card is different from the three other cards.

These four states have increasing difficulty.

If the initial configuration was FOUR we are done by just flipping all cards (we call this move 'F'). If the initial configuration was OPPOSITE we get to the FOUR state by flipping two (any two) opposite cards (move 'O'). From there we again win by flipping all four cards. If the initial configuration was TWO we get to FOUR or OPPOSITE by flipping any two cards in sequence (move 'T'). Finally, if the initial configuration is SINGLE we can get to some other configuration by just flipping any single card (move 'S'). In other words, the deterministic winning strategy is: F, O, F, T, F, O, F, S, F, O, F, T, F, O, F. Independent of the initial configuration these 15 moves win, even if the opponent knows our strategy.

</details>

<br>

**99 cops.** A town has 99 cops. A cop is either honest or corrupt, the majority of the cops is honest. You need to figure out all the corrupt cops, with less than 299 questions. All cops know who is honest and who is corrupt, but only honest cops will answer truthfully. Corrupt cops may lie arbitrarily. For security reasons you can only ask one type of question: You may ask cop X whether cop Y is corrupt. This question will by answered by X with either "Y is corrupt" or "Y is honest". Harder version is using $3(n-1)/2$ questions, where $n$ is the number of cops.

<details>
<summary>Show answer</summary>

Pair the cops arbitrarily. If the number of cops is odd, the last cop is a singleton. For each pair, ask both cops about the other cop. If at least one cop calls the partner cop corrupt, discard both cops. If both cops attest the other to be honest, keep one of them, discard the other (arbitrarily). If the number of cops kept in a round is even, keep the singleton cop as well. If the number of cops is odd, discard the singleton cop. Continue as long as you have more than one cop! We will prove below that this last cop is honest. All you need to do is to ask this honest cop about all the others, and you will know all honest cops.

Why does this work? Initially we have strictly less corrupt (C) than honest (H) cops, that is C < H. Assume that the number of cops is even. After pairing, we remove all the HC pairs because at least the honest cop will say that the other cop is corrupt. So we are left with HH and CC pairs, with CC < HH. Since we keep only one cop per pair, we still have C < H. Thanks to keeping/discarding the singleton cop this is also true if we have an odd number of cops: In case the singleton is corrupt, the pairs alone will guarantee C < H. In case the singleton is honest, he will break the tie if needed. No matter what, after every round we have C < H. Also, in each round cops are discarded, so eventually we end up with one cop only; thanks to our induction C < H the remaining cop is honest. For all that we need less than 299 questions. Thanks to the recursion we discard half of the cops each round. A closer analysis with the rounding because of singletons reveals that we no more than $98+48+24+12+6+2+98 = 288$ questions.

Now for the harder version using only $3(n-1)/2$ questions. We proceed in rounds, where in every round we implement a voting scheme. In round $i$, pick a random cop $x_i$. Then repeat the following: pick a random cop and ask if $x_i$ is honest or corrupt. As soon as the majority has voted $x_i$ to be corrupt, we put aside cop $x_i$ and all cops that have voted, and move to the next round. Observe that after every round, we are left with an odd number of cops and the majority of them are honest. There are two ways this scheme ends:

1. After some round $k$, there is one cop left which is honest by induction. In total, we needed $n-1-|\text{rounds}|$ questions to identify an honest cop. To this honest cop we address the following questions for every $i$:
    - Is cop $x_i$ honest or corrupt?
    - If honest, for every cop $j$ that voted honest in round $i$, ask if $j$ is honest or corrupt. If corrupt, for every cop $j$ that voted corrupt in round $i$, ask if $j$ is honest or corrupt.

    Let $n_i$ be the number of participants in round $i$. The number of questions is at most

    $$
    \begin{aligned}
    n-1-|\text{rounds}| + \sum_i (n_i/2+1) &= n-1-|\text{rounds}| + |\text{rounds}|+ 1/2 \cdot \sum_i n_i \\
    &= (n-1) + (n-1)/2 = 3(n-1)/2.
    \end{aligned}
    $$

2. In some round $k$, after choosing $x_k$, there are $m$ cops left. After $m/2$ of them vote for honest, we stop, since this implies that $x_k$ is honest. In total, we needed $n-|\text{rounds}|-|\text{unasked cops}|$ questions to identify an honest cop. To this honest cop we address the following questions for every $i \neq k$:
    - Is cop $x_i$ honest or corrupt?
    - If honest, for every cop $j$ that voted honest in round $i$, ask if $j$ is honest or corrupt. If corrupt, for every cop $j$ that voted corrupt in round $i$, ask if $j$ is honest or corrupt.

    For $i=k$, we know that $x_k$ is honest. So for every cop $j$ that voted honest in round $i$ and the ones we did not ask anything, ask if $j$ is honest or corrupt.

    Let $n_i$ be the number of participants in round $i$. The number of questions is at most

    $$
    \begin{aligned}
    & n-|\text{rounds}|-|\text{unasked cops}| + \sum_{i \neq k} (n_i/2+1) + m/2 + |\text{unasked cops}| \\
    &= n-|\text{rounds}| + \sum_{i \neq k} (n_i/2+1) + m/2 \\
    &= n-1 + \sum_{i \neq k} (n_i/2) + m/2 \\
    &= n-1 + 1/2 \cdot (n-1-m) + m/2 \\
    &= (n-1) + (n-1)/2 - m/2 + m/2 = 3(n-1)/2.
    \end{aligned}
    $$

</details>

<br>

**Hat problem.** 100 men stand in a queue, all looking in the same direction. Each man is wearing a hat. Hence, the last man can see all hats but his own, while the first man in the queue cannot see anybody's hat. The hats have a shape of a single digit, from 0 to 9. Starting with the last man in the queue, each man says a single digit, hopefully the digit on its own hat. Show that at least 99 men can guess correctly. Note that every man hears what everyone says.

<details>
<summary>Show answer</summary>

Let $v_j$ be the digit of man number $j$. The last man (number 100) announces $r = \sum_{i=1}^{99} v_i \mod 10$, which is most probably not his own digit. However, with this information the second last man (number 99) can figure out its digit $v_{99}$ from the equality $\sum_{i=1}^{98} v_i + v_{99} \mod 10 = r$. All the other men in the queue can also deduce their number. Man number $j$ can deduce his digit $v_j$ from equality

$$\sum_{i=1}^{j-1} v_i + v_j + \sum_{i=j+1}^{99} v_i \mod 10 = r.$$

Man number $j$ can compute the first by looking at the hats in front of him, and the second sum can be computed by listening to all the digits the men behind have announced.

</details>

<br>

**The switch.** The hangman summons his 100 prisoners, announcing that they may meet to plan a strategy, but will then be put in isolated cells, with no communication. He explains that he has set up a switch room which contains a single switch, which is either on or off. It is not known to the prisoners whether the switch initially is on or off. Also, the switch is not connected to anything, but a prisoner entering the room may see whether the switch is on or off (because the switch is up or down). Every once in a while, the hangman will let one arbitrary prisoner into the switch room. The prisoner may throw the switch (on to off, or vice versa), or leave the switch unchanged. Nobody but the prisoners will ever enter the switch room. The hangman promises to let any prisoner enter the room from time to time, arbitrarily often. That is, eventually, each prisoner has been in the room at least once, twice, a thousand times, any number you want. At any time, any prisoner may declare "We have all visited the switch room at least once". If the claim is correct, all prisoners will be released. If the claim is wrong, the hangman will execute all prisoners. What's the strategy?

<details>
<summary>Show answer</summary>

Assume that the switch is initially off. One prisoner is the leader. The leader will turn the switch on whenever possible, that is, whenever the switch is off. Any other prisoner will (if possible) turn the switch off, but only the first time it encounters a switch that is on. In other words, the second time a prisoner finds the switch on, the prisoner will leave it on. After having done that 99 times, the leader can declare "We have all...". This is because each of the 99 other prisoners have turned the switch off exactly once.

If the initial position of the switch is unknown, we cannot use our simple protocol since we may miscount by one. However, we can easily fix the protocol, by overcompensating this uncertainty of one: We simply let each prisoner turn the switch off twice. Then the leader can safely declare "We have all..." after throwing the switch on $2 \times 99 = 198$ times.

</details>

<br>

**100 hats.** To be released from prison, 100 prisoners have to win a game against the hangman. The hangman gives a hat to every prisoner, the hat shows an integer number from $[0,99]$. The numbers do not have to be different, the hangman can also choose to give each prisoner a hat with the same number. Prisoners can see the numbers on the other hats, but they cannot see their own number. Before playing the game, prisoners can discuss their strategy, but once the game starts there is an absolute communication stop. Now each prisoner has to guess his number (privately). If at least one prisoner guesses his number correctly, all prisoners are released. If no prisoner guesses right, the hangman executes his job. What's the strategy?

<details>
<summary>Show answer</summary>

With only two prisoners the solution is simple, prisoner $A$ just guesses the number he saw on $B$'s hat, prisoner $B$ guesses the number not on $A$'s hat. If the hangman gave both prisoners the same number, prisoner $A$ will guess right. In the other case, prisoner $B$ guesses right.

The solution for $n$ players is more or less the natural generalization. The idea is to enumerate the prisoners, and that prisoner $k$ (for $k$ from $0$ to $n-1$) is responsible to report the correct result if the sum of all hats modulo $n$ is equal to $k$. Hence the algorithm is: prisoner $k$ reports $k$ minus the sum of the numbers on the other $n-1$ hats, modulo $n$.

Let $S$ be the sum of all hats and $S \equiv k \mod n$. Observe that $S'+x \equiv k \mod n$, where $x$ is the number of prisoner $k$. It also holds that $x \equiv k-S' \mod n$. Hence the algorithm works. Prisoner $k$ reports $k$ minus the sum of the numbers on the other $n-1$ hats, modulo $n$, which is his number $x$.

</details>

<br>

**Unbiased coin.** Given a biased coin, i.e., the probability $p$ of HEADS is unknown, how can you use it to create unbiased coin flips?

<details>
<summary>Show answer</summary>

Toss the coin twice. If the results match, start over, forgetting both results. If the results differ, use the first result, forgetting the second.

The reason this process produces a fair result is that the probability of getting heads and then tails must be the same as the probability of getting tails and then heads, as the coin is not changing its bias between flips and the two flips are independent.

</details>

<br>

**Blind man.** A blind man is handed a deck of $n$ cards with exactly $k$ cards facing up. How can he divide it into two piles, each of which having the same number of cards facing up?

<details>
<summary>Show answer</summary>

Make a pile $A$ with $k$ cards and pile $B$ with $n-k$ cards, and flip all the cards in pile $A$. Let $x$ be the number of cards facing up in pile $A$, implying that pile $B$ has $k-x$ cards facing up. After flipping the cards in pile $A$, it will contain $|A|-x=k-x$ cards facing up.

</details>

<br>

**Hidden card (easy).** In this problem, you and a partner are to come up with a scheme for communicating the value of a hidden card in a normal $52$-card deck. The game is played as follows:

- Once you and your partner have finished strategizing, your partner is sent out of the room.
- The dealer hands you five cards from the deck. You look at the cards and hand them back to the dealer, one by one, in whatever order you choose.
- The dealer lays them in a rows in the order you gave them to the dealer. The dealer puts the first card face-down and the rest face-up. Assume that the cards are symmetrical, so you can't use orientation to transmit information to your partner.
- You leave the room and your partner enters the room. Your partner looks at the cards and the order in which they lie and, from that information (and your previously-agreed-upon game plan), guesses the face-down card. If the guess is correct, you win. What scheme can you and your partner use to always win?

<details>
<summary>Show answer</summary>

First, choose a pair of cards of the same suit. This must be possible since you're handed more cards than there are suits. Next, pick the card in that pair that's 1-6 ranks higher than the other, if one considers ranks to wrap around, and let $n$ be the number of ranks that card is higher than the other card. This must be possible since there are only $13$ cards in each suit. For instance, if the two cards are the $3$ and Q of hearts, then you choose the $3$ and $n=4$ since the $3$ is four ranks higher than the Q, counting Q-K-A-2-3.

Next, hand the dealer the chosen card, followed by the other card in the pair.

Finally, compute the $n$:th lowest permutation of your remaining three cards, using whatever sort order you agree on with your partner. This must be possible since there are six possible permutations and $1\leq n \leq 6$. Hand the dealer those three cards in the order given by that permutation.

When your partner comes in the room, they can compute $n$ based on the permutation they see of the last three cards. They can determine the suit of the hidden card from the suit of the first face-up card. Finally, they can add $n$ to the first face-up card's rank to determine the rank of the hidden card.

</details>

<br>

**Hidden card generalized.** Same rules as in the previous puzzle, but using a deck of size $(m-1)!\cdot 2+m-1$ and the dealer handing you $m$ card; or even harder, using a deck of size $m!+m-1$ and the dealer handing you $m$ cards.

<details>
<summary>Show answer</summary>

Consider deck size $(m-1)! \cdot 2+m-1$. You can split the deck into $m-1$ "suits". Every suit now contains $k := (m-2)! \cdot 2+1$ cards.

Similarly to the easy hidden card game, choose a pair of cards of the same suit. Next, pick the card in that pair that's at most $(k-1)/2=(m-2)!$ ranks higher than the other, if one considers ranks to wrap around, and let $n$ be the number of ranks that card is higher than the other card. With the remaining $m-2$ cards, you can express $(m-2)!$ permutations to indicate the value of $n$ to your partner.

Consider deck size $m!+m-1$. When you're handed $m$ cards, compute their sum modulo $m$ and call it $r$. Choose the $(r+1)$st lowest card and hand it to the dealer. This way, there are only $(m-1)!$ possibilities for the hidden card (non-trivial statement). Since there are $(m-1)!$ possible permutations of the remaining $m-1$ cards, you indicate the hidden card to your partner. See formal proof in [Link 1](https://jaylorch.net/brainteasers/TheHiddenCard2/).

See [Link 2](http://blue.butler.edu/~phenders/sigcse2005/niftyworkshop/Handouts/cardTrick.pdf) for a verbose case study of the problem, an existential proof (perfect matching problem in disguise) for the larger deck size and the algorithm, coupled with examples.

</details>

<br>

**Flip a coin.** I place $2^k$ coins on a table in a line with random sides up, and I pick one of them to be the special coin. You can look at the coins and then flip one coin. You leave and your friend enters. Come up with a strategy so that your friend can determine which coin you flipped which coin is the special coin.

<details>
<summary>Show answer</summary>

Good write-up solution in [Link 1](http://datagenetics.com/blog/december12014/index.html), video about the solution in [Link 2](https://www.youtube.com/watch?v=as7Gkm7Y7h4), high-level intuition and relation to hypercube colorings in [Link 3](https://www.youtube.com/watch?v=wTJI_WuZSwE).

</details>

<br>

**100 prisoners.** 100 prisoners labeled 1 to 100, are given a chance to earn their freedom: they are presented with 100 closed boxes, each of which contains a slip with a unique number ranging from 1 up to and including 100. Each prisoner can open 50 boxes (and look inside, and close each box afterwards). If all of the prisoners find their number on a slip, they all go free; but if even one of them fails to find their number, they all die. Of course, no prisoner knows where any of the numbers are, and they can't communicate once the first prisoner has started searching. However, they can communicate and decide on a strategy beforehand. What is a strategy to succeed with probability $> 0.3$?

<details>
<summary>Show answer</summary>

When admitted to the room, each prisoner first inspects the box with his number. He then looks into the box associated with the number on the slip he just found, etc., until he either finds his own number on a slip or has opened 50 boxes (and loses).

Since the slips are put into boxes randomly, the first prisoner will find his slip with probability $1/100$ in the first box. His slip will be in the second box with probability $1/99$. And so on. The probability that he finds his name within 50 boxes is $50/100$. Indeed, assume that he finds his name in exactly $50$ steps. This means that all the boxes he checked form a logical cycle. In other words, also all the other prisoners of that cycle will find their slip in exactly $50$ steps. Moreover, the other prisoners (not in that cycle) will be in a different cycle of the random permutation. So the question we need to ask is whether a random permutation of $100$ numbers has a cycle of length more than $50$.

Let $m > 50$ and observe that any permutation can have at most one $m$-cycle. What's the probability of having such an $m$-cycle? Well, there are ($n$ choose $m$) ways to pick the entries of the cycle, and $(m-1)!$ ways to order them. The rest can be permuted in $(n-m)!$ ways. Altogether there are

$$
\begin{aligned}
\binom{n}{m} \cdot (m-1)! \cdot (n-m)! &= \frac{n!}{m!(n-m)!} \cdot (m-1)! \cdot (n-m)! \\
&= n!/m
\end{aligned}
$$

ways to have a cycle of length $m$. Since there are $n!$ permutations, the probability to have one of exactly length $m$ becomes $1/m$. We need to worry about all cycles that are strictly larger than $50$. The probability of not having any is

$$1-1/51-1/52-\dots-1/100 \approx 0.311828.$$

When generalizing for (arbitrarily many) $n$ prisoners who are allowed to check at most $k\geq n/2$ boxes, the probability is

$$1- \int_{k}^{n} 1/x \, dx = 1- \ln n/k.$$

For example, when $n \to \infty$ and $k=n/2$ the probability approaches $1- \ln 2 \approx 0.306853$.

</details>

<br>

**Number guessing.** Consider an adversary that picks a number $x$ from some set of numbers $S$. You want to learn $x$, but you are only allowed to ask if $x \in S'$ for any subset $S' \subseteq S$ you choose. The adversary can either tell the truth or lie, but they cannot lie twice in a row. Give a $O(\log n)$ query complexity algorithm for finding $x$. Ignore corner cases arising for small $n$.

<details>
<summary>Show answer</summary>

Consider any sets $A,B$, such that $|A|,|B|,|A \cap B|, S \setminus \{A \cup B\} \approx n/4$. Ask if $x\in A$ and then if $x \in B$. If the answers are $(T,T)$: recurse on $S \setminus \{A \cup B\}$, $(F,F)$: recurse on $A \cap B$, $(T,F)$: recurse on $S \setminus \{B \setminus A\}$, $(F,T)$: recurse on $S \setminus \{A \setminus B \}$.

The correctness follows from the fact that there cannot be two consecutive lies, so we can safely exclude one region, which is some constant factor of the total space and the recursion depth is $O(\log n)$. There are some corner cases when $n$ is small, which we ignore.

</details>

<br>

**Airport queue.** Consider a queue of 100 people that want to board the plane. Every $i$:th person is assigned sear $i$ from the plane. However, instead of taking seat 1, the first person chooses a seat randomly. Every following person either takes their assigned seat if possible, or choose a random seat. With what probability, the last passenger gets their assigned seat?

<details>
<summary>Show answer</summary>

Consider the game won if someone occupies seat $1$, since every person that comes later gets their own seat. Consider the game lost if someone besides the last person occupies seat $100$.

When the first person enters the plane, the game is won or lost with probability $1/100$, respectively. If the game is not decided, i.e., the person chooses some seat $x \in [2,99]$, all people between $2$ and $x$ get their own seat. When person $x$ enters the plane, the game is won or lost with probability $1/(100-x+1)$, respectively. By applying this argument iteratively, the desired probability is exactly $1/2$.

</details>

<br>

**Ants on a line.** An adversary drops $100$ ants on a line of length $k$. Every ant has an adversarial orientation, either right or left. Every ant starts walking in the direction of their orientation until they either fall of the line or bump into another ant, in which case they change directions. All ants have the same speed, say $k/100$ per second. What is a tight bound on the time needed for all ants to fall of the line.

<details>
<summary>Show answer</summary>

Instead of thinking that ants change directions after bumping into each other, think of them walking past each other, which looks identical in practice. Hence, an adversarial placement of the ants results in needing $100$ seconds for all ants to fall of. In fact, the number of ants is irrelevant.

</details>

<br>

**Numbers on a cycle.** Consider an even cycle with all nodes choosing a number such that the numbers of all adjacent nodes differ by exactly one. The goal is to find a pair of opposite nodes that chose the same number, or concluding that there are none. A query consists of asking a node for its number. Give a $O(\log n)$ query complexity algorithm.

<details>
<summary>Show answer</summary>

Assume that the cycle is oriented clockwise. Query any two opposing nodes $a$ and $b$. If their parity is different, there is no solution. In other words, if the length of the cycle is not divisible by $4$, there is no solution. If $a=b$, we are done, so assume w.l.o.g. that $a > b$. If you consider plotting the (unknown) values from $a$ to $b$ and $b$ to $a$, the two lines must intersect at some node (due to parity), implying that there must exist opposite nodes with the same value. In order to find them, you query a node $x$ between $a \to b$ and a node $y$ between $b \to a$. If $x=y$, we are done. If $x > y$ recurse on intervals $x-b$ and $y-a$. If $x < y$ recurse on intervals $a \to x$ and $b \to y$.

</details>

<br>

**Lamps in tunnel.** There is a tunnel of unknown length that loops on itself. The curvature of the tunnel is very subtle, so locally, it always looks like you're walking in a straight line. Precisely every $100$ meters, there is a lamp that can be turned on or off. The states of the lamps are initially arbitrary. If you are placed in the tunnel, can you figure out the length of the tunnel in $O(n)$ steps, where $n$ is the length of the tunnel?

<details>
<summary>Show answer</summary>

Traverse in one direction until it looks like you traversed a cycle twice, then change directions and change something in the "first" round of the cycle, and if the change appears in the "second" round of the cycle, it is indeed a cycle and you are done. Otherwise, it was only a path, so you go back to where you turned around and continue searching. If you perform a cycle check after exploring $k$ steps of the tunnel, the next time you can suspect being in a cycle is after exploring at least $2k$ steps of the tunnel. Hence, this gives a runtime of $O(2+4+8+\dots+n)=O(n)$.

</details>

<br>

**Labyrinth.** Consider some finite, directed and strongly connected graph with one node being the exit, and the player being dropped at some starting node. Every out-edge of a node is numbered. A move consist of walking via a chosen out-edge to some other node. When being at a node, the player only sees the nodes numbered out-edges. The player does not know the topology of the graph nor the number of nodes. Design a finite algorithm for finding the exit.

<details>
<summary>Show answer</summary>

Consider we know the graph and the edge numbering, but we don't know where the exits is and where the player is dropped. We can brute-force the solution by assuming we know the node the player is dropped at, and guide the player through all nodes (and hence all possible positions for the exit). If this does not work, we assume the player was dropped at another node and compute where the player ended up via the failed previous sequence. We repeat this for every node.

Because we know nothing about the graph, we have to perform the above for every possible $n$, every possible graph of size $n$ and every possible edge numbering.

</details>

<br>

**Walking along a lollipop.** Consider a directed path that at some point loops back to itself. Two players start at the beginning of the path and can move along the nodes. Design an algorithm for finding the length of the loop.

<details>
<summary>Show answer</summary>

Set the speed of player $A$ to 1 node per time unit and the speed of player $B$ to 2 nodes per time unit. Eventually, they will be reach the loop, and more importantly they will reach some node within the loop. At that point player $B$ stops. The number of steps player $A$ takes until reaching $B$ is the length of the loop.

</details>

<br>

**The Chomp.** Chomp is a two-player game played on a chocolate bar in which the bottom left square is poisoned. The chocolate bar can have an arbitrary number of rows and columns. The two players take turns picking squares, and once they do, they eat every square of the chocolate bar that is above and to the right of the one they picked. The player who eats the poisoned square loses. Prove that there exists a winning strategy for the player who goes first when the chocolate bar is a rectangle of any size.

Give an explicit winning strategy for the player who goes first when the chocolate bar is of size $n \times n$ and $2 \times n$, where $n\geq 2$.

<details>
<summary>Show answer</summary>

We apply the strategy-stealing argument. Assume that the second player has a winning strategy $S$. Suppose then, that the first player takes only the upper right square. By our assumption, the second player has a winning strategy $S$ to this. However, if such a winning response exists, the first player could have played it as their first move and then used $S$ for the remainder of the game. The second player therefore cannot have a winning strategy.

The second player doesn't have a winning strategy, so there is a move that the first player can play such that there's no possible move that the second player can do to ensure a second player win. Suppose that the first player plays said first move. After the first move by both players, we are left with a (possibly non-rectangular) game of Chomp in which the second player doesn't have a winning strategy, and the board now has less squares. Now, we can repeat this argument to find a move that the first player can play in their second turn such that there's no possible move that the second player can do to ensure a second player win. Note that this move in the first player's second turn will depend on what the second player did in their first turn. After both player's second turn, we are left with a board with even less squares in which the first player has a move such that there's no possible move that the second player can do to ensure a second player win. If we keep repeating this argument, we will eventually run out of squares on the board, and since at no time can the second player assure a win, the first player will end up winning, no matter what the second player does. This means that we have proved that the first player has a winning strategy.

When the chocolate bar is of size $n \times n$, the first player chooses square $(2,2)$, after which it copies the second players moves symmetrically, e.g., if they choose $(1,x)$, the first player then chooses $(x,1)$.

When the chocolate bar is of size $2 \times n$, the first player chooses square $(n,2)$. Later, if the second players chooses $(x,1)$, the first player then chooses $(x-1,2)$, and if the second players chooses $(x,2)$, the first player then chooses $(x+1,1)$.

</details>

<br>

**Stones on a grid.** Consider an infinite grid where there is a stone at the origo $(0,0)$, which is in the bottom left corner. As the player, you can remove a stone from any coordinate $(a,b)$ as long as there are no stones at coordinates $(a+1,b)$ and $(a,b+1)$. When a stone at a coordinate $(a,b)$ is removed, two new stones spawn at $(a+1,b)$ and $(a,b+1)$. Prove that, no matter how long the player plays, there will always be a stone such that the sum of its coordinates is $\leq 3$.

Bonus: If one allows $k > 1$ stones per coordinate, what should the bound be?

<details>
<summary>Show answer</summary>

Assign potential $1/2^{a+b}$ to every stone with coordinates $(a,b)$. Initially, the total potential is 1, since $1/2^{0+0}=1$. In fact, throughout the game the total potential is always 1: removing a stone with potential $1/2^{a+b}$ for any $a,b > 0$ spawns two new stones with the combined potential of

$$1/2^{a+b+1} + 1/2^{a+b+1} = 2/2^{a+b+1} = 1/2^{a+b}.$$

Observe that if there would be a stone at every coordinate of the grid, the total potential would be $4$, since summing up the columns yields $2+1+1/2+1/4+\dots=4$. Furthermore, observe that the area $a+b\leq3$ accounts for $13/4$ potential. Hence, if there are no stones within area $a+b\leq3$, the maximum possible potential is $4-13/4=3/4$. Since the total potential is always $1$, there must be a stone such that the sum of its coordinates is $\leq 3$.

Another way to arrive at the same conclusion is to compute the maximum possible potential in area $a+b > 3$ directly by summing up the columns:

$$5/8 + 1/16 + 1/32 + \cdots \leq 1/2 + 1/4 = 3/4.$$

Regarding the bonus question. The potential of the stones throughout the game remains $1$. The sum of the potential of the columns becomes $4k$. Hence, the bound is the smallest $f(k)$ such that

$$4k - k \cdot \sum_{0}^{f(k)} (i+1) \cdot 2^{-i} < 1.$$

For different values of $k$, it holds that $f(1)=3$, $f(2)=4$, $f(3)=5$, $f(4)=6$ and so on. Observe however that already $f(5)=6$ and even $f(12)=7$, due to the rapid growth of $2^i$. It always holds that $f(k) \leq k+2$.

</details>

<br>

**Horse competition.** Given 25 horses, you want to know which are the 3 fastest. However, every competition is limited to 5 horses. After a competition, you only learn the relative performance of the horses involved, and not their absolute speed. What is the "minimum" number of competitions you need to find the 3 fastest horses? Assume that no two horses are equally fast and for sure, they have the same performance in every race.

<details>
<summary>Show answer</summary>

Divide the horses into 5 groups of 5 horses and run a competition for every group. Denote with $t_{i,j}$ the horse that belonged to group $i$ and finished in place $j$. Now run a competition with horses $t_{i,1}$ for all $i\in \{1,5\}$. Assume w.l.o.g. that horse $t_{1,1}$ finished first, $t_{2,1}$ second, $t_{3,1}$ third, etc. We know that horse $t_{1,1}$ is the absolute fastest horse among all 25 horses.

The only possible second and third fastest horses are among $t_{1,2}$, $t_{1,3}$, $t_{2,1}$, $t_{2,2}$ $t_{3,1}$, so we run a competition among them.

</details>

<br>

**Three points on a circle.** Three points are randomly chosen on a circle. What is the probability that the triangle with the vertices at the three points has the center of the circle in its interior?

<details>
<summary>Show answer</summary>

Let $P_1$, $P_2$, and $P_3$ be the points of interest. Let us decompose the random process of choosing $P_1$ and $P_2$ as follows. For both points, let us randomly choose a diameter of the circle, and then flipping a fair coin to determine at which endpoint does the point end up at.

Consider that $P_3$ is drawn randomly, and for $P_1$ and $P_2$ the random diameters are drawn, but it is not yet determined at which endpoints do the points end up. Now, the only possibility for the center to be contained in the triangle is that the furthermost ends (relative to the location of $P_3$) of both diameters are chosen. This probability is $1/4$.

</details>

<br>

**Candy in a box.** There are three boxes of candy: one contains red candies, one contains blue, and one contains a mix of both. Each box has a label, but every box is labeled incorrectly. What is the minimum number of candies you must draw to determine the true contents of all three boxes?

<details>
<summary>Show answer</summary>

You draw once from the mix box. Since it is initially labeled incorrectly, its true label is the color of the candy you draw, w.l.o.g., blue. Now, the box with label red has to be the mix box, and the box with label blue has to be red.

</details>
