## Category

### What is hamcrest?
- Framework that assists writing software tests in the Java programming language
- https://github.com/junit-team/junit4/wiki/Matchers-and-assertthat
- Joe Walnes proposes `assertThat()` with hamcrest: https://joewalnes.com/2005/05/13/flexible-junit-assertions-with-assertthat/
- http://hamcrest.org/JavaHamcrest/index
- JUnit 4 supported `assertThat()` by itself, but now hamcrest has `assertThat()` instead of JUnit 5
  - https://junit.org/junit5/docs/current/user-guide/#migrating-from-junit4-tips
  - https://junit.org/junit5/docs/snapshot/user-guide/#writing-tests-assertions-third-party

### What framework do I use for mock?
- https://github.com/mockito/mockito/wiki/Mockito-vs-EasyMock
- https://www.baeldung.com/mockito-vs-easymock-vs-jmockit

### How do I configure JUnit 5 for Maven?
- https://junit.org/junit5/docs/snapshot/user-guide/#running-tests-build-maven

### Where do I refer to matchers?
- http://hamcrest.org/JavaHamcrest/tutorial
- http://hamcrest.org/JavaHamcrest/javadoc/2.2/

### What is difference in assertions between JUnit 4 and JUnit 5?
- https://www.baeldung.com/junit-assertions

### How do I use temporary directory for test?
- https://howtodoinjava.com/junit/junit-creating-temporary-filefolder-using-temporaryfolder-rule/
- https://www.baeldung.com/junit-5-temporary-directory

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
