# Compiler untuk mata kuliah Teknik Kompilator

## Setup Awal
1. Compile file *.java dalam java_cup dan JLex
    ```bash
    javac java_cup/*.java java_cup/runtime/*.java JLex/*.java
    ```
2. Setup untuk model kompilator

    Linux/Unix
    ```bash
    java JLex.Main Scanner.lex
    java java_cup.Main Parser.cup
    mv Scanner.lex.java Yylex.java
    javac *.java
    ```

    Windows
    ```bat
    java JLex.Main Scanner.lex
    java java_cup.Main Parser.cup
    ren Scanner.lex.java Yylex.java
    javac *.java
    ```  

## Cara Compile MINUI
1. Cara compile

    ```bash
    java parser < [input_file]
    ```

    compile dan masukan ke output
    ```bash
    java parser < [input_file] > [target_file]

2. Cara menjalankan target file
    ```bash
    java Machine [target_file]
    ```

