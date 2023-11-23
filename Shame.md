# Problems which I Open the Editorial to Solve

## http://codeforces.com/problemset/problem/383/D - Antimatter

I thought this is some kind of a subset sum, which I think we can use some sort of Divide and Conquer, didn't realize the solution of dp where storing the balance exist. Very easy after that.

## https://codeforces.com/problemset/problem/351/E - Jeff and Permutation

Have little to no idea on how to minimize them permutations, tried to brute force and see the patterns that it would be like - - - - then + + + +, but for some times it gets random in the middle, turns out the observation of separating it by the largest elements and observing the inversion from that, no idea this could be done.

## https://codeforces.com/problemset/problem/1870/E - E. Another MEX Problem

Ideas:

- Binary search, but figuring out its not binary search the answerable,
- Got observation that it can be greedied by bits, probably involves some weird ds shit.
- Reducable to ignoring the mex, we can compute all possible segments in quadratic time, the DP now turns into pick subset of non adjacent element which results in the maximum xor.
- $N^3$ is pretty easy.
- Reducable to graph and maybe dijkstra able, each node will have $5000$ edges, each pointing to the minimum index which have mex equals to a certain value. check whether endNodes is visitable
- But this is impossible because then we have $5000^2$ nodes and each nodes have $5000$ edges.
- need a convolution to check whether a node is reachable for a certain node, but the node is impossible to pass between each others.

### Where I fucked up

- Turns out we do an edge reducal observation by using pigeonhole principle, the number of segments that exists is not $N^2$, but only $N$.

