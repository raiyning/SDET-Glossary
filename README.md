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
This creates an object that we access using the variable Tom 

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


## API

API (Application Programming Interface) - a set of functions and procedures allowing the creation of applications that access the features or data of an operating system, application, or other service.

API Key -  a code passed in by computer programs calling an application programming interface to identify the calling program, its developer, or its user to the Web site.

Client - the initiating party that sends an API request. Often times there will be many clients consuming the same API.

Endpoint - the URI that goes after the base URL and points towards the requested API functionality.

Parameter - an argument sent to the API which helps define the request and expected response.

URI (Unique Resource Identifier) - a string of characters used to identify a resource on a computer network, of which the best known type is the web address or URL.

Status Code - HTTP status codes are what the server sends in the response back to the client with regards to the status of the request.

Versioning - Assinging a unique identifier to keep track of the state of the API. If changes are made to the API, the version should change.

GET - The HTTP method for retrieving resources from a RESTful API.

POST - The HTTP method for creating resources with a RESTful API.

PUT - The HTTP method for updating resources with a RESTful API.

DELETE - The HTTP method for deleting resources with a RESTful API.

