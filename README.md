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
   * #### Code: Copy from GitHub
* #### Place the unit tests in a separate test class:
    * #### Name: TestVerifyDate
    * #### Goal: 100% code coverage
    * #### Run your test class at least once
