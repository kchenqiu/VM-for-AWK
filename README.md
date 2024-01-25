# VM-for-AWK
Created for CSI 311

## Virtual Machine for AWK Language
A Virtual Machine is "the virtualization or emulation of a computer system", in this Virtual Machine, it will simulate a program that can take in AWK code and process it.

This program is created for the intention of putting AWK code through a Lexer, Parser and Interpreter, in order to translate the code into machine readable language. Most of the code is reusable for other languages by changing the enums(Token.java, OperationNode.java) and syntax for the lexer and parser.

Create a file name "Sample.awk" to put AWK code through the VM. 
Change the file in Main.java in order to use it.

### Lexer
The lexer is made to transform the written code into a sequence of tokens.

Made up of: Lexer.java, StringHandler.java, Token.java

### Parser
The parser is made to transform the sequence of tokens created by the lexer into an abstract-syntax tree (AST)

Made up of: AssignmentNode.java, BlockNode.java, BreakNode.java, BuiltinFunctionDefinitionNode.java,ConstantNode.java, ContinueNode.java, DeleteNode.java, DoWhileNode.java, ForNode.java, FunctionCallNode.java, FunctionDefinitionNode.java, IfNode.java, Node.java, OperationNode.java, Parser.java, PatternNode.java, ProgramNode.java, ReturnNode.java, StatementNode.java, TernaryNode.java, TokenHandler.java, VariableReferenceNode.java, WhileNode.java

### Interpreter
The interpreter is the final part of this Virtual Machine and it produces the output of the code

Made up of: Interpreter.java, InterpreterArrayDataType.java, InterpreterDataType.java
