# Number Of Elements

```NumberOfElements.java
package NumberOfElements;

import java.util.List;

import org.openqa.selenium.By;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class NumberOfElements {
	public static void main(String[] args) {
		System.setProperty("webdriver.chrome.driver", "E:\\Workspaces\\EclipseWorkspace\\chromedriver.exe");
		ChromeDriver driver = new ChromeDriver();
		driver.get("https://www.google.co.in/");
		List<WebElement> links = driver.findElements(By.xpath("//img"));
		List<WebElement> allElements = driver.findElements(By.xpath("//*"));
		System.out.println("Total images = " + links.size() + "\nTotal Elements = " + allElements.size());
	}
}```