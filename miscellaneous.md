## Category

### What is difference between .c and .cpp?
- https://blog.naver.com/netrance/110141020979

### What is difference between .cc and .cpp?
- https://stackoverflow.com/questions/1545080/c-code-file-extension-cc-vs-cpp/1545085
- https://stackoverflow.com/questions/18590135/what-is-the-difference-between-cc-and-cpp-file-suffix

### What is difference between repair and fix?
Repairing is pretty much limited to putting things back to the way they were or restoring them to usefulness. Fixing often goes beyond that to include modifications or improvements.
- https://www.quora.com/What-is-the-difference-between-repair-and-fix

### What is "Eating your own dog food" or "dogfooding"?
Practice of an organization using its own product: https://en.wikipedia.org/wiki/Eating_your_own_dog_food

### What is "Syntactic sugar"?
Syntax within a programming language that is designed to make things easier to read or to express: https://en.wikipedia.org/wiki/Syntactic_sugar

### How can I test a class that has file operation?
Just use actual file with TemporaryFolder as "integration test". Don't mock a type you don't own! (e.g. `BufferedReader`). Your unit tests should only be concerned with how that class works with the content of the file, not the various conditions surrounding the connection. Can I refactor it under single-responsibility principle?
- https://stackoverflow.com/questions/17163484/mockito-mocking-behaviour-of-a-file/17164103
- https://groups.google.com/forum/#!topic/mockito/xhS6YoQxhUs
- https://dzone.com/articles/unit-testing-file-io
- https://github.com/mockito/mockito/wiki/How-to-write-good-tests#dont-mock-a-type-you-dont-own

### How can I understand legacy code?
Add tests. Get familiar with the code by "scratch refactoring".
- https://understandlegacycode.com/blog/key-points-of-working-effectively-with-legacy-code/
- https://dzone.com/articles/lets-deal-with-legacy-code
- https://www.freecodecamp.org/news/conquer-legacy-code-f9e23a6ab758/

### What is "Read the Docs"?
- Sphinx: Tool - https://www.sphinx-doc.org
- Read the Docs: Host - https://readthedocs.org/
- https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html

### What is difference between Declarative programming and Imperative programming?
- Declarative programming: Programming paradigm that expresses the logic of a computation without describing its control flow; focuses on **what** the program should accomplish without specifying how the program should achieve the result
- Imperative programming: Programming paradigm that uses statements that change a program's state; focuses on describing **how** a program operates
