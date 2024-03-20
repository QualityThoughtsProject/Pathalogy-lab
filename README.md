Writing Test Scenarios and Test Cases:

Login Page:

Scenario 1: Verify successful login with valid credentials.
Scenario 2: Verify error message for invalid credentials.
Scenario 3: Verify redirection to the home page after successful login.
Home Page:

Scenario 1: Verify the presence of todos list after login.
Scenario 2: Verify navigation to the Cost Calculator for blood tests.
Scenario 3: Verify logout functionality.
Cost Calculator for Blood Test:

Scenario 1: Verify calculation of the cost for selected blood tests.
Scenario 2: Verify application of discounts.
Scenario 3: Verify reset functionality.
Adding Patients and Creating Tests:

Scenario 1: Verify successful addition of patient details.
Scenario 2: Verify successful creation of test requests.
Scenario 3: Verify reflection of added test in the todos list.


import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.By;
import org.openqa.selenium.WebElement;

public class LoginPageTest {
    public static void main(String[] args) {
        System.setProperty("webdriver.chrome.driver", "path/to/chromedriver");
        WebDriver driver = new ChromeDriver();
        driver.get("https://gor-pathology.web.app/");
        ebElement usernameInput = driver.findElement(By.id("username"));
        usernameInput.sendKeys("test@kennect.io");
        WebElement passwordInput = driver.findElement(By.id("password"));
        passwordInput.sendKeys("Qwerty@1234");
        WebElement loginButton = driver.findElement(By.xpath("//button[@type='submit']"));
        loginButton.click();
        WebElement todosList = driver.findElement(By.className("todos-list"));
        if (todosList.isDisplayed()) {
            System.out.println("Login successful!");
        } else {
            System.out.println("Login failed!");
        }
        driver.quit();
    }
}
