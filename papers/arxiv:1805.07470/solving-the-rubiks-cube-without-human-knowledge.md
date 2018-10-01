# Solving the Rubik's Cube Without Human Knowledge

https://arxiv.org/abs/1805.07470

This is a very cool paper about training a deep reinforcment learning
algorithm to solve the Rubik's cube.  The approach is reminiscent of
Alpha Go Zero, training a policy-value network and combining it with
MCTS.

Unlike Alpha Go Zero they do not train the policy-value network
concurrently with running the MCTS.  Instead they train the network
first and then use MCTS "offline" to solve the cube.  I suppose this
is necessary because there is only one end state for the Rubik's cube,
and indeed this end state is exactly what we are trying to find!  For
Alpha Go Zero all paths reach an end state within some finite number
of moves.

Interestingly the authors make a direct nod to the idea of MCTS being
unsuitable for "single player games".  They store the maximum value
encountered along a tree, not the total (or average).

> unlike other implementations of MCTS, only the maximal value
> encountered along the tree is stored, and not the total value. This
> is because the Rubik’s Cube is deterministic and not adversarial, so
> we do not need to average our reward when deciding a move.

My observation is that if you consider the solved Go game tree or the
solved Rubik's cube graph as a data structure, then the policy-value
network can be considered a lossy compressed version of the same data
structure.  The MCTS is a means of attempting to recover a higher
fidelity version from the compressed version.

After the maximum computation time they use breadth-first search to
solve the cube.  It's unclear to me why they do this, rather than just
continue to use the policy-value network.  The network should be
*more* accurate closer to the solution, after all!
