# Selenium

package sample;

import java.util.List;

import org.openqa.selenium.Alert;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.ExpectedConditions;
import org.openqa.selenium.support.ui.WebDriverWait;

public class Program {

	public static void main(String[] args) throws InterruptedException {
		// TODO Auto-generated method stub
		
		System.setProperty("webdriver.chrome.driver", "C:\\Users\\Prasatho\\chromedriver.exe");
		WebDriver driver=new ChromeDriver();
	
		driver.get("https://www.goindigo.in/");
		List<WebElement> ab=driver.findElements(By.xpath("//input[@type='radio']"));
		System.out.println(ab.size());
		//WebDriverWait wait = new WebDriverWait(driver, 10);
		//wait.until(ExpectedConditions.visibilityOfAllElements(ab));
		ab.get(2).click();
		
		//wait.until(ExpectedConditions.elementToBeClickable(ab));
		
		/*driver.findElement(By.xpath("//input[@id='oneWayTrip']")).click();
		
		Alert a=driver.switchTo().alert();
		System.out.println(a.getText());
		Thread.sleep(500);*/
		
		
		

		
	}
}
