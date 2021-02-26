TwentySix.java - Style #26 Tabular
    - The input data of the problem is modeled as entities with relations between them
    - The data is placed in tables, with columns potentially cross-referencing data in other tables
    - Existence of a relational query engine
    - The problem is solved by issuing queries over the tabular data
    (output: 26.db)

TwentyEight.java - Style #28 Lazy rivers
    - Data comes to functions in streams, rather than as a complete whole all at at once
    - Functions are filters / transformers from one kind of data stream to another


Note:
No need to compile
Both java files have already compiled using: 
    javac -d ../out/26 TwentySix.java 
    javac -d ../out/28 TwentyEight.java


Instructions:
1. use command line
2. if you are at the root directory
    1) cd week6/out/xx      (xx can be 26, 28)
3. run TwentySix class file using commands:
    java -cp :sqlite-jdbc-3.34.0.jar TwentySix ../../../pride-and-prejudice.txt
4. run TwentyEight class file using commands:
    java TwentyEight ../../../pride-and-prejudice.txt

