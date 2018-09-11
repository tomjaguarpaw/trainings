# Using Destination-Passing Style to Compile a Functional Language
into Efficient Low-Level Code

https://www.microsoft.com/en-us/research/wp-content/uploads/2016/11/dps-submitted.pdf

This is a very nice paper which takes to its logical conclusion the C
idiom of passing to function a pre-allocated buffer ("destination
passing style").  With a functional language with sufficient
restrictions ("F smooth") one can compile to C code that does not heap
allocate.  All data can be stored on a stack.  In consequence, code
written in this high-level functional language can be compiled to code
that runs as fast as hand-written C.

If you want to implement a highly-efficient high-level language then
read this paper!
