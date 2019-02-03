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

 
