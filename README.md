
# Automation Approach

## Required gems 

source 'http://rubygems.org'

* gem 'cucumber'
* gem 'rspec'
* gem 'selenium-webdriver'
* gem 'require_all'

## Framework approach

Framework is created using pageobject model below is the folder structure

* features:  cucumber features will be added to this folder
* features/step_definitions:  step definitions related to feature files will be added to this folder
* support: utilities and base driver initialization files are added to this folder
* pages: each file in this folder represents a page/section on web application and has all the elements and actions related to the page
* config: cucumber.yaml added to this folder which contains default cucumber commandline arguments
* reports: folder to store sample reports
* report.html: html reporting file with test run information

## Running tests

* we can run tests using below command
  
   cucumber BROWSER=chrome URL=https://farmdrop.com/

* we can pass browser and url parameters from commandline

## Running tests on different browsers

* we can run tests on different browsers and different environments by passing browser and url as parameters to 'cucumber' [and we can use these comands with different parameters to create CI builds]

Example:
 
 Running tests on Chrome in Dev environment:  cucumber BROWSER=chrome URL=https://dev.farmdrop.com/
 Running tests on firefox in UAT environment: cucumber BROWSER=firefox URL=https://uat.farmdrop.com/


## Reporting

* cucumber reporting is used to generate html test reports and when we run tests by default reports will be stored in report.html in root folder [sample html reports can be found in reports folder]
