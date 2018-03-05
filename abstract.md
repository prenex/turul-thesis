Kivonat {.unnumbered}
=======

TODO: Magyar kivonat

Abstract {.unnumbered}
========

In this document we investigate a structured source code representation and processing approach with a goal to create "programming language engines" with similar architectural choices of the so-called "3D engines". These 3D engines are visibly dominating the field of 3D game and content development, but for a long time not only compilers, but also the games were created in ad-hoc ways, which later evolved into code "libraries", "frameworks" and more recently/finally complete "engines". While a code library is just a collection of useful methods, and a framework is just a set of rules that define an extensible system - engines provide an all-encompassing and structured way to handle the specifics of a field. Until now I do not know about any works that approach the field of compiler construction using this structured way.

In this document we define, analyse and investigate the structured data-based approach and "plugin scripting" that serves as an extensible architecture of a modern C++14 implementation for the forementioned system. The system is called turul (Tree-Using Really Unorthodox Language) and the readable-binary representation of trees that are used through the solution is called "tbuf" (or turbo-buf) for its hoped processing speed. Despite we are talking about an "engine" for languages, the system can be thought as an extensible language with unseen metaprogramming support too and in the final naming we stick to this terminology.

In our goal to investigate possibilities of more structured ways of compiler constructrion using the engine approach, the differences of the engine approach and compiler-compilers (like lex and yacc) and the underlying algorithms of the efficent implementation is documented as a reference with proper baseline analysis of the ideas. Implementation serves as an extensible engine that can serve as the basis for further research and useful not only in teaching - but for smaller experimental compiler construction to evaluate programming language ideas too.
