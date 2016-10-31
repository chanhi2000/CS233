# CS233 - Computer Architecture

[[IllinoisUniversity] Computer Architecture][1]


## COURSE OBJECTIVES:

1. Grasp basic principles of combinational and sequential logic design.
2. Have a high-level understanding of how to design a general-purpose computer, starting with simple logic gates.
3. To provide you with a mental model of how high-level language programs get executed on computer hardware
4. To introduce you to the organization and performance analysis of modern computers,
5. Expose you to the hardware-level mechanisms for exposing parallelism.

The first two goals we will address together as we teach you the principles of logic design through the implementation of a processor capable of executing a subset of the MIPS instruction set architecture (ISA). Along the way we will discuss how computers represent numbers, understand the decode/execute model, the design of finite state machines and more. Specifically we will test the following objectives:

a. students should be able to design modest combinational circuits (20-30 gates) from an natural language (*e.g.*, English) specification
b. students should be able to design finite state machines of moderate complexity (10-20 states) from a natural language specification. Furthermore, they should be able to implement these FSMs using a collection of gates and flip flops.
c. students should be able to analyze the design of a simple processor and modify a Verilog implementation to implement new instructions.

As computers execute programs in machine language, we will address the third goal through an extensive discussion of machine language and its human readable counterpart, assembly language. We will demonstrate how features of modern programming languages (*e.g.*, function calls, recursion, pointers, dynamic memory allocation, etc.) are implemented in assembly language. In addition, topics like compilation, linking, I/O programming, and interrupt programming will be covered. We will specifically test the following objectives:

d. students should be able to translate small (20 line) C programs that include conditionals, loops, function calls, recursion, data structures, and pointers into MIPS assembly, observing calling conventions and stack management.
e. students should be able to translate short (30 line) MIPS programs to corresponding C programs including function prototypes.

The fourth goal will be addressed in three ways: 1) We will present an overview of the organization of modern computers (processor, memory, I/O system) demonstrating the key challenges and ideas (*e.g.*, pipelining, caching, indirection, etc.) that influence their design, 2) we will present both theoretical and practical performance analysis techniques and analyze the performance of many parts of modern machines (processors, memory, caches, disks, networks), and 3) we will write code in high-level languages and assembly to optimize program execution. We will specifically test the following objectives:

f. students should be able to define and provide examples of the key implementation ideas of modern computers (abstraction, caching, hierarchy, indirection, pipelining, parallelism, speculation).
g. students should be able to analyze performance questions to identify what phenomena and/or numerical values are required and compute a result if these are provided.
h. students should be able to identify the hardware structures in a pipelined processor and cache/memory systems and explain their role.

While the previous goals focus primarily on single-processor systems, the last goal presents hardware mechanisms for implementing parallel processing. Specifically, we will discuss SIMD execution, cache coherence, memory consistency, and hardware synchronization primitives. As part of this discussion, we introduce concepts of race conditions, false sharing, and the need for memory barriers. We will specifically test the following objectives:

i. Provided a small piece of code executing on a shared memory parallel computer, students should be able to recognize synchronization, coherence, and consistency pitfalls that could impact the execution's result or performance.


## TEXTBOOK:
- __Logic and Computer Design Fundamentals__, by M. Morris Mano and Charles R. Kime. (Published by Prentice-Hall), 2008.
	- Fourth Edition 2008 ISBN: 0-13-198926-X
- __Computer Organization & Design: The Hardware/Software Interface__, by David A. Patterson and John L. Hennessy. (Published by Morgan Kaufmann)
	- Second Edition: 1998 ISBN: 1-55860-428-6
	- Third Edition: 2004 ISBN: 1-55860-604-1
	- Fourth Edition 2008 ISBN-13: 978-0123744937
- __Verilog HDL: A Guide to Digital Design and Synthesis__,  by Samir Palnitkar. (Published by Prentice Hall).
	- Second Edition:2003 ISBN: 0-13-044911-3

The first part of this course follows the first book Logic and Computer Design Fundamentals, but much of this material is available in an appendix of Computer Organization & Design: The Hardware/Software Interface.

Some of the discussion sections in the first part of the course consist of Verilog problems, for which the Verilog HDL book can be used as a reference. However, the Verilog material covered in this course is very basic, and you should be able to find on-line any references needed.
The second and third part of this course follows the book on Computer Organization & Design: The Hardware/Software Interface very closely, so it is highly recommended, but many students find they don't refer to the book. Any of the second, third, or fourth editions are fine.


[1]: https://wiki.cites.illinois.edu/wiki/display/cs233sp16/Home
