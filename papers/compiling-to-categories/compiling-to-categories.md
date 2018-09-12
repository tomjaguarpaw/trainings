# Compiling to Categories

http://conal.net/papers/compiling-to-categories/compiling-to-categories.pdf

Another lovely and clearly written paper from Conal which takes an
idea to a high level of abstraction.  He shows that any simply typed
lambda calculus (STLC) expression can be rewritten in the operations
of a cartesian closed category (CCC).  The benefit is that many other
languages and contexts are also CCCs, for example hardware wiring
diagrams and languages for automatically differentiated functions.
One can then freely convert between these different categories by
applying simple functorial operations.  Given the simple primitive
functorial operations, automatic differentiation then comes "for
free".

As with Conal's work on automatic differentation, I am concerned that
the translation will give poorly performing results if used as the
intermediate language of a compiler.  It seems to be too far away from
the machine, and even too far away from a realistic abstract machine.

Nonetheless, the paper is eye opening and thought provoking and a good
read for anyone interested in functional programming, compilers or AD.
