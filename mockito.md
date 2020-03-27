## Category

### What should I read first?
- https://www.baeldung.com/mockito-series
- https://site.mockito.org/
- https://javadoc.io/doc/org.mockito/mockito-core/latest/org/mockito/Mockito.html
- https://github.com/powermock/powermock/wiki

### What is difference between PowerMock and PowerMockito?
PowerMockito is a PowerMock's extension API to support Mockito. To use PowerMock you need to depend on Mockito + PowerMockito (or EasyMock + PowerMock) as well as a test framework. JUnit 4.x not 5.x is required to use PowerMock.
- https://www.baeldung.com/intro-to-powermock
- https://github.com/powermock/powermock/wiki/Getting-Started
```
<dependency>
    <groupId>org.powermock</groupId>
    <artifactId>powermock-module-junit4</artifactId>
    <version>${powermock.version}</version>
    <scope>test</scope>
</dependency>
<dependency>
    <groupId>org.powermock</groupId>
    <artifactId>powermock-api-mockito2</artifactId>
    <version>${powermock.version}</version>
    <scope>test</scope>
</dependency>

<dependency>
    <groupId>org.mockito</groupId>
    <artifactId>mockito-core</artifactId>
    <version>3.3.3</version>
</dependency>

<dependency>
    <groupId>junit</groupId>
    <artifactId>junit</artifactId>
    <version>4.13</version>
    <scope>test</scope>
</dependency>
<dependency>
    <groupId>org.junit.vintage</groupId>
    <artifactId>junit-vintage-engine</artifactId>
    <version>5.6.0</version>
    <scope>test</scope>
</dependency>

<dependency>
    <groupId>org.hamcrest</groupId>
    <artifactId>hamcrest</artifactId>
    <version>2.2</version>
    <scope>test</scope>
</dependency>

<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-api</artifactId>
    <version>5.6.0</version>
    <scope>test</scope>
</dependency>
<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-engine</artifactId>
    <version>5.6.0</version>
    <scope>test</scope>
</dependency>
```

### How do I mock for static class?
- https://www.baeldung.com/intro-to-powermock#methods

### What is ArgumentCaptor?
- https://www.baeldung.com/mockito-series
- https://www.baeldung.com/mockito-argument-matchers

### What is BDDMockito?
The Mockito library is shipped with a BDDMockito class which introduces BDD-friendly APIs.
This API allows us to take a more BDD friendly approach arranging our tests using `given()` and making assertions using `then()`.
- `when/then` → `given/will`
- `verify` → `then`
- https://www.baeldung.com/bdd-mockito
- https://javadoc.io/doc/org.mockito/mockito-core/latest/org/mockito/BDDMockito.html

### How do I mock for final class?
- https://www.baeldung.com/mockito-final

### What is difference between mock, stub and spy?
- There is a difference in that the stub uses state verification while the mock uses behavior verification. Meszaros refers to stubs that use behavior verification as a Test Spy: https://martinfowler.com/articles/mocksArentStubs.html
- When you use the spy then the real methods are called (unless a method was stubbed). Real spies should be used carefully and occasionally, for example when dealing with legacy code: https://javadoc.io/doc/org.mockito/mockito-core/latest/org/mockito/Mockito.html#spy

### How do I mock for new class?
- https://stackoverflow.com/questions/5920153/test-class-with-a-new-call-in-it-with-mockito
- https://stackoverflow.com/questions/48783661/how-to-mock-methods-local-variables-variable-methods-using-mockito
- https://stackoverflow.com/questions/20671008/what-is-the-difference-between-a-local-variable-an-instance-field-an-input-par
- https://github.com/powermock/powermock/wiki/MockConstructor

### What is difference between `Mockito.mock()` and `@Mock`?
There are three different ways of creating mock objects.
- https://www.baeldung.com/java-spring-mockito-mock-mockbean
- If you want `@Mock`, then use `@ExtendWith(MockitoExtension.class)`:
  - https://www.baeldung.com/mockito-junit-5-extension
  - https://stackoverflow.com/questions/40961057/how-to-use-mockito-with-junit5
  - https://stackoverflow.com/questions/55276555/when-to-use-runwith-and-when-extendwith
  - https://www.baeldung.com/junit-5-runwith

### What does it mean that "Warning: it is recommended to use ArgumentCaptor with verification but not with stubbing." in https://javadoc.io/doc/org.mockito/mockito-core/latest/org/mockito/Mockito.html#15?
Just use matcher during stubbing. But verification is a different story. If your test needs to ensure that this method was called with a specific argument, use ArgumentCaptor and this is the case for which it is designed.
- https://stackoverflow.com/questions/12295891/how-to-use-argumentcaptor-for-stubbing

### What is @InjectMocks?
Inject mock or spy fields into tested object automatically.
- https://www.baeldung.com/mockito-annotations#injectmocks-annotation
- https://javadoc.io/doc/org.mockito/mockito-core/latest/org/mockito/Mockito.html#21
- https://javadoc.io/doc/org.mockito/mockito-core/latest/org/mockito/InjectMocks.html
- https://stackoverflow.com/questions/33397643/manually-instantiating-the-injectmock-annotated-field

### Where do I refer to matchers?
- https://javadoc.io/doc/org.mockito/mockito-core/latest/org/mockito/ArgumentMatchers.html
- https://javadoc.io/doc/org.mockito/mockito-core/latest/org/mockito/AdditionalMatchers.html

### How do I test a method use `System.exit()`?
For JUnit 5, refer to https://todd.ginsberg.com/post/testing-system-exit/ and below.
```
@Test
@ExpectSystemExit
public void testMain() {
    main(new String[]{});
}
```
```
<dependency>
    <groupId>com.ginsberg</groupId>
    <artifactId>junit5-system-exit</artifactId>
    <version>1.0.0</version>
    <scope>test</scope>
</dependency>
```
- JUnit 4: https://stefanbirkner.github.io/system-rules/
- https://stackoverflow.com/questions/309396/java-how-to-test-methods-that-call-system-exit

### What do I add into `@PrepareForTest()` for PowerMock?
- https://stackoverflow.com/questions/56430071/what-does-preparefortest-in-powermock-really-mean
- https://javadoc.io/doc/org.powermock/powermock-core/1.6.5/org/powermock/core/classloader/annotations/PrepareForTest.html
- https://www.baeldung.com/intro-to-powermock

### How do I mock singleton?
- http://buckybits.blogspot.com/2011/11/testing-singletons-and-static-classes.html
- https://www.baeldung.com/intro-to-powermock
- https://github.com/powermock/powermock/wiki/mockito#mocking-static-method

### How do I mock File?
Possible with PowerMock. But please don't do that.
- https://stackoverflow.com/questions/17681708/mocking-files-in-java-mock-contents-mockito
- https://stackoverflow.com/questions/16035365/is-it-possible-to-use-powermock-to-mock-new-file-creation

### How do I mock a method in the same test class?
Use `spy` instead of `mock`.
- https://towardsdatascience.com/mocking-a-method-in-the-same-test-class-using-mockito-b8f997916109
