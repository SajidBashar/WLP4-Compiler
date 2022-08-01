# WLP4-Compiler

This is the resulting compiled files for a WLP4 compiler written for CS 241, written in C++.  The compiler takes in ``.wlp4`` files and generates ``.asm`` files, from which one can use the appropriate converters to generate the resulting ``.mips`` code.

Download all the files.  I have provided a ``compile.sh`` script in ``/req/``.  To compile, just do ``compile.sh <your_file>.wlp4``, where ``<your_file>`` is the file name.  This will generate a ``.asm`` file of the same name in the same directory.  Provided is ``example.wlp4``, pulled off the WLP4 overview page linked above, as well as the resulting ``example.asm`` file.

Note that I did not compile all the code into one big program, and **every** file in the ``./req/`` folder is required for this to work, *including* the wlp4grammar.lr1 file!  

Specifically, you must run your WLP4 first through the scanner (wlp4scan), then the parser (wlp4parse), and finally the code generator (wlp4gen).  This is just how the nature of the assignment went.  In short, you would want to pipe the result of each stage into the next, as per the ``compile.sh`` file provided. 

The compiler features various optimization features to reduce the length of the generated file.
WLP4 is a subset of C, with various limitations put in to make it more digestable to write a compiler for second year students. A full specification of the language can be found at: https://student.cs.uwaterloo.ca/~cs241/wlp4/WLP4.html. 

