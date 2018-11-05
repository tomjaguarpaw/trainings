# Efficient Differentiable Programming in a Functional Array-Processing Language

https://arxiv.org/abs/1806.02136

This is a very promising paper about techniques for taking programs written
in a functional programming language (F-smooth, a subset of F#) and using
automatic differentiation to calculate their derivatives.  The applications
of this technique are to any field where optimisation of real-valued
functions is involved, notably computer vision and machine learning.

The F-smooth language is powerful and expressive.  The authors demonstrate
how you can use it to write an embedd domain specific language called
M-smooth, which is very similar to Matlab, R and NumPy.

The authors describe how to use a collection of functional programming
optimisation techniques to generate efficient code.  The techniques include
partial evaluation and loop fusion.  An unusal technique, loop *fission*, is
used to efficiently compile projections from tuples.  One of the key
techniques is using the DPS stack discipline, which I summarised in
[Destination Passing Style](DPS/destination-passing-style.md).

With DPS, the authors show that forward mode automatic derivatives can be
compiled to code that runs as fast as some of the best automatic
differentiation engines currently in use (Tapenade, Theano) even when the
latter use reverse mode (which is typically faster for large problems). 
This result is quite remarkable and I haven't yet managed to understand how
it's possible.
