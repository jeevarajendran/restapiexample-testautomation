Project structure
-----------------

    src
    |
    |_ _ test
            |
            |_ _ java
                    |
                    |_ _ RestAPITest : Test class to test the api http://dummy.restapiexample.com/
            |
            |_ _ resources
                         |
                         |_ _ CreateEmployeeJSONRequest : JSON request payload to create an employee
                              UpdateEmployeeJSONRequest : JSON request payload to update an employee's salary
    pom.xml
          |
          |_ _ This file contains the dependencies for the project


How to run the tests
--------------------

    Step 1 :
    - Download the project ‘restapiexample-testautomation’ into a local folder

    Step 2 ( one of the following) :

    1. TestNG : Using TestNG runner through IDE (IntelliJ)
        - Open the project in IntelliJ as a maven project
        - Right click on pom.xml file -> maven -> import/Reimport
        - Create a run configuration in IntelliJ for the TestNG test runner as follows :
            - Name : RestAPITestRunner (Note : any name for the run configuration)
            - Class : RestAPITest
            - Working directory : $MODULE_WORKING_DIR$
            - Use classpath of module : restapiexample-testautomation (Note : usually this will be populated by default)
            - JRE : 1.8 (Note : usually this will be populated by default)
        - Run the configuration

    2. Command line ( Maven )
        - Open command prompt and navigate to the project location restapiexample-testautomation in the local directory
        - Run the following command :
            mvn test

        - Sample output
            [INFO] -----------< com.jeevarajendran.test:restapiexample-testautomation >-----------
            [INFO] Building restapiexample-testautomation 1.0-SNAPSHOT
            [INFO] --------------------------------[ jar ]---------------------------------
            [INFO]
            [INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ restapiexample-testautomation ---
            [WARNING] Using platform encoding (Cp1252 actually) to copy filtered resources, i.e. build is platform dependent!
            [INFO] Copying 0 resource
            [INFO]
            [INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ restapiexample-testautomation ---
            [INFO] Nothing to compile - all classes are up to date
            [INFO]
            [INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ restapiexample-testautomation ---
            [WARNING] Using platform encoding (Cp1252 actually) to copy filtered resources, i.e. build is platform dependent!
            [INFO] Copying 2 resources
            [INFO]
            [INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ restapiexample-testautomation ---
            [INFO] Nothing to compile - all classes are up to date
            [INFO]
            [INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ restapiexample-testautomation ---

            -------------------------------------------------------
             T E S T S
            -------------------------------------------------------
            Running RestAPITest
            Configuring TestNG with: org.apache.maven.surefire.testng.conf.TestNG652Configurator@368239c8
            log4j:WARN No appenders could be found for logger (org.apache.http.client.protocol.RequestAddCookies).
            log4j:WARN Please initialize the log4j system properly.
            log4j:WARN See http://logging.apache.org/log4j/1.2/faq.html#noconfig for more info.

            Created Employee record : {"id":"48512","employee_name":"TestUser-RestAPI","employee_salary":"1000","employee_age":"25","profile_image":""}
            Updated Employee record : {"id":"48512","employee_name":"TestUser-RestAPI","employee_salary":"1000","employee_age":"25","profile_image":""}
            Returning NULL as the employee does not exist in the database
            Employee record deleted successfully!

            Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 3.88 sec

            Results :

            Tests run: 1, Failures: 0, Errors: 0, Skipped: 0

            [INFO] ------------------------------------------------------------------------
            [INFO] BUILD SUCCESS
            [INFO] ------------------------------------------------------------------------
            [INFO] Total time:  6.693 s
            [INFO] Finished at: 2019-08-09T20:56:49+01:00
            [INFO] ------------------------------------------------------------------------

