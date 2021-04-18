## Category


### What is difference between Program synthesis and Inductive programming?
- **Program synthesis**: task to construct a program that provably satisfies a given high-level formal specification
- Inductive programming: In many applications the output program must be correct with respect to the examples and partial specification,
and this leads to the consideration of **inductive programming as a special area inside automatic programming or program synthesis**,
usually opposed to 'deductive' program synthesis, where the specification is usually complete.

### What is difference between Program synthesis and Automatic programming?
In contrast to automatic programming techniques, specifications in program synthesis are usually non-algorithmic statements.

### What is difference between Inductive programming and Programming by example?
- **Inductive programming**: special area of automatic programming, covering research from artificial intelligence and programming,
which addresses learning of typically declarative (logic or functional) and often recursive programs **from incomplete specifications, such as input/output examples or constraints**.
  - Incorporates all approaches which are concerned with learning programs or algorithms from incomplete (formal) specifications.
  - Possible inputs:
    - Set of training inputs and corresponding outputs or an output evaluation function, (**Programming by example**)
    - Describing the desired behavior of the intended program, (**Programming by demonstration**)
    - Traces or action sequences which describe the process of calculating specific outputs, (**Programming by demonstration**?)
    - Constraints for the program to be induced concerning its time efficiency or its complexity,
    - Various kinds of background knowledge such as standard data types,
    - Predefined functions to be used,
    - Program schemes or templates describing the data flow of the intended program,
    - Heuristics for guiding the search for a solution or other biases
  - Output: program in some arbitrary programming language containing conditionals and loop or recursive control structures, or any other kind of Turing-complete representation language
- Programming by example (PbE): Application niche for inductive programming; end-user development technique for teaching a computer new behavior by demonstrating actions on concrete examples

### What is difference between Inductive programming and Machine learning?
Inductive programming is seen as a more general area where any declarative programming or representation language can be used
and **we may even have some degree of error in the examples, as in general machine learning**, the more specific area of structure mining or the area of symbolic artificial intelligence.
**A distinctive feature is the number of examples or partial specification needed. Typically, inductive programming techniques can learn from just a few examples.**

### What is difference between Anti-unification and Unification?
https://cstheory.stackexchange.com/questions/34083/what-is-the-difference-between-unification-and-anti-unification
