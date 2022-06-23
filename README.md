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
## Challenge 10 Create Test Data Factory for Apex Tests:
https://trailhead.salesforce.com/content/learn/modules/apex_testing/apex_testing_data?trailmix_creator_id=lanfu2&trailmix_slug=lanis-trailmix
### Learning Objectives
 * #### Create a test utility class.
 * #### Use a test utility method to set up test data for various test cases.
 * #### Execute all test methods in a class.
 * 
### Create a Contact Test Factory
#### Create an Apex class that returns a list of contacts based on two incoming parameters: the number of contacts to generate and the last name. Do not insert the generated contact records into the database.

#### NOTE: For the purposes of verifying this hands-on challenge, don't specify the @isTest annotation for either the class or the method, even though it's usually required.
* #### Create an Apex class in the public scope
   * #### Name: RandomContactFactory (without the @isTest annotation)
* #### Use a Public Static Method to consistently generate contacts with unique first names based on the iterated number in the format Test 1, Test 2 and so on.
   * #### Method Name: generateRandomContacts (without the @isTest annotation)
   * #### Parameter 1: An integer that controls the number of contacts being generated with unique first names
   * #### Parameter 2: A string containing the last name of the contacts
   * #### Return Type: List < Contact >

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

#### Two methods to import data from outside of salesforce: Data Import Wizard and Data Loader

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


### Project 2: Export Data:
https://trailhead.salesforce.com/content/learn/modules/lex_implementation_data_management/lex_implementation_data_export?trail_id=force_com_dev_beginner&trailmix_creator_id=lanfu2&trailmix_slug=lanis-trailmix

#### Two methods of exporting data from salesforce: 
 * ##### Data Export Service—an in-browser service, accessible through the Setup menu. It allows you to export data manually once every 7 days (for weekly export) or 29 days (for monthly export). You can also export data automatically at weekly or monthly intervals. Weekly exports are available in Enterprise, Performance, and Unlimited Editions. In Professional Edition and Developer Edition, you can generate backup files only every 29 days, or automatically at monthly intervals only.
 * ##### Data Loader—a client application that you must install separately. It can be operated either through the user interface or the command line. The latter option is useful if you want to automate the export process, or use APIs to integrate with another system.
#### Follow these steps to export data using the Data Export Service.
```
1. From Setup, enter Data Export in the Quick Find box, then select Data Export and Export Now or Schedule Export.
  * The Export Now option prepares your files for export immediately. This option is only available if enough time has passed since your last export.
  * The Schedule Export option allows you to schedule the export process for weekly or monthly intervals.
2. Select the desired encoding for your export file.
3. If you want images, documents, attachments, and so on included in your data, select the appropriate options.
4. Select Replace carriage returns with spaces to have spaces instead of carriage returns or line breaks in your export files. This is useful if you plan to use your export files for importing or other integrations.
5. If you're scheduling your export, select the frequency (only available for organizations with monthly exports), start and end dates, and time of day for your scheduled export.
6. Under Exported Data, select the types of data to include in your export. We recommend that you select Include all data if you’re not familiar with the terminology used for some of the types of data.
7. Click Start Export or Save. Salesforce creates a zip archive of CSV files and emails you when it's ready. Exports will complete as soon as possible, however we can't guarantee the date and time the export will complete. Large exports are broken up into multiple files. Follow the link in the email or click Data Export to download the zip file. Zip files are deleted 48 hours after the email is sent.
```
***
## Challenge 19 Data Security:
https://trailhead.salesforce.com/content/learn/modules/data_security?trail_id=force_com_dev_beginner

### Overview of Data Security:
#### "The platform makes it easy to specify which users can view, create, edit, or delete any record or field in the app. You can control access to your whole org, a specific object, a specific field, or even an individual record. By combining security controls at different levels, you can provide just the right level of data access to thousands of users without having to specify permissions for each user individually."
####   You can manage record-level access in these four ways:
```
Records
**You can allow particular users to view an object, but then restrict the individual object records they're allowed to see. For example, an interviewer can see and edit her own reviews, but not the reviews of other interviewers. You can manage record-level access in these four ways.

1. Organization-wide defaults specify the default level of access users have to each others’ records. You use org-wide sharing settings to lock down your data to the most restrictive level, and then use the other record-level security and sharing tools to selectively give access to other users.

2. Role hierarchies give access for users higher in the hierarchy to all records owned by users below them in the hierarchy. Role hierarchies don’t have to match your organization chart exactly. Instead, each role in the hierarchy should represent a level of data access that a user or group of users needs.

3.Sharing rules are automatic exceptions to organization-wide defaults for particular groups of users, so they can get to records they don’t own or can’t normally see. Sharing rules, like role hierarchies, are only used to give additional users access to records. They can’t be stricter than your organization-wide default settings.

4. Manual sharing allows owners of particular records to share them with other users. Although manual sharing isn’t automated like org-wide sharing settings, role hierarchies, or sharing rules, it can be useful in some situations, such as when a recruiter going on vacation needs to temporarily assign ownership of a job application to someone else
```
### Control Access to the Org:
 * #### Create, view, and manage users.
 * #### Set password policies.
 * #### Limit the IP addresses from which users can log in.
 * #### Limit the times at which users can log in.
### Project: Create a guest administrator user and deactivate it
 * #### Your hands-on org comes with a System Administrator user. Create a new user using the System Administrator profile, then deactivate that user to preserve the licenses in your org.
 * #### Challenge Requirements
   * #### Create a new user:
    * ##### Profile: System Administrator
    * ######  User License: Salesforce
    * ###### Username: must contain guestadmin somewhere in it
* ##### Alias: guestadm
  * ######  The new user must be inactive

### Control Access to the Objects:
https://trailhead.salesforce.com/content/learn/modules/data_security/data_security_objects
 #### You can set object permissions with profiles or permission sets. Each user is assigned one profile. Users can be assigned one or more permission sets.
    * #### A user’s profile determines the objects they can access and the things they can do with any object record (such as create, read, edit, or delete).
   * #### Permission sets grant additional permissions and access settings to a user.
### Project: Create a Cleaner profile
#### through a data cleanup project, and you assigned a consultant to help you. You want the consultant to have read-only access to most objects, but have edit rights only on accounts, contacts, and leads. You don't want the consultant to delete anything or create new records.
#### Challenge Requirements
```
Clone the Minimum Access - Salesforce profile with the following settings:
Use existing profile: Minimum Access - Salesforce
Profile Name: Cleaner
Control access for the Cleaner profile:
Object Permissions: Accounts (Read, Edit)
Object Permissions: Contacts (Read, Edit)
Object Permissions: Leads (Read, Edit)
Make sure Edit and Create object permissions aren't enabled for any other objects in the Cleaner profile.
```
### Control Access to the Fields:
### Project: 
#### Create a profile and permission set to handle field access
Sales team members have most of the same object and field permissions as the Standard User profile. But your company wants to make sure that sales team members don’t delete certain records, and that only senior sales members have access to certain fields.

For this challenge, use both profiles and permission sets to control object-level permissions. Make sure that all sales team members can create, edit, and view accounts and contacts, but NOT delete them. Then make sure that most sales members can't see or edit the Rating field on accounts, but some senior sales members can.
```
Challenge Requirements
Clone the Standard User profile:
Existing Profile: Standard User
Profile Name: Sales
Control access for the Sales profile:
Standard Object Permissions:
Accounts: Read, Create, Edit
Contacts: Read, Create, Edit
Field Permissions:
Rating field on the Account object: no access
All other permissions from the Standard User profile remain as is
Create a new permission set:
Label: Rating
API Name: Rating
User License: Salesforce
Control access for the Rating permission set:
Field Permissions:
Rating field on the Account object: Read Access, Edit Access
```

### Control Access to Records:
#### You control record-level access in four ways. They’re listed in order of increasing access. You use org-wide defaults to lock down your data to the most restrictive level, and then use the other record-level security tools to grant access to selected users, as required.
```
Org-wide defaults specify the default level of access users have to each other’s records.
Role hierarchies ensure managers have access to the same records as their subordinates. Each role in the hierarchy represents a level of data access that a user or group of users needs.
Sharing rules are automatic exceptions to org-wide defaults for particular groups of users, to give them access to records they don’t own or can’t normally see.
Manual sharing lets record owners give read and edit permissions to users who might not have access to the record any other way.
```
### Project: Challenge Requirements
```
Create a custom object:
Label: Project
Plural Label: Projects
Object Name: Project
Record Name: Project Name
Record Name Data Type: Text
Configure organization-wide default sharing settings for the Project object so that Project records are visible only to the record owner and to users above them in the role hierarchy.
```

### Create a Role Hierarchy:
### Define sharing rules: 


*** 





