Project Name - TRL - Sample project for automating user journeys

Created by - Rashmi Kulkarni using Selenium, Java, Mavem & TestNG in Chrome browser on Mac

The project structure was created using Maven and all the dependencies can be found in POM.xml
Test case execution order is defined in TestNG.xml as per logical order of the functionality

Below are the details of the folder structure - 
Src/main/Resources package - Below are its contents - 
-----------------------------------------------------
-It has a Base class which has all the reusable methods
-It has two class created to write and read json data. This has been executed
 independently to populate json data as a pre-requisite for car make and model selection
 This data is stored in data.json
-It also has data.properties which is used for parameterising browser, url, username
 and password.
-It has log4j.xml configuration file to extract logs

Src/main/PageObjects package - Below are its contents - 
-------------------------------------------------------
-These classes have all the objects and methods based on pages
-LandingPage - Has all the object/methods in scope for this project for landing page
-LoginPage - Has all the object/methods in scope for this project for login page
-HomePage - Has all the object/methods in scope for this project for Home page
-carSelectionPage - Has all the object/methods in scope for this project for the page
                    where car makes and models are selected
-myGaragePage - Has all the object/methods in scope for this project for the page
                    where watchlist is displayed
Src/test/WishList Package - Below are its contents -
----------------------------------------------------
This package has all the tests. The test can be executed either independently or through 
TestNG.xml which is integrated in POM.xml. So these tests can be run directly from command prompt as a suit or through Jenkins by creating a job and integrating mvn command.
-fullTest - covers full end to end test
-Listeners - covers methods to take screen shots when test fails
-testCase1Login - covers test for login functionality
-testCase2SelectMakeAndModel - covers test to select car make and model
-testCase3AddToWatchList - covers test to add to watchlist functionality
-testCase4RemoveFromWatchList - covers test to remove from watchlist functionality
-testCase5SortCarList - covers test to sort

Area of improvement
-------------------
1) Considering this is a proof of concept for framework building, the scope of this project is to add only 1 car. Tests can be improvised to handle adding of multiple cars which has been taken care for removal of multiple car
2) For few of the locators relative xpaths could have been given which is time consuming instead of absolute xpath.
3) HTML report can also be generated




