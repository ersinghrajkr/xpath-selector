# Advance XPath Tutorial (Automate -> [http://the-internet.herokuapp.com/]() )


Single forward Slash( / ) => coming down step by step from to destination element i.e Absolute Xpath

Double forward Slash ( // ) => It will jump directly to element   i.e Relative Xpath




## XPath Syntax and Functions

#### **Xpath for SVG Element - [local-name()='svg'] (chrome devtool doesn't support'):**

***[https://developer.mozilla.org/en-US/docs/Web/SVG/Element/svg]()***

//*[local-name()='svg'][@class='icon'][1]

//*[local-name()='svg'][@class='icon'][1]/ancestor::button[@id='mdn-cta-close']

//*[local-name()='svg'][@id='mdn-docs-logo'][1]


#### Xpath for SVG path Element - [name()='path']:

[https://www.w3schools.com/graphics/svg_path.asp]()

//*[name()='path'][contains(@d, 'M150')]

//*[name()='path'][contains(@d,'M150 0 L75 200 L225 200 Z')]

//*[name()='path'][@id='lineAB']

//*[name()='path'][@id='lineBC']

//*[name()='path'][@stroke='green']

//*[name()='path'][@stroke='blue' and contains(@d, 'M 100 350 q')]


#### Shadow-Dom (Normal Xpath doesn't work here') - [http://the-internet.herokuapp.com/shadowdom]() :

(//span)[1]

(//li)[1]

(//li)[2]


#### **Absolute Xpath**:    /tageName =>

/html/body/div[2]/div[1]/h1[position()=1]


/html/body/div[2]/div[1]/h1[text()='Welcome to the-internet']

/html/body/div[2]/div[1]/h1[contains(text(),'Welcome to the-internet')]

/html/body/div[2]/div[1]/h1[starts-with(text(),'Welcome to the-internet')]

/html/body/div[2]/div[1]/h1[substring-after(text(),'Welcome to the-interne')]  => t

/html/body/div[2]/div[1]/h1[substring-before(text(),'elcome to the-internet')]  => W


/html/body/div[2]/div[1]/h1[@class='heading']

/html/body/div[2]/div[1]/h1[contains(@class,'heading')]




#### **Relative Xpath**:        //**tagName**[*@**attrbuteName**="**attributeValue**"*]

//h1[position()=1]


//h1[text()='Welcome to the-internet']

//h1[contains(text(),'Welcome to the-internet')]

//h1[starts-with(text(),'Welcome to the-internet')]

//h1[substring-after(text(),'Welcome to the-interne')]  => t

//h1[substring-before(text(),'elcome to the-internet')]  => W


//h1[@class='heading']

//h1[contains(@class,'heading')]


#### Normalize-Space :        //**tagName**[n**ormalize-space**="**textValue**"]

/html/body/div[2]/div[1]/h1[contains(normalize-space(),'Welcome to the-internet')]

//h1[contains(normalize-space(),'Welcome to the-internet')]


#### **And functions  =>**

//h1**[contains**(@class,'heading') **and** text()='Welcome to the-internet'**]**

//h1[**@class**='heading' and **text()=**'Welcome to the-internet']


#### **Or functions  =>**

//h1[@class='heading' **or** text()='Welcome to the-internet']


#### **text()  =>** 

//h1[**text()**='Welcome to the-internet']

//h1[contains(**text()**,'Welcome to the-internet')]

//h1[contains(normalize-space(),'Welcome to the-internet')]

//h1[starts-with(**text()**,'Welcome to the-internet')]

//h1[substring-after(**text()**,'Welcome to the-interne')]  => t

//h1[substring-before(**text()**,'elcome to the-internet')]  => W


#### **Index, Position, Last element etc:**

//h1[position()=1]


#### With Respect To Element(Parent/Ancestor) ( Find of "Available Examples" w.r.t ) => Common Parent

//h1[@class='heading']/ancestor::div//h2[text()='Available Examples']

//div[@id="content"]/ul/li[3]/ancestor::div//ul/li[2]

//div[@id="content"]/ul/li[3]/a[text()='Basic Auth']/ancestor::div//ul/li[2]/a[@href='/basic_auth']

//div[@id="content"]/ul/li[3]/a[text()='Basic Auth']/ancestor::div//ul/li[2]/a[text()='Add/Remove Elements']



#### Xpath without Axes:


#### Platform To Right Xpath

Chrome DevTool

Chrome Console(Dollar x)
