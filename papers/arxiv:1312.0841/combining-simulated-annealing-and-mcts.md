# Combining Simulated Annealing and Monte Carlo Tree Search for
  Expression Simplification

https://arxiv.org/abs/1312.0841

This paper doesn't do anything to convince me that MCTS makes any
sense for trees that are not two player extensive form zero sum games.
In order to promote searching the tree deeply they introduce a dynamic
exploration parameter T which decreases as the number of iterations
increases.  Why don't they just sample the next state from the
neighbours of *all* nodes visited so far?  There's no need to walk
down the tree from the root (i.e. the original expression)!
