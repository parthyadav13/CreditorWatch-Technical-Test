# Cerditor Watch TechnicalTest
Project Submission for Technical Test
I have tried to complete all the requried task as much as possible.
Following are the task list with my comments and details about what I did to accomplish the task:

1. Automation Framework    : I have used Cucumber with Junit to automate given scenarios in BDD approach.
2. Programming Language    : Java(as suggested).
3. Design Pattern          : I have used Page Factory to create Object repository to achieve Page Object Model. I have also create seprate test classes to perform desired                                    operations on that page seperately and calling methods of these classes in step defination to have data abstraction, so that step definations are                                not modified while modifing testcases.  
4. Configuration file      : I have used property file to store browser informations(like browers, drivers and browser timOut), application url and json input and output file                                locations. 
5. Buid Management Tool    : Maven.
6. Output of Test Execution: Output of test execution is in JSON format(/TechnicalTestCucumber/target/jsonReports)
7. Source Code Upload      : GitHub
8. Instruction Readme file : Instructions to run are below this task list. 
9 Negetive Scenarios       : I has not able to include any negetive scenarios because of the time constraints, however I have included 2 testcases for Testcase1 as happy path                                includes 2 scenarios
                             a) When user selects gender from "Male", "Female" and "Do not Disclose"
                             b) When user selects gender = "Custom"
                             
                        
# Instruction to run test cases

Testcases can be run from:
1. Test Runner   - /TechnicalTestCucumber/src/test/java/cucumberOptions/TestRunner.java
2. Command promt - After importing the project, testcases can be run from command promt. To run the test cases move from current directory to workspace to project                                directory ./TechnicalTestCucumber and run mvn commands.(mnv verify is required to generate reports).
3. Jenkins     - (Let me know if you want to run through Github, I will make it private repository and configure the authorisations) Configure a Jenkins job to the given                      repository
                   1.(Source Code Management->repositories(Git)->url of repository(provide the url of this project)).
                   2. Under 'Build Triggers', tick 'Build when a change is pushed to Github'.
                   3.Save and build.
                   4.

# Details of Framework

1. TechnicalTestCucumber/src/main/java

    Page Object repository - pageObjects(contains all the webelements definations in PageFactory Model and methods to pass webelements to test classes)
                           - I have used xpath as a locator identifies to have uniformity in project but for some webelements using other identifiers was more suitable,                                      therefore, I have used other identifiers as well. As google uses dynamic webobjects, I have used "xpath-text()" to identify webelements.
    Utilities              - GlobalVariables(mothord to read and write in property file)
                           - Base(mothods to initialise driver and getting values from GlobalVariable)
                           
2. TechnicalTestCucumbersrc/test/java

    testPages              - Contains classes were all test cases related to particular webpage are written in test methods. Methods of these classes will be called in step                                definations to finally run test cases based on feature file scenarios. Json input is passed in these test classes.  
    testInputPOGO          - Contain POGO classes to perform serialisation and deserialisation of Json input. I have directly passed the input into test classes but it could                              be enhanced by using Array<List> to parameterise the inputs for multiple test data( was not able to achieve this because of limited time to                                    complete the all tasks)

