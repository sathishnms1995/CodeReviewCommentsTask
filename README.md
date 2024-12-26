# CodeReviewCommentsTask
Find all the review comments here:

Empty catch block found in scrollElement(String Locator) - Can be handled in other ways
Thread.sleep is used in scrollElement(String Locator), instead, explicit or fluent wait can be used
waitImplicitly() is set both in the constructor and other methods, its conflictiong. Better this can be used in driver initialization once
Hardcoded WAIT_TIME_SEC = 60.Instead this can be set in config and property files 
maximizeWindow() is unnecessary in the page object, can be done during the driver setup once
Hardcoded path to chromedriver.exe.- Can be used in config file
Basic ChromeDriver initialization - Use ChromeOptions for configurations like headless mode
Setup/teardown at suite level.-Use @BeforeTest and @AfterTest for better test isolation.
No error handling for initialization failures - Add exception handling
No null checks - Can add null checks as well
Hardcoded XPath in methods.- Use dynamic locators or store them in a config file
Too many @FindBy annotations in one class - Group in to small helper class
Typo in method name - Fix typos and maintain consistent names
Direct use of System.out.println- Instead log4j can be implemented
Generic method names like TestCase1 make the test flow unclear - Rename methods as per the actions
No assertions inside the test to validate outcomes - Add assertion to validate




