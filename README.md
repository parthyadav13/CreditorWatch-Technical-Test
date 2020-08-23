# Creditor Watch Technical Test 

Project Submission for Technical Test 

I have tried to complete all the required task as much as possible. 

Following are the task list with my comments and details about what I did to accomplish the task: 

  

1. Automation Framework    : I have used Cucumber with Junit to automate given scenarios in BDD approach. 

2. Programming Language    : Java(as suggested). 

3. Design Pattern          : I have used Page Factory to create Object repository to achieve Page Object Model. I have also created separate test classes to perform desired                                    operations on that page separately and calling methods of these classes in step definition to have data abstraction, so that step definitions are                                not modified while modifying testcases.   

4. Configuration file      : I have used property file to store browser information(like browsers, drivers and browser timeout), application url and json input and output file                                locations.  

5. Build Management Tool    : Maven. 

6. Output of Test Execution: Output of test execution is in JSON format(/TechnicalTestCucumber/target/jsonReports) 

7. Source Code Upload      : GitHub 

8. Instruction Readme file : Instructions to run are below this task list.  

9 Negative Scenarios       : I has not able to include any negative scenarios because of the time constraints, however I have included 2 testcases for Testcase1 as happy path                                includes 2 scenarios 

                             a) When user selects gender from "Male", "Female" and "Do not Disclose" 

                             b) When user selects gender = "Custom" 

                              

                         

# Instruction to run test cases 

  

Testcases can be run from: 

1. Test Runner   - /TechnicalTestCucumber/src/test/java/cucumberOptions/TestRunner.java 

2. Command prompt - After importing the project, testcases can be run from command prompt. To run the test cases, move from current directory to workspace to project                                directory ./TechnicalTestCucumber and run mvn commands.(mnv verify is required to generate reports). 

3. Jenkins     - (Let me know if you want to run through Github, I will make it private repository and configure the authorizations) Configure a Jenkins job to the given                      repository 

                   1.(Source Code Management->repositories (Git)->url of repository (provide the url of this project)). 

                   2. Under 'Build Triggers', tick 'Build when a change is pushed to Github'. 

                   3.Save and build. 

                   4. 

  

# Details of Framework 

  

1. TechnicalTestCucumber/src/main/java 

  

    Page Object repository - pageObjects(contains all the webelements definitions in PageFactory Model and methods to pass webelements to test classes) 

                           - I have used xpath as a locator identifies to have uniformity in project but for some webelements using other identifiers was more suitable,                                     therefore, I have used other identifiers as well. As google uses dynamic webobjects, I have used "xpath-text ()" to identify webelements. 

    Utilities              - GlobalVariables(method to read and write in property file) 

                           - Base(methods to initialize driver and getting values from GlobalVariable) 

                            

2. TechnicalTestCucumbersrc/test/java 

  

    testPages              - Contains classes were all test cases related to particular webpage are written in test methods. Methods of these classes will be called in step                                definitions to finally run test cases based on feature file scenarios. Json input is passed in these test classes.   

    testInputPOGO          - Contain POGO classes to perform serialization and deserialization of Json input. I have directly passed the input into test classes but it could                              be enhanced by using Array<List> to parameterize the inputs for multiple test data(was not able to achieve this because of limited time to                                    complete the all tasks) 

 

 