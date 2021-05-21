# Automate Your Website With Selenium 

# Live Class-1 Instant Notes

## Links

Project: [Cross Error To Resolve Phase-3:Click Here](https://github.com/wahidKhan74/phase3-spring-ecomm-webservice-03-14-2022/blob/master/src/main/java/com/simplilearn/webservice/config/SimpleCORSFilter.java)

[Selenium Related Jar Files Link](https://www.selenium.dev/downloads/)
[For Mozilla FireFox](https://github.com/mozilla/geckodriver/releases)

# Github Link:
> First Part of Session-1: https://github.com/wahidKhan74/phase5-selenium-test-05-01-2021

> Second Part Of session-1: https://github.com/wahidKhan74/phase5-selenium-junit-test-05-01-2021
> 


# Maven Based Selenium Testing Links:

> https://maven.apache.org/surefire/maven-surefire-plugin/examples/junit-platform.html

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

>https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter-api/5.4.2

>https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-java


# Live Class-2 Instant Notes
Date: 2nd May 2021

Github link:
1.  [First Session](https://github.com/wahidKhan74/phase5-selenium-junit-test-05-01-2021) 
2.  [Second Session](https://github.com/wahidKhan74/phase5-selenium-junit-test-05-01-2021)
3.  [Third Session Part](https://github.com/wahidKhan74/phase5-selenium-junit-test-05-01-2021)



# Notes: After Live Session-1


## Topics to cover in FSD-5

> Testing Application

> Testing Pipeline 

> Cloud Computing 

> AWS

> Docker/Kubernatese

# Automate Your Website With Selenium

>" Selenium is an umbrella project for a range of tools and libraries that enable and support the automation of web browsers."

> Selenium is an `open source` automation tools for testing.

> Selenium itself is a combination of others software pieces, where each piece play a different roles, like 
  1. Selenium IDE: Record and Play Tool
  2. Selenium Remote Control (RC)
  3. Selenium Webdriver
  4. Selenium Grid  

> Selenium Testing helps you for webapplication and mobile application . 

> Plays a key role in DevOps 

##  Features of Selenium IDE:

> Record and playback

> Autofilling Locators: ID, name, link, Xpath, CSS and DOM 

> Dropdown selection of Selenium commands

> Features of debugging tests

> Capability to save tests as HTML and convert to WebDriver Java, Ruby, Python and C# 

> Support for Selenium user-extensions.js file

> Scheduler for scheduling your tests . 

## Testing:

1. Manual Test
```
 - Tester -> e2e test -> functionality test 
 - features of application 
 - It require human efforts
 ```

2. Automation Test
```
- Retable, cost effective 
```

Automation Test is again divided into three types:

a. Functional Test
 - Unit test 
 - Integration Test 
 - User Acceptance Test(e2e)

b. Non-function Test
 - Performance Test
 - Load / Volume Test 
 - Scalability Test 
  
c. Maintenance Test
  
  - Regression Test

# Ideal Practice:

1. It's better to do `Manual Test` first. 
2. Then jump for `Automation Test`.
   
# Selenium IDE 

> According to different Browser You Do Download It
> I Use `selenium ide for microsoft edge` As my browser is: `Microsoft Edge` .

> Refer; [Selenium Documentation](https://www.selenium.dev/documentation/en/getting_started/quick/)

## General Workflow:

Example-1: 
> Create an account

> Configure the unicorn

> Add it to the shopping cart

> Check out and pay 

> Give feedback about the unicorn 

# Installing Selenium Libraries

Java:  Installation of Selenium libraries for java can be done using `Maven`.Add the `selenium-java` dependency in your project `pom.xml`.

```
<dependency>
  <groupId>org.seleniumhq.selenium</groupId>
  <artifactId>selenium-java</artifactId>
  <version>3.X</version>
</dependency>

```

Time: 2:00:00

- Right click on the Command Line OF the Command Column -> Insert new command 

## How to export or export the test cases with java 

- Right click on the name of the main test suit -> Then click on `Export` -> Then do check on `Java JUnit` [It is code based] 

# Disadvantage of Selenium IDE: Play Record Tool

- initial testing.
- no programatic control(for , while loop, if, conditional statement, assertions)
- No Database testing with selenium ide
- CI/CD pipeline integration 
- Cross browser ->
- External Element Control
- Integration of tools jUnit, Jbehave, Jmeter .  

So , we do use `Selenium Web Driver`.  

## Selenium Web Driver

Browser -----> Driver -------> Selenium Classes 


# Selenium Set UP And Basic Test 

## Set Up A Web driver:

1. Download `Selenium Standalone Server jar` and `Selenium Webdriver specific to web-browser` from official site: 
   

- [Click To Download Selenium .Jar File]([selenium.dev/downloads/](https://www.selenium.dev/downloads/))

- Then download a 

    [Selenium Driver File for Browser: Microsoft Edge]()
   
   (or) 
   
   [Chrome Driver Download For Browser Chrome]()
2. Launch Eclipse and Create a Java Project
   
   - Than add the `.jar files`. Make sure all the .jar files will be added in `Class Path`. 
3. Configure Web-driver with eclipse
   
4. Push the code to GitHub Repository
  
Q. `Why linux driver file for the respective browser?` Because it was linux operating system.


# Steps To Configure Web-driver of firfox with eclipse

```
//Step-1: Formulate a base test url.
final String siteURL = "https//www.google.com";

//Step-2: Locate Web Driver
final String  driverPath = "/home/..../geckodriver";

//Step-3: Set selenium system properties
System.setProperty("webdriver.geco.driver",driverPath);

//Step-4: Instantiate selenium web deriver.
WebDriver driver = new FirefoxDriver();

//5. Launch browser.
driver.get(siteURL);

//6. Perform test Evaluation 

String expectedTitle = "Goooogle";

if(expectedTitle.equals(driver.getTitle())){
  System.out.println("Test is Passed !");
} else {
  System.out.println(Test is failed !");
}

System.out.println("Actual :: " + driver.getTitle());
System.out.println("Expected :: " + expectedTitle);


//7.  .close driver

driver.close();

```
Note:

> To Run the test: Right Click -> Run As java Application 

> How to get the `driver path` from eclipse file structure of driver for particular driver? 
```
Right click on driver file name-> properties -> Copy the path from Location.

Add it in `driverPath` . 
```

# Example-2: GoogleSearchTest

> Copy step-1 to step-5: of previous example test. 

Add the following command: 

//`find element`
```
WebElement searchBox = driver.findElement(By.name("q"));

//add text to search box
searchBox.sendKeys("selenium documentation");

//submit text
searchBox.submit();
```
> Click on bookmark and copy the Name 

//Perform Test Evaluation 

> When there is `No Id` , `No Name` is there , Right Click On the element-> Click on copy -> Click on `Copy selector` 

//Open Link

```
WebElement refLink = driver.findElement(By.cssSelector("Past the copy selector link here "));

refLink.click();
```

# Example-3: Create another Class : AmazonHomePage.java

//Step-1: Setup Code
```
final String siteURL = "https://www.amazon.in/"
final String driverPath = "driver/gecodriver";
System.setProperty("webdriver.gecko.driver",driverPath);
Webdriver driver = new FirefoxDriver();
driver.get(siteURL);

```
//Step-2 Perform test evaluation
```
String expectedTitle ="copy the title name and past here";
if(expectedTitle.equals(driver.getTitle())){
  System.out.println("Test is Passed !");
} else {
  System.out.println(Test is failed !");
}

System.out.println("Actual :: " + driver.getTitle());
System.out.println("Expected :: " + expectedTitle);

```

# Maven Based Selenium Test > [Maven + Junit Unit + Selenium ]

Example-1:  

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
> Note: If sth go wrong while running the `Maven` Project , Right Click On The Project -> Maven -> Update Project -> Ok

> Then `Run As-> jUnit Test`

> jUnit provide the `Assert Statement` for test cases.  So no need to write `If...else` . 


# Live Class-2:


