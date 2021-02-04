Nine.java - Style #9 Kick Forward
    - Each function takes an additional parameter, usually the last, which is another function
    - That function parameter is applied at the end of the current function
    - That function parameter is given as input what would be the output of the current function
    - Larger problem is solved as a pipeline of functions, but where the next function to be applied is given as parameter to the current function
    (output: term_frequency9.txt)

Ten.java - Style #10 The One
    - Existence of an abstraction to which values can be converted.
    - This abstraction provides operations to (1) wrap around values, so that they become the abstraction; (2) bind itself to functions, so to establish sequences of functions; and (3) unwrap the value, so to examine the final result.
    - Larger problem is solved as a pipeline of functions bound together, with unwrapping happening at the end.
    - Particularly for The One style, the bind operation simply calls the given function, giving it the value that it holds, and holds on to the returned value.
    (output: term_frequency10.txt)

Note:
No need to compile
All three java files have already compiled using: 
    javac -d out/9 src/Nine.java    (change to 9 10 and Nine Ten respectively)


Instructions:
1. use command line
2. if you are at the root directory
    1) cd week4
    2) cd out 
    3) cd xx          (xx can be 9, 10)
3. to run each class file using commands:
    1) java Nine ../../../pride-and-prejudice.txt
    2) java Ten ../../../pride-and-prejudice.txt

