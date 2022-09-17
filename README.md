# WLP4-Compiler

This is a compiler written in C++ for a subset of the C language, known as WLP4. A full formal language theory specification of the WLP4 language can be found at https://student.cs.uwaterloo.ca/~cs241/wlp4/WLP4.html. The compiler, referred to as ``wlp4c``, accepts a ``.wlp4`` file and targets a corresponding ``.mips``. Particularly, the compilation of the corresponding ``.mips`` file is a result of the ``.wlp4`` file being sequentially passed into a scanner, parser, code generator, and assembler. These components can be found in the ``Compiler`` subdirectory and must be present for the compiler to generate the machine code correctly.

# Usage

Run ``./wlp4c`` with the desired ``.wlp4`` file as an operand. The ``wlp4c`` progam will produce a corresponding ``.mips`` file in the ``WLP4-Compiler`` directory. Ensure that you run the ``wlp4c`` program in the ``WLP4-Compiler`` directory. 

Provided is ``example.wlp4``, taken from the WLP4 language specification page given above, along with the correspnding ``example.asm`` file. The invocation of ``wlp4c`` to compile ``example.wlp4`` would be 

```sh
./wlp4c example.wlp4
```
