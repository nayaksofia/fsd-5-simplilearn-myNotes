# Maven Based Selenium Test > [Maven + Junit Unit + Selenium ]

>Step-1: Create Maven Project

>Step-2: Choose: `maven-archetype-quickstart`

>Step-3:  Group ID: com.ecom.webapp
> ArtifactID: phase5-selenium-junit-test-05-01-2021

>Step-4:  Open `pom.xml` file
- Integrate jUnit5 here:
 
- So, Search for dependency : `junit.jupiter.api` in google search

## And add the following dependencies.

First, remove the previous jUnit dependency. 
```
<!--junit-jupiter-api-->
<dependency>
  <groupId>org.junit.jupiter</groupId>
  <artifactId>junit-jupiter-api</artifactId>
  <version>5.4.2</version>
  <scope>test</scope>
</dependency>

<!--junit-jupiter-engine-->
<dependency>
  <groupId>org.junit.jupiter</groupId>
  <artifactId>junit-jupiter-engine</artifactId>
  <version>5.4.2</version>
  <scope>test</scope>
</dependency>

<!--selenium-java-->
<dependency>
   <groupId>org.seleniumhq.selenium</groupId>
   <artifactId>selenium-java</artifactId>
   <version>3.141.59 </version>
</dependency>

```
Then Add In <Properties> Tag for compiler settings. 

```
<maven.compiler.target>8</maven.compiler.target>
<maven.compiler.source>8</maven.compiler.source>
```

> Step-5: Search for `junit 5 maven surefire ` plugin and add it after <dependencies></dependencies> Tag.

[Link Of Surefire Plugin To Download](https://maven.apache.org/surefire/maven-surefire-plugin/examples/junit-platform.html
)

```
<build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-surefire-plugin</artifactId>
                <version>3.0.0-M5</version>
            </plugin>
        </plugins>
</build>

```
If we do not add this plugin , we can't able to execute the jUnit test cases from Maven. 
> Step-6: Add `driver for browser chrome/microsoft edge` of your choice. No need to add the `Selenium Standalone Server.jar` , as we already add dependency in `pom.xml` files.

> Step-7: Now add `jUnit Test Case` on the file structure of `src/test/java`.
For that, right click `package name` -> Other -> Search `jUnit Test Case` -> Click on `jUnit Test Case`.

> Then, write Name:`TestCaseName`
> Make sure you do check the Check box of `New jUnit Jupiter Test`  And check the `setUp` and `tearDown`

>Step-8: Write the code for test.

>Step-9: Final Step TO Execute. 

```
Right Click on project -> Run As -> JUnit Test
```
> **Improtant Notes**: If sth go wrong while running the `Maven` Project , `Right Click On The Project Name -> Maven -> Update Project -> Ok`

> Then `Run As-> jUnit Test`

> jUnit provide the `Assert Statement` for test cases.  So no need to write `If...else` . 