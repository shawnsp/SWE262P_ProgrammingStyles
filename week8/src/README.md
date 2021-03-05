TwentyNine.java - Style #29 Actors - Similar to the letterbox style, but where the 'things' have independent threads of execution. Constraints:
    - The larger problem is decomposed into 'things' that make sense for the problem domain
    - Each 'thing' has a queue meant for other \textit{things} to place messages in it
    - Each 'thing' is a capsule of data that exposes only its ability to receive messages via the queue
    - Each 'thing' has its own thread of execution independent of the others.

Thirty.java - Style #30 Dataspaces
    - Existence of one or more units that execute concurrently
    - Existence of one or more data spaces where concurrent units store and retrieve data
    - No direct data exchanges between the concurrent units, other than via the data spaces

ThirtyTwo.java - Style #32 Double Map Reduce
    - Input data is divided in chunks, similar to what an inverse multiplexer does to input signals
    - A map function applies a given worker function to each chunk of data, potentially in parallel
    - The results of the many worker functions are reshuffled in a way that allows for the reduce step to be also parallelized
    - The reshuffled chunks of data are given as input to a second map function that takes a reducible function as input

Note:
No need to compile
All three java files have already compiled using: 
    javac -d out/29 src/TwentyNine.java   
    javac -d out/30 src/Thirty.java
    javac -d out/32 src/ThirtyTwo.java

Instructions:
1. use command line
2. if you are at the root directory
    cd week8/out/29
    cd week8/out/30
    cd week8/out/32
3. to run each class file using commands:
    java TwentyNine ../../../pride-and-prejudice.txt
    java Thirty ../../../pride-and-prejudice.txt
    java ThirtyTwo ../../../pride-and-prejudice.txt

