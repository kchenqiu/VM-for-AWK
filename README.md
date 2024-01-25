# VM-for-AWK
Created for CSI 311

## Virtual Machine for AWK Language
A Virtual Machine is "the virtualization or emulation of a computer system". In this Virtual Machine, it will simulate a program that can take in AWK code and process it.

This program is created for the intention of putting AWK code through a Lexer, Parser and Interpreter, in order to translate the code into machine readable language. Most of the code is reusable for other languages by changing the enums(Token.java, OperationNode.java) and syntax for the lexer and parser.

Create a file named "Sample.awk" to put AWK code through the VM. 
Change the file in Main.java in order to use it.

### Lexer
The lexer is made to transform the written code into a sequence of tokens. It removes whitespace, and it will assign tokens to variable names, symbols, keywords(ex. for, if, print, when), strings, and patterns.

Made up of: Lexer.java, StringHandler.java, Token.java

### Parser
The parser is made to transform the sequence of tokens created by the lexer into an Abstract Syntax Tree (AST). It analyzes the code to check that it is using logical grammar for AWK and it separates them into BEGIN, OTHER, END, and FUNCTION blocks within the ProgramNode.

Made up of: AssignmentNode.java, BlockNode.java, BreakNode.java, BuiltinFunctionDefinitionNode.java,ConstantNode.java, ContinueNode.java, DeleteNode.java, DoWhileNode.java, ForNode.java, FunctionCallNode.java, FunctionDefinitionNode.java, IfNode.java, Node.java, OperationNode.java, Parser.java, PatternNode.java, ProgramNode.java, ReturnNode.java, StatementNode.java, TernaryNode.java, TokenHandler.java, VariableReferenceNode.java, WhileNode.java

### Interpreter
The interpreter is the final part of this Virtual Machine and it produces the output of the code. It reads through the AST and it works through the code (ex. checking if the conditions in an if function is true in order to run through the statements in it).

Made up of: Interpreter.java, InterpreterArrayDataType.java, InterpreterDataType.java
