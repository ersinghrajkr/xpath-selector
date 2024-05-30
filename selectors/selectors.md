# Basic Locators in Web

### CSS ID

//input[@id='value']

//input[@id='first-name']

### Class Name -

//button[@class='value']

//button[@class='btn btn-lg btn-danger']

### Name Attribute

//tagname[@Attribute='Value']

//input[@placeholder='Enter first name']

### Tag Name

Xpath =//tagname[@Attribute=value]

//input[@placeholder='Enter first name']

### Link Text

### Partial Link Text

### XPath(Absolute & Relative)

**Absolute XPath** - Absolute XPath is the way of identifying an element starting from the root of the DOM. The XPath expression starts with **“/” **symbol.
for example - ***/html/body/div/div/div/main/div/div/div/select**

**Relative XPath -** Relative XPath is the way of identifying an element by using its attributes for querying and can also be used for its nearest elements. Relative XPath doesn’t start with a root node; hence, this way of writing XPath is always reliable. The Path expression starts with “//”

for example - **//form/input[3]**

#### **Using Attributes**

//select[@id='select-menu']/option[@value='1']

### Logical Operators ( or & and)

https://formy-project.herokuapp.com/form

//input[@type='radio' and contains(text(), 'High School')]

//input[@type='checkbox' and contains(text(), 'Male')]

//a[@role='button' and contains(normalize-space(),'Submit')]

//div/text()[normalize-space()='Prefer not to say']

*//input[@type='checkbox' and contains(normalize-space(), '         Male       ')]*

*//input[@type='checkbox' and contains(normalize-space(),'         Prefer not to say       ')]*

//input[@type='checkbox' and contains(normalize-space(translate(text(), '', ''), '        Male       ')]

**//input[contains(normalize-space(text()), 'Male')]**

#### **XPath Using text() function**

//button[@type='button' and text()='Success']

//button[text()='Danger' and @type='button']

### XPath using contains() function:

//button[contains(text(), 'Danger') and @type='button']

### XPath using starts-with() function

//input[starts-with(@id, 'first-n')]

### XPath using ends-with() function

//input[ends-with(@id, '-name')]

### DATA TABLES Xpath

[https://www.cricbuzz.com/cricket-series/7607/indian-premier-league-2024/points-table]()

//table[@class="table cb-srs-pnts"]/tbody/tr/td//div[text()='Royal Challengers Bengaluru']

//table[@class="table cb-srs-pnts"]/tbody/tr/td//div[contains(text(),'Bengalur')]

//table[@class="table cb-srs-pnts"]/tbody/tr/td//div[contains(text(),'Bengaluru')]/../../../../td[8]

//table[@id="customers"]/tbody/tr/td/span[text()='Mexico']/../../td[last()]

//table[@id="customers"]/tbody/tr/td/span[last()]/../../td[last()]

[https://www.techlistic.com/2017/02/automate-demo-web-table-with-selenium.html]()

//table[@id="customers"]/tbody/tr/td/span[text()='Microsoft']/../../td[3]

//table[@id="customers"]/tbody/tr/td/span[text()='Mexico']/../../td[last()]

//table[@id="customers"]/tbody/tr/td/span[last()]/../../td[last()]

//table[@id="customers"]/tbody/tr[last()]/td[last()] - Best way
