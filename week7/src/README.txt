TwentyOne.java - Style #21 Constructivist
    - Every single procedure and function checks the sanity of its arguments and either returns something sensible when the arguments are unreasonable or assigns them reasonable values
    - All code blocks check for possible errors and escape the block when things go wrong, setting the state to something reasonable


TwentyTwo.java - Style #22 Tantrum
    - Every single procedure and function checks the sanity of its arguments and refuses to continue when the arguments are unreasonable
    - All code blocks check for all possible errors, possibly print out context-specific messages when errors occur, and pass the errors up the function call chain


TwentyFive.java - Style #25 Quarantine: a variation of style #09, The One, with the following additional constraints
    - Core program functions have no side effects of any kind, including IO
    - All IO actions must be contained in computation sequences that are clearly separated from the pure functions
    - All sequences that have IO must be called from the main program


Note:
No need to compile
All three java files have already compiled using: 
    javac -d out/21 src/TwentyOne.java   
    javac -d out/22 src/TwentyTwo.java
    javac -d out/25 src/TwentyFive.java

Instructions:
1. use command line
2. if you are at the root directory
    cd week7/out/21
    cd week7/out/22
    cd week7/out/25
3. to run each class file using commands:
    java TwentyOne ../../../pride-and-prejudice.txt
    java TwentyTwo ../../../pride-and-prejudice.txt
    java TwentyFive ../../../pride-and-prejudice.txt

