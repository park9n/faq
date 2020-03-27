## Category

### What is difference between .c and .cpp?
- https://blog.naver.com/netrance/110141020979

### What is difference between .cc and .cpp?
- https://stackoverflow.com/questions/1545080/c-code-file-extension-cc-vs-cpp/1545085
- https://stackoverflow.com/questions/18590135/what-is-the-difference-between-cc-and-cpp-file-suffix

### What is "Eating your own dog food" or "dogfooding"?
Practice of an organization using its own product: https://en.wikipedia.org/wiki/Eating_your_own_dog_food

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
