# **Apex_Trailhead Challenges**
##  **Challenge 1:**

***
##  **Challenge 2:  Create an Apex class with a method that returns an array ( or list) of strings**

#### * Create an Apex class with a method that returns an array ( or list) of formatted **_strings('Test0', 'Test1',..)_** 
#### * The length of the array is determined by an **_integer parameter_**
#### * The Apex class must be called StringArrayTest and be in the public scope
#### *  The apex class must have a public static method called **_generateStringArray_**
#### *  The **_generateStringArray_** method must return an array ( or list) of **_strings_**.
#### *  The method must accept an incoming Integer as a parameter, which will be used to determine the number of retuening strings
#### *  The method must return a string value in the format **_Testn _** where n is the index of the current dstring in the array

***


## **Challenge 3: Create a method for inserting accounts. ( Manipulate Records with DML)**

#### * To pass this challenge, create an **Apex class** that **inserts a new account** named after an incoming **_parameter_**.
#### If the account is successfully inserted, the method should **return** the account record. If a DML **exception** occurs, the method should **return _null_**.
#### * The Apex class must be called **_AccountHandler_** and be in the **public** scope
#### * The Apex class must have a **public static method** called **_insertNewAccount_**
#### * The method must accept an incoming **_string_ as a parameter**, which will be used to create the **Account name**
#### * The method must **insert the account** into the system and then **return** the record
#### * The method must also accept an **empty string**, **catch the failed DML and then return _null_**

***

## **Challenge 4: SOQL** 
```
Create an Apex class that returns contacts based on incoming parameters.
For this challenge, you will need to create a class that has a method accepting two strings. 
The method searches for contacts that have a last name matching the first string and a mailing postal code matching the second. 
It gets the ID and Name of those contacts and returns them.
The Apex class must be called ContactSearch and be in the public scope
The Apex class must have a public static method called searchForContacts
The method must accept two incoming strings as parameters
The method should then find any contact that has a last name matching the first string, and mailing postal code 
(API name: MailingPostalCode) matching the second string
The method should finally return a list of Contact records of type List that includes the ID and Name fields
```
***
## **Challenge 5: SOSL**

* #### Create an Apex class that returns both contacts and leads based on a parameter.
* #### To pass this challenge, create an Apex class that returns both contacts and leads that have first or last name matching the incoming parameter.
* #### The Apex class must be called ContactAndLeadSearch and be in the public scope
* #### The Apex class must have a public static method called searchContactsAndLeads
* #### The method should then find any contact or lead that matches the string as part of either the first or last name
* #### The method should finally use a return type of List<List< sObject>>
* #### NOTE: Because SOSL indexes data for searching, you must create a Contact record and Lead record before checking this challenge. Both records must have the 
* #### last name Smith. The challenge uses these records for the SOSL search

***

## Challenge 6:  Create an Apex trigger

#### Create an Apex trigger that sets an account’s Shipping Postal Code to match the Billing Postal Code if the Match Billing Address option is selected. Fire the trigger before inserting an account or updating an account.

#### Pre-Work:
#### Add a checkbox field to the Account object:

* #### Field Label: Match Billing Address
* #### Field Name: Match_Billing_Address
     Note: The resulting API Name should be Match_Billing_Address__c.
 #### Create an Apex trigger:
* #### Name: AccountAddressTrigger
* #### Object: Account
* #### Events: before insert and before update
* #### Condition: Match Billing Address is true
* #### Operation: set the Shipping Postal Code to match the Billing Postal Code 

***
## Challenge 7:
#### Create a Bulk Apex trigger
#### Create a bulkified Apex trigger that adds a follow-up task to an opportunity if its stage is Closed Won. Fire the Apex trigger after inserting or updating an opportunity.
#### Create an Apex trigger:
* #### Name: ClosedOpportunityTrigger
* #### Object: Opportunity
* #### Events: after insert and after update
* #### Condition: Stage is Closed Won
* #### Operation: Create a task:
* #### Subject: Follow Up Test Task
* #### WhatId: the opportunity ID (associates the task with the opportunity)
* #### Bulkify the Apex trigger so that it can insert or update 200 or more opportunities

***
## Challenge 8: unit test

#### Create a Unit Test for a Simple Apex Class
#### Create and install a simple Apex class to test if a date is within a proper range, and if not, returns a date that occurs at the end of the month within the range. You'll copy the code for the class from GitHub. Then write unit tests that achieve 100% code coverage.
* #### Create an Apex class:
   * #### Name: VerifyDate
   * #### Code: Copy from GitHub : https://github.com/developerforce/trailhead-code-samples/blob/master/VerifyDate.cls
* #### Place the unit tests in a separate test class:
    * #### Name: TestVerifyDate
    * #### Goal: 100% code coverage
    * #### Run your test class at least once

*** 
## Challenge 9: Create a Unit Test for a Simple Apex Trigger

#### Create and install a simple Apex trigger which blocks inserts and updates to any contact with a last name of 'INVALIDNAME'. You'll copy the code for the class from GitHub. Then write unit tests that achieve 100% code coverage.
#### Create an Apex trigger on the Contact object
 * ####  Name: RestrictContactByName
 * #### Code: Copy from GitHub
 *  #### Place the unit tests in a separate test class
* #### Name: TestRestrictContactByName
* #### Goal: 100% test coverage
* #### Run your test class at least once

*** 
## Challenge 11A : Set up Org unit with postman:
https://trailhead.salesforce.com/content/learn/projects/quick-start-connect-postman-to-salesforce/set-up-your-org
```
Get Your Trailhead Playground Username and Password
Let’s get started by opening your Trailhead Playground. Scroll to the bottom of this page and click Launch. If you see a tab in your org labeled Get Your Login Credentials, great! Skip ahead to step 1. Otherwise, from the App Launcher (), find and open Playground Starter and follow the steps.

Click the Get Your Login Credentials tab and take note of your username.
Click Reset My Password.
This sends an email to the address associated with your username.
Click the link in the email.
Enter a new password, confirm it, and click Change Password.
Save your username and password for use later in this project.

Set Up Cross-Origin Resource Sharing in Salesforce
Cross-Origin Resource Sharing (CORS) allows code running in a web browser to communicate with Salesforce from a specific origin. Let’s add the URL patterns for Postman.

In your Trailhead Playground, from Setup, enter cors in the Quick Find box and select CORS.
In the Allowed Origins List, click New.
Enter https://*.postman.com as the Origin URL Pattern.
Click Save.
Select CORS again.
Click New and enter https://*.postman.co (note the .co domain extension) as the Origin URL Pattern.
Click Save.
```
***
## Challenge 11 B: Set Up and Connect Postman
Sign Up for Postman and Create a Workspace
https://trailhead.salesforce.com/content/learn/projects/quick-start-connect-postman-to-salesforce/set-up-and-connect-postman

***
## Challenge 12: Use REST API
https://trailhead.salesforce.com/content/learn/modules/api_basics/api_basics_rest?trailmix_creator_id=lanfu2&trailmix_slug=lanis-trailmix

#### A REST resource is an abstraction of a piece of information or an action, such as a single data record, a collection of records, or a  query. Each resource in REST API is identified by a named Uniform Resource Identifier (URI) and is accessed using standard HTTP methods (HEAD, GET, POST, PATCH, DELETE). REST API is based on the usage of resources, their URIs, and the links between them.
```
You use a resource to interact with your Salesforce org. For example, you can:
Retrieve summary information about the API versions available to you.
Obtain detailed information about a Salesforce object, such as Account, User, or a custom object.
Perform a query or search.
Update or delete records.
A REST request consists of four components: a resource URI, an HTTP method, request headers, and a request body. Request headers specify metadata for the request. The request body specifies data for the request, when necessary. If there’s no data to specify, the body is omitted from the request.
```

#### Create a New Account Record with REST API
* ####  Create a new record in your accounts using REST API:
* ####  Name: Blackbeards Coconut Milk Emporium
* ####  Description: The finest coconut milk in the seven seas.
***
## Challenge 13 Import Accounts Using Bulk API and Postman
 https://trailhead.salesforce.com/content/learn/modules/api_basics/api_basics_bulk?trailmix_creator_id=lanfu2&trailmix_slug=lanis-trailmix
Import account records using Bulk API and Postman.
CSV File: bulkv2hocdata

***
## Challenge 14 Create a Formula Field
https://trailhead.salesforce.com/en/content/learn/modules/point_click_business_logic/formula_fields?trail_id=force_com_dev_beginner&trailmix_creator_id=lanfu2&trailmix_slug=lanis-trailmix

#### Create a formula field that calculates the number of days remaining before a contract expires.
* #### Create a custom field:
* #### Object: Contract
* #### Data Type: Formula
* #### Field Label: Days Remaining
* #### Field Name: Days_Remaining
* #### Formula Return Type: Number
* #### Formula: Calculate the number of days between the contract end date and today

***
## Challenge 15 Create a Rollup Summary Field

https://trailhead.salesforce.com/en/content/learn/modules/point_click_business_logic/roll_up_summary_fields?trail_id=force_com_dev_beginner&trailmix_creator_id=lanfu2&trailmix_slug=lanis-trailmix

#### Add a custom field to the standard account object to provide a rollup summary of the total expected revenue from all related opportunities.

#### Important: If you have Advanced Currency Management enabled in your Trailhead Playground, disable it for this Hands-On Challenge.
* #### Create a roll-up summary field on the Account object:
* #### Field Label: Potential Value
* #### Field Name: Potential_Value
* #### Calculate the total expected revenue of all the opportunities related to the accountCreate a Rollup Summary Field
* #### Add a custom field to the standard account object to provide a rollup summary of the total expected revenue from all related opportunities.
***

## Challenge 16 Create a Validation Rule
https://trailhead.salesforce.com/content/learn/modules/point_click_business_logic/validation_rules?trail_id=force_com_dev_beginner&trailmix_creator_id=lanfu2&trailmix_slug=lanis-trailmix
#### Create a validation rule that displays an error message and prevents a user from creating or updating a contact if two conditions are both true.
#### A validation rule can contain a formula or expression that evaluates the data in one or more fields and returns a value of “True” or “False.”
####  Validation rules can also include error messages to display to users when they enter invalid values based on specified criteria. Using these rules effectively contributes to quality data

Project: 
##### Create a validation rule:
* #### Rule Name: Contact_must_be_in_Account_ZIP_Code
* #### Operator: AND (return true if both conditions are true)
* #### Define two error conditions:
* #### The contact is associated with an account id
* #### Hint: Use the ISBLANK and NOT functions.
* #### The contact mailing zip code is different than the account shipping zip code
* #### Hint: Use the API names (MailingPostalCode and ShippingPostalCode) and the <> (Not Equal) operator.
* #### Enter an error message for the validation rule
***
## Challenge 17. Data modeling:
#### Project 1: Understand Custom & Standard Objects

```
Learning Objectives
After completing this unit, you’ll be able to:

Describe the perks of using objects on the Salesforce platform.
Explain the difference between standard objects and custom objects.
List the types of custom fields an object can have.
```
#### Build a custom Offer object:
When a homebuyer makes an offer to buy a property, the brokers at DreamHouse Realty need to track the details in Salesforce. Create a custom object they can use to record the offer amount and target close date for the sale. Use auto numbering to generate the name of each offer record.
#### Create a custom object
* #### Label: Offer
* #### Object Name: Offer
* #### Record Name: Offer Name
* #### Data Type: Auto Number
* #### Display Format: OF-{0000}
* #### Starting Number: 1
* #### Create a custom currency field on the Offer object
* #### Data Type: Currency
* #### Field Label: Offer Amount
* #### Field Name: Offer_Amount
Create a custom date field on the Offer object
* #### Data Type: Date
 * #### Field Label: Target Close Date
* #### Field Name: Target_Close_Date

#### Project 2: Create relationships for the Offer object
https://trailhead.salesforce.com/content/learn/modules/data_modeling/object_relationships?trailmix_creator_id=lanfu2&trailmix_slug=lanis-trailmix
##### The object you created for the previous challenge is pretty handy. Imagine how much more useful it would be if brokers could specify which client made an offer and which property the client wants to buy. Add two relationships to the Offer object so brokers can capture this data in Salesforce. Create a Master-Detail relationship with the Property object and a Lookup relationship with the Contact object.


#### Challenge Requirements:
### Create a custom Master-Detail field on the Offer object
#### Data Type: Master-Detail
#### Field Label: Property
####  Field Name: Property
### Create a custom Lookup field on the Offer object
#### Data Type: Lookup
#### Field Label: Contact
#### Field Name: Contact

#### Project 3: Use Schema Builder to create a custom field for the Property object
https://trailhead.salesforce.com/content/learn/modules/data_modeling/schema_builder?trailmix_creator_id=lanfu2&trailmix_slug=lanis-trailmix

#### DreamHouse brokers often visit properties with their clients. They want to see on the property record where the property is located.
##### Use Schema Builder to add a street address field to the Property object.
* #### Data Type: Text Area
* #### Field Label: Street Address
* #### Field Name: Street_Address
* #### Always require a value in this field in order to save a record: Selected
*** 

## Challenge 18. Data management:
#### Project 1: Import Data
(https://trailhead.salesforce.com/en/content/learn/modules/lex_implementation_data_management/lex_implementation_data_import?trail_id=force_com_dev_beginner&trailmix_creator_id=lanfu2&trailmix_slug=lanis-trailmix)

#### Import data using the Data Import Wizard.
#### Download a CSV file that contains contact data, and import it using the Data Import Wizard.
Download this CSV file by right-clicking and selecting "Save Link As". Make sure you save it as a CSV (.csv) file, and not a text (.txt) file. You don't need to use Excel.
### Use the Data Import Wizard to import the file:
  * #### Kind of data: Accounts and Contacts
  * #### Type of import: Add new records
  * #### Match Contact by: Name
* #### Where is your data located?: CSV
  * ####  File: Choose File
  * ####  Character Code: ISO-8859-1 (the default)
  * #### Character Code: ISO-8859-1 (the default)
   * #### Values Separated by: Comma
* #### Map all fields:
   * #### FNAME to Contact: First Name
   * #### LNAME to Contact: Last Name
   * #### CELL to Contact: Mobile

