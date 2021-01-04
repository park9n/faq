## Category

### What is listener?
- https://github.com/antlr/antlr4/blob/master/doc/listeners.md

### Where is grammars?
- https://github.com/antlr/grammars-v4

### How do I use IntelliJ IDEA plug-in?
- https://plugins.jetbrains.com/plugin/7358-antlr-v4-grammar-plugin

### What is separate .g4 files?
- https://stackoverflow.com/questions/24299214/using-antlr-parser-and-lexer-separatly
- https://stackoverflow.com/questions/32985258/how-to-split-an-antlr-grammar-file-into-multiple-ones

### What is difference between abstract syntax tree and parse tree?
ANTLR 4 constructs parse tree (=concrete syntax tree), NOT abstract syntax tree. ASTs differ from parse trees because superficial distinctions of form, unimportant for translation, do not appear in syntax trees.
- **Parse tree**: representation of grammars in a tree-like form (leaves are tokens); **very formal representation** that strictly shows how the parser understands the statement
- **AST**: **"simplified"** syntactic representations of the source code; without showing the whole syntactic clutter, represents the parsed string in a structured way, discarding all information that may be important for parsing the string, but isn't needed for analyzing it

Refer to
- https://stackoverflow.com/questions/29971097/how-to-create-ast-with-antlr4
- https://github.com/antlr/antlr4/blob/master/doc/faq/general.md#what-is-the-difference-between-antlr-3-and-4
- https://stackoverflow.com/questions/5967888/whats-the-difference-between-parse-trees-and-abstract-syntax-trees
- https://github.com/datacamp/antlr-ast

### What is difference between abstract syntax tree and control flow graph?
- http://www.cs.columbia.edu/~suman/secure_sw_devel/Basic_Program_Analysis_CF.pdf
- http://web.cs.iastate.edu/~weile/cs641/2.ProgramRepresentations.pdf
- https://en.wikipedia.org/wiki/Abstract_syntax_tree
- https://en.wikipedia.org/wiki/Control-flow_graph
