# CompilerProject

# Overview of zip file
The zip file contains all of the files that has:
- A c++ program that gets rid of white spaces from a given file "Incorrect_code.txt"
- Compiles our lex and yacc files that check the white-space free file for syntax errors
- Converts the fixed file to a cpp program and generate aba13.cpp
- Executes the aba13.cpp file

*OTHER FILES IN FOLDER*
- lex.yy.c, y.tab.c, and y.tab.h are generated from the lex and yacc files by running the commands listed below 
- Checking the syntax errors in the given incorrect file
```
lex lexer.lex
yacc Syntax_Checker.yacc
cc y.tab.c lex.yy.c -o syntax_analyzer
./syntax_analyzer Incorrect_code.txt
```
- To convert to c++
```
lex cpp_converter_lexer.lex
yacc convert_to_cpp.yacc
cc y.tab.c lex.yy.c -o Converter
./Converter 
```
- y.tab.h must **NOT** be changed
- Valid_Code.txt is the correct file output we want to analyze with no errors and to convert to c++ program, aba13.cpp
- Makefile contains all the compile and execute commands that will run all our code automatically with the command
```
make all
```

# Written by:
Kailie Chang\
Ryan Chen\
Dianne Lopez\
Mina Trevizo
