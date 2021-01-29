Twelve.java - Style #12 LetterBox
    - the larger problem is decomposed into 'things' that make sense for the problem domain
    - Each 'thing' is a capsule of data that exposes one single procedure, namely the ability to receive and dispatch messages that are sent to it
    - Message dispatch can result in sending the message to another capsule
    (output: term_frequency12.txt)

Thirteen.java - Style #13 Closed Maps
    - The larger problem is decomposed into 'things' that make sense for the problem domain
    - Each 'thing' is a map from keys to values. Some values are procedures/functions.
    (output: term_frequency13.txt)

Sixteen.java - Style #16 Publish-Subscribe
    - Larger problem is decomposed into entities using some form of abstraction (objects, modules or similar)
    - The entities are never called on directly for actions
    - Existence of an infrastructure for publishing and subscribing to events, aka the bulletin board
    - Entities post event subscriptions (aka 'wanted') to the bulletin board and publish events (aka 'offered') to the bulletin board. the bulletin board does all the event management and distribution
    (output: term_frequency16.txt)

Note:
No need to compile
All three java files have already compiled using: 
    javac -d out/12 src/Twelve.java    (change to 12 13 15 and Twelve, Thirteen, Fifteen respectively)


Instructions:
1. use command line
2. if you are at the root directory
    1) cd week3 
    2) cd out 
    3) cd xx          (xx can be 12, 13, 15)
3. to run each class file using commands:
    1) java Twelve ../../../pride-and-prejudice.txt
    2) java Thirteen ../../../pride-and-prejudice.txt
    3) java Six ../pride-and-prejudice.txt



Special Instructions: 
    Thirteen.java is runing 13.2
    if 13.1 is what you are looking for, comment out the code right after //13.2 and uncomment //13.1
    compile it at week3 folder using: javac -d out/13 src/Thirteen.java
    then go to week3/out/13 amd run: java Thirteen ../../../pride-and-prejudice.txt

    Sixteen.java is runing 16.2
    if 16.1 is what you are looking for, comment out the code that indicated with //16.2
    compile it at week3 folder using: javac -d out/16 src/Sixteen.java
    then go to week3/out/16 amd run: java Sixteen ../../../pride-and-prejudice.txt