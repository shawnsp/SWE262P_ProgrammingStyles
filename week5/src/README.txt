Sevemteen.java - This is a variation of Style #17: apply reflection base on code from Style #11
    > Original Style #17 Introspective
        - The problem is decomposed using some form of abstraction (procedures, functions, objects, etc.)
        - The abstractions have access to information about themselves, although they cannot modify that information
    > Variation of Style #17
        1. In the run method of WordFrequencyController (or equivalent in your code, style 11), invoke the methods of the DataStorageManager, StopWordManager, and WordFrequencyCounter objects using reflection.
        2. In your main function (or main block), prompt the user for a class name of one of your application classes (e.g. DataStorageManager) and call a function that prints out all of that class's fields (their names and types), all of its method names, and all of its superclasses and implemented interfaces -- this should be done using reflection, and not hardcoded with conditionals (harcoding with conditionals would be you doing if the user chose DataStorageManager let me printout the fields I know it has, etc.). The printout function should take a class name as string and should work in a generic manner for any class that exists in your application.
    (output: term_frequency17.txt)


Twenty - Style #20 Plugins
    - The problem is decomposed using some form of abstraction (procedures, functions, objects, etc.)
    - All or some of those abstractions are physically encapsulated into their own, usually pre-compiled, packages. Main program and each of the packages are compiled independently. These packages are loaded dynamically by the main program, usually in the beginning (but not necessarily).
    - Main program uses functions/objects from the dynamically-loaded packages, without knowing which exact implementations will be used. New implementations can be used without having to adapt or recompile the main program.
    - External specification of which packages to load. This can be done by a configuration file, path conventions, user input or other mechanisms for external specification of code to be linked at run time.
    
    framework here can be owner party code (provide jar to 3rd party as interfaces to follow)
    words and wordFreqs can be 3d party code (send their jars back to owner party)
    all 3 jars together construct the entire program



-------- User Manual ------
Seventeen: 
    No need to compile
    Seventeen.java has already compiled using: 
        javac -d out/17 src/Seventeen.java 

    To run Seventeen:
        1. cd week5/out/17
        2. java Seventeen ../../../pride-and-prejudice.txt
        3. system will generate top25 words 
        4. ask for a class name
            1) enter one of the four class names and get class information 
                (system will print below information that it has, won't print information that it doesn't have)
                a. fields (name and type)
                b. methods
                c. superclass
                d. interfaces
            2) enter X to quit the program


Twenty:
    No need to compile
    Seventeen.java has already compiled using:
        cd week5/src/Twenty/framework
        javac *.java
        jar cfm framework.jar manifest.mf *.class

        cd week5/src/Twenty/words
        cp ../framework/framework.jar .
        javac -cp ./framework.jar *.java
        jar cf Words1.jar Words1.class
        jar cf Words2.jar Words2.class

        cd week5/src/Twenty/wordFreqs
        cp ../framework/framework.jar .
        javac -cp ./framework.jar *.java
        jar cf WordFreqs1.jar WordFreqs1.class
        jar cf WordFreqs2.jar WordFreqs2.class

        cd week5/out/deploy
        cp ../../src/Twenty/framework/framework.jar .
        cp ../../src/Twenty/words/Words1.jar .
        cp ../../src/Twenty/words/Words2.jar .
        cp ../../src/Twenty/wordFreqs/WordFreqs1.jar .
        cp ../../src/Twenty/wordFreqs/WordFreqs2.jar .


    To run Twenty:
        1. cd week5/out/deploy
        2. java -jar framework.jar ../../../pride-and-prejudice.txt
        3. system will generate top25 words 
