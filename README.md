# SDET-Glossary
 
*place main contents of your branch withing allocated headers
 
### OOP main glossary
 
### Ruby main glossary
 
### Testing main glossary
 
### Data main glossary

#### Json
JSON stands for JavaScript Object Notation(JSON), its primary use is to  transmit data between a web application and a server. They are lightweight text-based and human readable. It is incresinly popular as an alternative to XML. Calling from an API commonly returns JSON format information.

Data wtihin a JSON is displayed like so
```
var Tom = {
	"age" : "25",
	"hometown" : "Cool Town",
	"gender" : "male"
}
```
This creats an object that we access using the variable Tom 

A more complicated exmaple is storing two people within the one variable like so 
```
var family = [{
    "name" : "Jason",
    "age" : "24",
    "gender" : "male"
},
{
    "name" : "Kyle",
    "age" : "21",
    "gender" : "male"
}];
```
This way stores the two poeple in an array represented by the square brackets

### XML
XML data is known as self-desribing or self-defining, meaning that the struture of the data is embededded with the data arrives there is no need to pre-build the structure to store the data. The basic building block of an XML document is an element, defined by tags. An element has beginning and an ending tag. As shown below

```
<?xml version="1.0" standalone="yes"?>

<conversation>

<greeting>Hello, world!</greeting>

<response>Stop the planet, I want to get off!</response>

</conversation>
```
XML's power resides in its complicty. It can take large chunks of information and consolidate them into an XML document.






