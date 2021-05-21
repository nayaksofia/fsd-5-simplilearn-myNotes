# Browser:  Microsoft Edge

>Microsoft Edge also provides a driver named `“EdgeDriver”`, which acts as an *intermediatory between Selenium and the Edge browser* and helps in executing the Selenium test cases on the Edge browser.

## How to Run Selenium Test On Edge Browser Using EdgeDriver? 

> Refer This [Article](https://www.toolsqa.com/selenium-webdriver/run-selenium-tests-on-edge/) For More Details. 

> Official Site for Microsoft Edge: [Edge Developer Site](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/)

> Articles: [Selenium Webdriver documentation](https://www.selenium.dev/documentation/en/webdriver/driver_requirements/)

> Edge

```
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.edge.EdgeDriver;

WebDriver driver = new EdgeDriver();
  
```
If Edge driver is not present in your path, you can set the path using the following line:

```

System.setProperty("webdriver.edge.driver", "C:/path/to/MicrosoftWebDriver.exe");
  
```
# Browser Chrome:

## Search for `Selenium IDE for Chrome` and Add the Extension. 

My Chrome Browser Version : Version 90.0.4430.93 (Official Build) (64-bit)

