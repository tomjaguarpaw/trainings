# Don't Unroll Adjoint: Differentiating SSA-Form Programs

https://arxiv.org/abs/1810.07951

An explanation of Zygote, Julia's automatic differentiation tool.

It provides a nice introduction to Pearlmutter and Siskind's higher
order differentiation function "J" and describes the pitfalls of both
tracing and unrolled reverse mode AD implementations.

However, once it gets to section 3 (static single assignment)
everything becomes unclear.  They state, without explanation, the
reverse mode translation of an SSA program.  There is no algorithm nor
translation rules.  Introducing conditionals and iteration only makes
things less clear.

The section "handling language features" is presented fairly
straightforwardly, however.

I'm sure Zygote works as advertised, but the information presented in
this paper doesn't seem sufficient to reconstruct the main ideas.
