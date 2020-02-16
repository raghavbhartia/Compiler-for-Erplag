erplag-compiler
Term project for the course Compiler Construction
# modules
Lexer (lexer.c) : the module reads the source code in HLL as a stream of charaters and converts sequence of characters to meaningful tokens. the tokens are passed to the parser and contains information about the line of occurance, name of the token, token id etc.\
Parser (parser.c) : parser takes in the sequence of tokens and verifies the syntactical correctness of the source code by constructing the parse tree. the Parser also has error recovery mechanism to parse the complete sequence of tokens even if a syntactical error exist.\
AST Construction (ast.c) : this module takes in the parse tree and 1). Delete all the irrelevant tokens, 2). Changes the structure of to infix notation (for proper checking and evaluation), 3). removes chaining in tree and 4). removes empty non-terminals.\
Symbol Table and Scoping (symboltable.c) : this module constructs the symbol-table for the corresponding AST. The symbol table has a tree structure that depicts the scoping of the blocks of code. Each node of the tree has a linked list of its locally defined variables. It also reports the errors related to redundant declaration, no declaration of variables and modules.\
Type Checker and Semantic Analyser (semantic.c) : this module performs semantic checks on the AST for verifiying semantic correctness of the source code. It also determines the correctness of the expressions.\
Code Generation (codegenerator.c) : Generates the NASM-assembly code of the source code.
