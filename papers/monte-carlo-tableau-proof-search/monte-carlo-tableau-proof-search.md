# Monte Carlo Tableau Proof Search

http://cl-informatik.uibk.ac.at/users/cek/docs/17/mfckju-cade17.pdf

I don't find this paper particularly convincing and in fact it just
strengthens my belief that MCTS doesn't make sense for a setting that
is not a two-player zero-sum extensive form game.  The evidence for
this is the β-minimal Expansion Policies which are heuristics needed
to make the algorithm more efficient.  It seems these heuristics
manipulate the "game tree" in a way that does not preserve the
original structure of the proof search tree.
