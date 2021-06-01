## Note
```
Every web page is a XML document and consists of tags and attributes so using xpath we can query the document
```
## Syntax
```
1) / -> starts from the root node     
2) //-> searches for the perfect match

//tagname[@attribute='value'][occurances]
can aslo use parent in xpath
//input[@text='test1 test2']//parent:://td[@class='datalistrow']
can also use preceeding sibiling

can append more xpath 
e.g //button[@class='style-scope yt-icon-button'] [@id='button']

```
## Types
```
1)Relative Xpath direct call
2)Absolute Xpath traverse from root 
```
##Functions
```
contains()
 used when the value of attribute changes dynamically e.g //tagname[contains(@attribute,'value')] 
 
starts-with()
 used when the value of the attribute changes when the page got refereshed or any operation done on the webpage
 e.g //tagname[starts-with(@attribute='value')]
 
text()
 used to find the exact text e.g //tagname[text()='value']
```
## Operator
```
Or operator
xpath1 | xpath2
```
## Locating elements relative to know element
```
1)locating parent element
syntax //<knownxpath>/parent::elementName
eg: //tagname[@attribute='value']/parent::form

2)Locating a child element
syntax://<knownxpath>/child::<elementName>

3)Locating ancestors of a known element
//<knownxpath>/ancestor::<elementname>

4)Locating following elements 
//<knownxpath>/following::<elementname>

5)Locating by preceding element 
//<knownxpath>/preceding::<element>

6)Locating by following-sibiling::
//<knownxpath>/following-sibiling::<elementname>

7)Locating by preceeding sibiling 
//<knownxpath>/preceding-sibiling::<elementname>
```



