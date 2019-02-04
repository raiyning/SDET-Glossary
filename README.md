# SDET-Glossary

*place main contents of your branch withing allocated headers
 
### OOP main glossary

### Abstraction

Abstraction is one of the key concepts of object-oriented programming. In abstraction, the programmer hides all the irrelevant data about an object in order to reduce complexity and increase efficiency—hiding the implementation details while presenting the essential features to the user. An example of abstraction can be given with a database system. The user does not know how the data is stored and how the data is maintained to a very technical degree. The complexities are hidden from the user; only that which is essential is exposed.

### Encapsulation

Similar to abstraction, encapsulation also hides data, but this time, for the purpose of protection. Encapsulation binds data and functions that manipulate that data into a single unit such as a class (which is a model of objects). For example, in ruby, encapsulation can make methods and variables private within a class which prevents other classes from accessing them (unless they are made public), therefore, preventing the unauthorised use of them. Only the object's methods can directly manipulate or inspect its fields.

### Inheritance 

Inheritance is the idea of getting or inheriting features from a parent. This concept is essential in object-oriented programming. In OOP this means that a child class (or subclass) can inherit features from a parent class (super class). The child class inherits attributes and methods from the parent class. This enables the child class (subclass) to define new attributes and methods which are then applied to those that were inherited. In other words, what has been inherited can be overridden in the child class and new logic can be created.

### Polymorphism 

Poly is the Greek word for many; morph in the Greek means forms—so polymorphism means the ability to be many forms. In OOP polymorphism refers to the ability of a variable, function or object to take on many forms. Polymorphism incorporates inheritance due to the fact that classes that inherited from the  same parent class (super class) may contain methods (or functions) bearing the same name—but when executed, exhibit different behaviours. 

# Instance Variables

## Objectives

1. Define instance variables.
2. Distinguish instance variables from local variables
3. Describe how instance variables give objects attributes and properties

## Defining instance variables
* Instance variable are variables that leave through the instance of a class. declaring an instance variable in a method that belongs to a calss would make that variable useble in all other meethods that belong to that intstace of the class. We declare instance variable by adding ```@``` at the beggening of the variable name

## Distinguishing instace variables from local variables
* A variable is a way to pass data for instance ```test = "something"``` in this we set a new variable called ```test``` and its value is ```"something"```. Using the ```" "``` sign means the value is in the form of string. This way we passed values/data through variables. 
* When using this form of declaration it would be a local variable. Declaring it in a method means it is only acessible in that method of the class.
```
class TestClass
  def test_method
    duck = "test"
  end

  def test_method_two
    duck2 = duck
  end
end
```
* consider the two methods are present in a class. If someone were to instantiate the class ```test = TestClass.new``` and then run ```test.test_method``` then ```test.test_method_two``` the user would get an error ```undefined local variable duck``` . This happens because ```duck``` only exists in the first method.

* On the other hand if the variable was to be instantiated with ```@duck = "test"``` it would live throughout the whole instance. 
```
class TestClass
  def test_method
    @duck = "test"
  end

  def test_method_two
    duck2 = @duck
  end
end
```
If you were to look at the first example and replace ```duck``` with ```@duck``` then running the methods would result ```duck2 to be equal to "test"```

## Describe how instance variables give objects attributes and properties
* We use instance variables to pass atributes that are created in a different method and applied them in others.

## Classes and Modules
### What is a Class?
A class is defined inside a file. A class is a group of methods and attributes that share commonalities.

### What is a Module?
A module is a modular part of programming which can be called by classes in order to keep code DRY. This typically happens when many classes have the same method which does the same thing.

#### Glossary
DRY - Don't Repeat Yourself

### Ruby main glossary

 ### DataTypes
  Data types in Ruby represents different types of data like text, string, numbers, etc. All data types are based on classes because it is a Object-Oriented language. There are different data types in Ruby as follows:

                  Numbers
                  Boolean
                  Strings
                  Hashes
                  Arrays
                  Symbols

  #### Numbers:
   Generally a number is defined as a series of digits and by using a dot as a decimal mark. There are different kinds of numbers like integers and float.

      E.g. Integer = 3, 30, 300, 3000
          Float = 1.2, 1.23, 1.234, 1.2345

  #### Boolean:
   Boolean data type represents only one bit of information either true(1) or false(0).


      E.g.  if true
              puts "It is True!"
            else
              puts "It is False!"
            end

  #### Strings: 
  A string is a group of letters that represent a sentence or a word. Strings are defined by enclosing a text within a single (”) or double (“”) quotes. You can use both double quotes and single quotes to create strings.

      E.g. puts "String Data Type"

  #### Hashes: 
  A hash assign its values to its key. Value to a key is assigned by => sign. A key pair is separated with a comma between them and all the pairs are enclosed within curly braces.

      E.g. hash = colors = { "red" => 0xf00, "green" => 0x0f0, "blue" => 0x00f }

  #### Arrays: 
  An array stores data or list of data. It can contain all types of data. Data in an array are separated by comma in between them and are enclosed within square bracket.The position of elements in an array starts with 0. 

      E.g.  ary = ["fred", 10, 3.14, "This is a string", "last element"]


#### Symbols :

  A Symbol is basically the same as a String, but with one important difference. A Symbol is immutable. They are usually generated by using :name literal syntax

#### MVC
The Model-View-Controller (MVC) is an architectural pattern that separates an application into three main logical components: the model, the view, and the controller. Each of these components are built to handle specific development aspects of an application. MVC is one of the most frequently used industry-standard web development framework to create scalable and extensible projects.

![Image description](https://danielmiessler.com/images/MVC1.png)

Model -
The Model component corresponds to all the data-related logic that the user works with. This can represent either the data that is being transferred between the View and Controller components or any other business logic-related data. For example, a Customer object will retrieve the customer information from the database, manipulate it and update it data back to the database or use it to render data.

View -
The View component is used for all the UI logic of the application. For example, the Customer view will include all the UI components such as text boxes, dropdowns, etc. that the final user interacts with.

Controller -
Controllers act as an interface between Model and View components to process all the business logic and incoming requests, manipulate data using the Model component and interact with the Views to render the final output. For example, the Customer controller will handle all the interactions and inputs from the Customer View and update the database using the Customer Model. The same controller will be used to view the Customer data.
 
#### GEMS

Gem is a ruby software package which offers specific functionalities to programs that run ruby. For example, if you want to have a function that lets you authenticate within your program so you don't always need to write one out, you can get it in form of a gem to put within the program. Gems are stored in a file called in Ruby Gemfile. This file has to be located in the root of the project in order for the gems to run.

##### HTTParty

HTTParty is a gem you can use in Ruby to help call an external API through the use of request methods, such as GET, POST, PUT and DELETE. Through the use of the HTTParty gem, it helps to expose the module and encapsulate all of the methods from that specific module to help with calling the external API through the different request methods. 

##### Dotenv

Dotenv helps to load enviromental variables from an .env file into a specific file by calling it within the methods. If you want more information on this, click on the following link: https://github.com/bkeepers/dotenv

##### JSON

JSON gem helps provide the methods to use within your class in your project, so that you can easily parse through external API's into a json format. 

### Testing main glossary

### ISTQB

### Testing Tools

### Glossary Terms 

Test tool - a software product that supports one or more test activities such as planning and control, specification, building initial files and data, test execution and test analysis

Incident management tools/Defect management tools:
- Used to perform two critical activities: creation of an incident report and maintenance of the details about the incident as it progresses through the incident life cycle
- Use a database to store/manage details of incidents. This allows the incident to be categorised according to values stored in the appropriate fields.

Requirement management tools:
- Used by BAs to record, manage and priorities the requirements of a system. 
- Use of a traceability function enables links and references to be made between requirements, functions, test conditions and other testware items so as requirements change it is easy to identify which other items may need to change. 

Configuration management tools:
- Designed primarily for managing the versions of different software and hardware components that compromise a complete build of the system. 
- Allows traceability between testware and builds of an integrated system and versions of subsystems and modules. This is useful for identifying the correct version of test procedures, determining which test procedures can be reused or need to be updated/maintained and tracing back to previous versions for debugging purposes

Review tools:
- Provide a framework for reviews or inspections, this can include:
 - Maintaining information about the review process such as rules and checklists
 - The ability to record, communication and retain review comments/defects
 - The ability to amend the deliverable under review while retaining a log of the changes made
 - Traceability functions

Static analysis tools:
- Analyse code before it is executed in order to identify defects as early as possible, so therefore are mainly used by developers prior to unit testing
- Medium/large changes to existing code requires the use of a static analysis tool
- Used to enforce programming standards, improve the understanding of code and to calculate complexity and other metrics

Modelling tools:
- Used primarily by developers during the analysis and design stages of the SDLC
- Very cost effective at finding defects as early as possible in the SDLC
- Allow omissions and inconsistencies to be identified and fixed early so that detailed design/programming can begin from a consistent and robust model - this in turn prevents fault multiplication

Test design tools:
- Used to support the generation and creation of test cases
- In order for the tool to generate test cases, a test basis needs to be input and maintained

Test data preparation tools:
- Used by testers and developers to manipulate data so that the environment is in the appropriate state for the test to be run
- This can involve making changes to the field values in DBs, data files etc. and populating files with a spread of data

Test comparators:
- Compare the contents of files, DBs, XML messages, objects and other electronic data formats.
- Allows expected results and actual results to be compared so that differences can be highlighted which provides assistance to developers when localising and debugging code

Test execution tools:
- Allows test scripts to be run automatically (or at least semi-automatically)
- A test script is used to navigate through the system under test and compare predefined expected outcomes with actual outcomes
- The results are then written to a test log

Test harnesses/Unit test framework tools:
- Used primarily by developers to simulate a small section of the environment in which the software will operate
- Usually written by in-house developers to perform component or integration testing for a specific purpose
- Use stubs and drivers 

Dynamic analysis tools:
- Used to detect the type of defects that are difficult to find during static testing
- Typically used by developers during component testing and component integration testing
- Generally used for safety-critical and other high risk software where reliabilty is critical

The pilot project:
- Aims of the project include the following:
 - To establish what changes need to be made to the high-level processes and practices currently used within the test organisation
 - To determine the lower level detail such as templates, naming standards and other guidelines for using the tool - this can take the form of a user guidelines document
 - To establish whether the tool provides value for money - this is done by trying to estimate and quantify the financial benefits of using the tool
 - To learn about what the tool can and cannot do and how these functions can be applied with the test organisation to obtain the maximum benefit

- A pilot project should report back to the stakeholders that determined the requirements of the tool

 ### Testing Principles 
  1. Testing shows the presence of bugs 
  * Running a test through a software system can only show that one or more defects exist
  * Testing cannot show that the software is error free
  2. Exhaustive testing is impossible 
  * This is a testing approach in which all possible data combinations are used. This includes implicit data combinations present in the state of the software/data at the start of testing
  3. Early testing 
  * The earlier a problem (defect) is found, the less it costs to fix
  4. Defect clustering 
  * It is often a small number of modules that exhibit the majority of the problems
  * This is the application of the Pareto principle to software testing: approximately 80 percent of the problems are found in 20 percent of the modules
  5. The pesticide paradox 
  * Running the same set of the tests continually will not continue to find new defects 
  6. Testing is context dependent 
  * Different testing is necessary in different circumstances
  * Risk can be a large factor in determining the type of testing that is needed
  7. Absence of errors fallacy 
  * Software with no known errors is not necessarily ready to be shipped
 
### FTP (Fundamental test process)
#### Test planning and control
  - Determining your exit criteria 
  - Determine what is going to be tested 
  - Who is doing the testing 
  - How it will be achieved 
  - How it is going to be tested 
  - what should be done when the activities do not match with plans 
#### Test analysis and design 
  - Test base is reviewed 
  - Test conditions, cases and procedures 
  - Fine detail of what to test 
  - Designing tests including priority 
#### Test implementation and execution 
  - Most visible part of testing 
  - Prioritising test cases 
  - creating test suites from collected test cases 
  - Log testing activities and defects 
  - Running tests 
  - Comparing actual results with expected results
  - repeate test activities when changes have been made 
#### Evaluating exit criteria and reporting 
  - Has the criteria been met?
  - Does the system do as expected?
  - Determine if more tests need to be made?
  - Is the system ready to be released?
  - Writing up results of the testing 
#### Test closure activities
  - Making sure documents are up to date 
  - Passing over testware to maintenance teams
  - Lessons learned 
  
 ### What is a Review
* A review is a systematic examination of a document by one or more people with the aim of finding and removing errors

### Activities of a formal review 
#### Planning 
* Defining the review criteria 
* Selecting the personnel
* Allocating roles
* Defining the entry and exit criteria 
* Selecting the parts of the documents to be reviewed 
* Checking entry criteria
#### Kick-off
* Distributing documents 
* Explaining the objectives 
#### Individual preparation
* Preparing for the review 
* Noting potential defects 
#### Review meeting 
* Discussing or logging with documented results
* Noting defects 
* Examining/evaluating and recording issues
#### Rework
* Fixing defects found
* recording updated status of defects
#### Follow-up 
* Checking the defects have been addressed 
* Metrics
* Checking on exit criteria

### Roles in a formal review
#### Manager
* Decides on the execution of the reviews
* Determines whether the review process objectives have been met
#### Moderator
* Plans the review
* Chooses participants 
* Conducts meeting
* Performs follow up
#### Author
* Writer or person with the chief responsibility for the development of the document(s) to be reviewed
#### Reviewers
* Have specific technical or business background
* Identify and describe findings 
#### Scribe
* Documents all the issues and points made during the meeting

### Levels of formality 

#### Informal
* No formal process
* Not usually documented 
* Inexpensive way to achieve limited benefits
* Maybe implemented as pair programming
#### Walkthrough
* Led by the author of the document 
* Can be very open ended and may very from quite informal to formal
#### Technical Review 
* Usually performed as a peer review
#### Inspection
* Led by trained moderator
* Process is formal 
* Pre-meeting preparation is essential
* Inspection report is produced
* Follow up process is used
* Main purpose is to find defects


#### Life Cycles

Development life cycle – involves capturing the initial requirements from the customer, expanding on these to provide the detail required for code production, writing the code and testing the product, ready for release

Verification - checks the work-product meets the requirements set out for it e.g. ensuring a website built follows the guidelines for making websites usabale by as many people as possible. Ensures we are building the product in the RIGHT WAY.

Validation - focuses on the evaluation of the work-product against user needs e.g. ensuring the behaviour of the work-product matches the customer needs as defined for the project. An example of this is that a website built is also intended for novice users. Validation would include these users checking that they too can use the website easily. Validation ensures we are building the RIGHT PRODUCT as far as the users are concerned.

Waterfall/Linear/Sequential Model:
- Shows the steps in sequence where the requirements are progressively refined to the point where coding can take place.
- Each activity is completed before moving on to the next
- Testing is carried out once the code has been fully developed and then a decision is made whether the product can be released

![alt text](https://www.softwaretestinggenius.com/wp-content/uploads/2018/07/ISBF2.jpg "Logo Title Text 1")

V-Model/Sequential development model:

The left hand side of the model focuses on elaborating the initial requirement, providing successively more technical detail as development progresses. 

In the model these are:
 - Requirement specification
 - Functional specification
 - Technical specification
 - Program specification

These specifications could be reviewed to check the following:
 - Conformance to the previous work product 
 - That there is sufficient detail for the subsequent work product to be built correctly
 - That it is testable

The middle of the V-Model shows that planning for testing should start with each work-product

The right hand side focuses on testing activities e.g. for each work-product a testing activity is identified. 

In the model these are:
 - Testing against the requirement spec takes place at the acceptance testing stage
 - Testing against the functional spec takes place at the system testing stage
 - Testing against the technical spec takes place at the integration testing stage
 - Testing against the program spec takes place at the unit testing stage

This model allows testing to be concentrated on the detail provided in each work-product so that defects can be identified as early as possible.

![alt text](https://www.softwaretestinggenius.com/wp-content/uploads/2018/07/ISBF5A6.jpg "Logo Title Text 1")


Iterative-incremental development models:

Requirements do not need to be fully defined before coding can start. Instead a working version of the product is built in a series of iterations. Each stage encompasses requirements definition, design, code and test. 

Iterative/Cyclical development have defined time scales and cost. Within this, cycles will be defined - these are referred to as time-boxes. For each time-box a requirement is defined and a version of the code is produced. At the end of each time-box a decision is made on what extra functionality needs to be created for the next iteration. This process is repeated until a fully working system is produced. 

A key feature is the involvement of the user reps in the testing. This minimises the risk of developing an unsatisfactory product. The user reps are empowered to request changes to the software to meet their needs.

![alt text](https://www.softwaretestinggenius.com/wp-content/uploads/2018/07/ISBF5B7.jpg "Logo Title Text 1")

#### Specification
Specification tests are derived from the specifications. The tester concentrates on what the software does and **does not** run the code to perform the tests. 

ISTQB Definition: *A procedure to derive and/or select test cases based on an analysis of the specification, either functional or non-functional, of a component or system without reference to its internal structure.*


Overall, these are the types of tests:

| Specification | Structure | Experience | Maintenance |
| --- | --- | --- | --- |
| Black box | Control flow diagram | Error guessing | Statement coverage |
| Equivalence partioning | Statement coverage | Exploratory guessing | |
| Boundary Value Analysis | Decision coverage | | |
| Decision Tables | Path coverage
| Use cases |
 
### Data main glossary

