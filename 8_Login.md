# 8 Login
```Login.java
package Login;

import org.openqa.selenium.By;
import org.openqa.selenium.chrome.ChromeDriver;

public class Login {
	public static void main(String[] args) {
		System.setProperty("webdriver.chrome.driver", "E:\\Workspaces\\EclipseWorkspace\\chromedriver.exe");
		ChromeDriver driver = new ChromeDriver();
		driver.get("https://www.facebook.com/");
		driver.findElement(By.name("email")).sendKeys("ashwinathappank@gmail.com");
		driver.findElement(By.name("pass")).sendKeys("Ashwin0208");
		driver.findElement(By.name("login")).click();
	}
}

```