# Title Check

```TitleCheck.java
package TitleCheck;

import org.openqa.selenium.By;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class TitleCheck {
    public static void main(String[] args) {
        System.setProperty("webdriver.chrome.driver", "E:\\Workspaces\\EclipseWorkspace\\chromedriver.exe");
        ChromeDriver driver = new ChromeDriver();
        driver.get("https://google.com");
        String title = driver.getTitle();
        System.out.println("Title is : " + title);
        if (title.equals("Google")) {
            System.out.println("True");
        } else {
            System.out.println("False");
        }

        driver.get("https://en.wikipedia.org/wiki/Main_Page");
        driver.findElement(By.id("pt-login")).click();
        String url = driver.getCurrentUrl();
        if (url.equals("https://en.wikipedia.org/w/index.php?title=Special:UserLogin&returnto=Main+Page")) {
            System.out.println("True");
        } else {
            System.out.println("False");
        }
    }
}```