# SDET-Glossary

*place main contents of your branch withing allocated headers
 
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

