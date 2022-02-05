# Login

```Login.java
package Login;

import org.openqa.selenium.By;
import org.openqa.selenium.chrome.ChromeDriver;

public class Login {
	public static void main(String[] args) {
		System.setProperty("webdriver.chrome.driver", "E:\\Workspaces\\EclipseWorkspace\\chromedriver.exe");
		ChromeDriver driver = new ChromeDriver();
		driver.get("https://demo.guru99.com/v4/");
		driver.findElement(By.name("uid")).sendKeys("mercury");
		driver.findElement(By.name("password")).sendKeys("mercury");
		driver.findElement(By.name("btnLogin")).click();
	}
}
```