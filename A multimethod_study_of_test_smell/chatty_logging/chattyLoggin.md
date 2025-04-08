## Chatty Logging

```java
public class LoginTest {
    private WebDriver driver;

    @Before
    public void setUp() {
        driver = new ChromeDriver();
        driver.manage().window().maximize();
    }

    @After
    public void tearDown() {
        driver.quit();
    }

    @Test
    public void testValidLogin() {
        LoginPage loginPage = new LoginPage(driver);
        loginPage.enterUsername("testuser");
        loginPage.enterPassword("password");
        loginPage.clickLoginButton();

        String expectedUrl = "https://example.com/dashboard";
        String actualUrl = driver.getCurrentUrl();

        if (actualUrl.equals(expectedUrl)) {
            System.out.println("Login test passed.");
        } else {
            System.out.println("Login test failed. Expected URL: " + expectedUrl + ", Actual URL: " + actualUrl);
        }

        assertTrue(actualUrl.equals(expectedUrl));
    }
}