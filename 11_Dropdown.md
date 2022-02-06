# Dropdown

```Dropdown.java
package Dropdown;

import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

public class Dropdown {
	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", "E:\\Workspaces\\EclipseWorkspace\\chromedriver.exe");
		
		ChromeDriver driver = new ChromeDriver();
		
		driver.get("https://demoqa.com/select-menu");
		
		Select select = new Select(driver.findElementById("cars"));
		System.out.println("All Available Elements are : ");
		for (WebElement w : select.getOptions()) {
			System.out.println(w.getText());
		}
		
		if (select.isMultiple()) {
			select.selectByIndex(2);
			Thread.sleep(1000);
			select.selectByValue("saab");
			Thread.sleep(1000);
			select.selectByVisibleText("Audi");
			Thread.sleep(1000);
			System.out.println("\n\n\nThe selected elements are : ");
			for (WebElement w : select.getAllSelectedOptions()) {
				System.out.println(w.getText());
			}
			
			select.deselectByIndex(2);
			Thread.sleep(1000);
			select.deselectByValue("saab");
			Thread.sleep(1000);
			
			System.out.println("\n\n\nAfter deselection the selected elements are : ");
			for (WebElement w : select.getAllSelectedOptions()) {
				System.out.println(w.getText());
			}
		}
		
	}
}
```