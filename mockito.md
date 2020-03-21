## Category

### What should I read first?
- https://www.baeldung.com/mockito-series
- https://site.mockito.org/
- https://javadoc.io/doc/org.mockito/mockito-core/latest/org/mockito/Mockito.html

### What is different between PowerMock and PowerMockito?
PowerMockito is a PowerMock's extension API to support Mockito.
- https://www.baeldung.com/intro-to-powermock

### How do I mock for static class?
- https://www.baeldung.com/intro-to-powermock#methods

### What is ArgumentCaptor?
- https://www.baeldung.com/mockito-series
- https://www.baeldung.com/mockito-argument-matchers

### What is BDDMockito?
The Mockito library is shipped with a BDDMockito class which introduces BDD-friendly APIs.
This API allows us to take a more BDD friendly approach arranging our tests using `given()` and making assertions using `then()`.
- https://www.baeldung.com/bdd-mockito

### How do I mock for final class?
- https://www.baeldung.com/mockito-final

### What is different between mock, stub and spy?
- There is a difference in that the stub uses state verification while the mock uses behavior verification. Meszaros refers to stubs that use behavior verification as a Test Spy: https://martinfowler.com/articles/mocksArentStubs.html
- When you use the spy then the real methods are called (unless a method was stubbed). Real spies should be used carefully and occasionally, for example when dealing with legacy code: https://javadoc.io/doc/org.mockito/mockito-core/latest/org/mockito/Mockito.html#spy

### How do I mock for new class?
- https://stackoverflow.com/questions/5920153/test-class-with-a-new-call-in-it-with-mockito

### What is different between `Mockito.mock()` and `@Mock`?
There are three different ways of creating mock objects.
- https://www.baeldung.com/java-spring-mockito-mock-mockbean
- If you want `@Mock`, then use `@ExtendWith(MockitoExtension.class)`: https://www.baeldung.com/mockito-junit-5-extension, https://stackoverflow.com/questions/40961057/how-to-use-mockito-with-junit5, https://stackoverflow.com/questions/55276555/when-to-use-runwith-and-when-extendwith

### What does it mean that "Warning: it is recommended to use ArgumentCaptor with verification but not with stubbing." in https://javadoc.io/doc/org.mockito/mockito-core/latest/org/mockito/Mockito.html#15?
Just use matcher during stubbing. But verification is a different story. If your test needs to ensure that this method was called with a specific argument, use ArgumentCaptor and this is the case for which it is designed.
- https://stackoverflow.com/questions/12295891/how-to-use-argumentcaptor-for-stubbing
