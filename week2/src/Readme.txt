Four.java - Style #4 Monolith
No abstractions
No use of library functions
(output: term_frequency4.txt)

Five.java - Style #5 Procedural
Larger problem decomposed in procedural abstractions
Larger problem solved as a sequence of commands, each corresponding to a procedure
(output: term_frequency5.txt)

Six.java - Style #6 pipeline
Larger problem decomposed in functional abstractions. Functions, according to Mathematics, are relations from inputs to outputs.
Larger problem solved as a pipeline of function applications
(output: term_frequency6.txt)

Note:
All three java files have already compiled using:
javac xxx.java

Instructions:
1. use command line
2. cd week2 if you are at the root directory
3. to run each class file using commands:
    1) java Four ../pride-and-prejudice.txt
    2) java Five ../pride-and-prejudice.txt
    3) java Six ../pride-and-prejudice.txt