# The simple essence of automatic differentiation

https://arxiv.org/abs/1804.00746

A very elegant and highly general paper, as always with Conal.  His
aim is to distill the precise essence of automatic differentiation so
that everything else about it drops out naturally.  In particular, the
distillation proceeds by translating a program into the language of
cartesian categories (CCs).  In CC form the program can be
differentiated using a simple homomorphism and Conal claims that by
changing the association of the function composation one obtains
forward mode, reverse mode, or a mixed mode AD.

There are a few things that give me pause.  In general Conal's
(beautiful) high level of abstraction seems to obscure some of the
nuts and bolts.

* It seems that recursion is not treated

* I cannot see how one can perform the CC translation without
  incurring significant performance penalty.  The translation to CC
  seems to be designed to do away with `let` and carry the whole
  environment around through function application, which seems
  wasteful.

* I'm still confused about how the order of association can lead to
  mixed modes.  I suppose it's to do with the implicit order in which
  you multiply the sequence of matrices which comprise the Jacobian.
