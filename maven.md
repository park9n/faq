## Category

### What should I read first?
- http://maven.apache.org/guides/getting-started/index.html
- http://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html
- http://maven.apache.org/guides/getting-started/maven-in-five-minutes.html

### What is difference between `maven compile` and `Build Project`?
- https://stackoverflow.com/questions/30166698/difference-between-intellij-project-make-and-maven-compile

### What is `maven-antrun-plugin` and when I use it?
- https://maven.apache.org/plugins/maven-antrun-plugin/
- https://www.geoffhayward.eu/2018/10/maven-packaging-dockerfiles-with-variables

### How do I select dependency version?
The Versions Maven Plugin is the de facto standard way to handle versions management nowadays.
- https://www.baeldung.com/maven-dependency-latest-version

### Should I write all core Maven plugins in a `build` element of the POM?
No, you don't have to.
- https://stackoverflow.com/questions/59557884/how-is-default-maven-plugin-version-decided
- https://www.baeldung.com/core-maven-plugins
- https://maven.apache.org/guides/mini/guide-configuring-plugins.html

### How do I generate executable jar without `no main manifest attribute` issue or `java.lang.NoClassDefFoundError`?
Simply use `maven-assembly-plugin` referring to http://maven.apache.org/plugins/maven-assembly-plugin/usage.html.
- https://www.baeldung.com/executable-jar-with-maven
- https://stackoverflow.com/questions/574594/how-can-i-create-an-executable-jar-with-dependencies-using-maven
```
<plugin>
    <artifactId>maven-assembly-plugin</artifactId>
    <version>3.2.0</version>
    <configuration>
        <archive>
            <manifest>
                <mainClass>com.samsung.tcm.tca.standalone.Main</mainClass>
                <addDefaultImplementationEntries>
                    true
                </addDefaultImplementationEntries>
            </manifest>
        </archive>
        <descriptorRefs>
            <descriptorRef>jar-with-dependencies</descriptorRef>
        </descriptorRefs>
    </configuration>
    <executions>
        <execution>
            <id>make-assembly</id> <!-- this is used for inheritance merges -->
            <phase>package</phase> <!-- bind to the packaging phase -->
            <goals>
                <goal>single</goal>
            </goals>
        </execution>
    </executions>
</plugin>
```

### How do I get version information from POM?
`Main.class.getPackage().getImplementationVersion()` reads `Implementation-Version` from META-INF/MANIFEST.MF.
```
Manifest-Version: 1.0
Implementation-Title: tca-standalone
Implementation-Version: 1.0-SNAPSHOT
Build-Jdk-Spec: 1.8
Created-By: Maven Archiver 3.5.0
Main-Class: com.samsung.tcm.tca.standalone.Main
```
Please add `<addDefaultImplementationEntries>true</addDefaultImplementationEntries>` into POM to save `Implementation-Version` into META-INF/MANIFEST.MF referring to the example for maven-assembly-plugin above.
- https://stackoverflow.com/questions/3697449/retrieve-version-from-maven-pom-xml-in-code/41791885
- https://github.com/remkop/picocli/issues/236

### How do I use logger (SLF4J + Logback)?
Please add following dependency only. In addition to `logback-classic-1.2.3.jar`, this will pull `slf4j-api-1.7.28.jar` as well as `logback-core-1.2.3.jar` into your project. Please ensure that the version `slf4j-api` automatically pulled is under 1.8. If it is 1.8 or later, you meet http://www.slf4j.org/codes.html#noProviders.
```
<dependency> 
  <groupId>ch.qos.logback</groupId>
  <artifactId>logback-classic</artifactId>
  <version>1.2.3</version>
</dependency>
```
- http://www.slf4j.org/manual.html#projectDep
- https://www.baeldung.com/logback
- http://logback.qos.ch/reasonsToSwitch.html

### What is `mvn integration-test`?
- https://stackoverflow.com/questions/1399240/how-do-i-get-my-maven-integration-tests-to-run
- https://blog.sonatype.com/2009/06/integration-tests-with-maven-part-1-failsafe-plugin/
- http://maven.apache.org/surefire/maven-failsafe-plugin/index.html
- http://maven.apache.org/surefire/maven-failsafe-plugin/usage.html
- http://maven.apache.org/surefire/maven-failsafe-plugin/examples/inclusion-exclusion.html
- https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html
- https://www.baeldung.com/maven-integration-test

### What is "SNAPSHOT" version?
- https://maven.apache.org/guides/getting-started/index.html#What_is_a_SNAPSHOT_version

### How do I avoid `logback.xml` conflict between the project and the external library?
- Exclude `logback.xml` when packaging library: https://mkyong.com/maven/maven-exclude-logback-xml-in-jar-file/
- Exclude from the existing library: https://stackoverflow.com/questions/33897196/how-to-disable-inherited-logback

### What is difference between `<dependencies>` inside `<plugin>` and outside `<plugin>`?
- https://stackoverflow.com/questions/24716142/maven-differences-between-dependencies-inside-plugin-and-outside
- https://maven.apache.org/guides/mini/guide-configuring-plugins.html
