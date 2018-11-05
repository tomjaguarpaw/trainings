# Deep Reinforcement Learning for Join Order Enumeration

https://arxiv.org/abs/1803.00055

Deep Reinforcement Learning for Join Order Enumeration is an interesting
counterpart to [The Case for Learned Index
Structures](arxiv:1712.01208/the-case-for-learned-index-structures.md).  The
latter paper proposed replacing traditional index structures with machine
learned ones.  This paper proposes replacing another part of the join
pipeline: join order selection.

The setup is a fairly standard deep reinforcement learning one.  The states
are (potentially partially built) join orders.  The terminal states are
complete join orders.  Only the terminal states have reward, which is the
speed at which the join executes (reciprocal cost).

One strange aspect is that the encoding of the join orders is very
cumbersome.  The state vector is as large as the number of tables in the
database, and there seems to be one state vector per subtree in the
partially built join order.  It is not clear how this is fed into the
network, nor is the network structure clear.  Figure 2 suggests are
two-hidden-layer fully connected network, but that doesn't seem particularly
plausible.  One wonders why they did not use graph neural networks.

Takes 9.5k queries to train enough to beat Postgres.  This experiment was
done with estimated query performance rather than actual.
