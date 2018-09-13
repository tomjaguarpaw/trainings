# The Case for Learned Index Structures

https://arxiv.org//1712.01208

This paper takes the rather ingenious point of view that database
indexes, be they range indexes, point indexes or existence indexes,
are just functions from keys to values, and thus it is reasonable to
consider replacing them with learned functions of the same type.
Learning range and point indexes is a regression problem and learning
existence indexes is a classifaction problem.

Indexes may already be approximate (they only index a subset of keys)
and already retrained (B-trees need to be rebalanced).

The paper is quite convincing that replacing B-trees or other indexing
structures with machine learned models is a plausible route to faster
database lookups.
