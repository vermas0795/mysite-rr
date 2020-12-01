---
title: "Test Strategy"
description: "Test strategy provides a rational deduction from organizational, high-level objectives to actual test activities to meet those objectives from a quality assurance perspective"
date: 2020-01-28T00:34:51+09:00
draft: false
weight: -4
---
![RR-Logo](../../../images/Rolls-Royce.jpg)

### Test Strategy

Version 1.0

![R2DL-Logo](../../../images/R2DL.jpg)

**Warning**

This is a hard copy of a document maintained on electronic media. It may not be the latest version. Kindly ascertain the latest version from the Document Master List available with the Project Leader.

**REVISION LIST**

| Revision No. | Revision Date | Revision Description | Revision By | Remarks |
| - | - | - | - | - |
| Initial Draft | 03/06/2020 | Initial Setup | Balaji |   |
| v0.1 | 10/06/2020 | Review Comment Implemented | Jayalakhmi and Karthika |   |
| v0.2 | 23/06/2020 | Final Review Comment Implemented | Samitanjaya |   |

**REVIEW LIST**

| Revision No. | Revision Date | Revision By | Remarks |
| - | - | - | - |
| Initial Draft | 04/06/2020 | Mayank Madhukar |   |
| v0.1 | 08/07/2020 | Mayank Madhukar |   |


## 1. Introduction

These sections detail out the overall purpose of the document, the purpose and the target audience who can refer the document and the references used while creating this document.

### 1.1 Purpose

> This document is the guideline that can be followed as a base for any type of project in any of the stream.
>
> The purpose of this document is to draw an outline that describes thetesting approach of the software development cycle. Test strategy provides a rational deduction from organizational, high-level objectives to actual test activities to meet those objectives from a quality assurance perspective. The creation and documentation of a test strategy should be done in a systematic way to ensure that all objectives are fully covered and understood by all stakeholders.
>
> This document scope is to have a complete test strategy for the {PROJECT NAME} application. This document will include the test strategy for all the layers of {PROJECT NAME} application. This document is created by QA and reviewed by Product Owner. This testing strategy will be used across all the sprints.

### 1.2 Intended Audience

This document is intended for the following audience:

- **Analysts/ Business Analysts/ System Analysts --** to create functional test cases, or sometimes even to carry out the test cases themselves.
- **Software Developers --** to keep track of the workflow followed to reproduce an issue.
- **Project Managers --** advocating the appropriate level of quality by the resolution of important defects.

## 2. Test Approach

Testing approach provides details of the processes and testing activities that are followed in the overall quality lifecycle of the {PROJECT NAME} application. The approach follows three key principles, to test early, everywhere and every time, a focus on continuous testing and pushing test left is utilized to achieve this goal.

The below mentioned test approach defines the test plan, roles and responsibility of various team members, testing levels, defect tracking and management. The approach will be followed for both web applicationlayer and database layer.

{Please add other specific information about the project, if applicable}

### 2.1 Test Plan

- During each sprint, a sprint test plan will be created and reviewed.
- Test cases will be created for each Product Backlog Item. These willbe based on the PBI's acceptance criteria.
- Testing will be conducted throughout the sprint for development complete PBI's and defect fixes.
- As the testing is done during each sprint, the results will be tracked in VSTS and corresponding defects will be raised and managed in VSTS.
- If there is any change in requirement in the sprint execution period, corresponding required test cases will be added to Product Backlog Items.
- Once the defects are fixed retest will be done followed by regression testing before final release and go-live.
- Sign off from QA will be provided before the final release or go-live

  ### 2.2 Test Actors
- The Test Actors are the Product Owner-PO, Scrum Master, Product Developers and QA.
- QA team will be responsible for creating sprint wise test plan, writing test cases for each PBI, executing the test cases and tracking the results in VSTS, defect finding and managing in VSTS.
- Product Developers are responsible for conducting unit testing for each PBI and fixing the defects raised by the QA.
- Product Owner and Scrum Master are responsible for reviewing and approving all the test activities carried out in each sprint.

### 2.3 Levels of Testing

#### 2.3.1 Unit Testing

> Unit testing will be integrated in to the development lifecycle developers will aim to cover all complex business logic and will be run as part of continuous integration

#### 2.3.2 Buddy testing

> Buddy testing activities will be run in the dev environment during the sprint; testers will sit with the developers and test the application to ensure business logic is enforced. This approach is followed on a case to case basis and is primarily focused on testing business
> critical flows so as to identify and fix high severity defects early in the life cycle.

#### 2.3.3 Functional Testing

> Functional testing will be carried out by the test team to confirm components of the solution are functioning as expected. The test cases written for each PBI will be executed and the corresponding results will be tracked in VSTS

#### 2.3.4 Integration Testing

> End to end Integration testing conducted by test team on the test/QA environment.

#### 2.3.5 Regression Testing

> Regression Testing will be performed by the QA team typically on release basis to ensure the defect fixes and new features developed have not impacted the existing functionality.

#### 2.3.6 User Acceptance Testing

> User Acceptance Testing will be performed by the end user before the application will go live. This will be conducted during the last sprint when the complete application is ready to go live. User must be provided the Application User Guide and along with the details of what and how the features of application works and how it is configured to use.

#### 2.3.7 Sanity Testing

> Sanity testing is a kind of Software Testing performed after receiving a software build, with minor changes in code, or functionality, to ascertain that the bugs have been fixed and no further issues are introduced due to these changes. The goal is to determine that the proposed functionality works roughly as expected. If sanity test fails, the build is rejected to save the time and costs involved in a more rigorous testing.

#### 2.3.8 Automation Testing

> Automation Testing means using an automation tool to execute your test case suite. The automation software can also enter test data into the System under Test, compare expected and actual results and generate detailed test reports. Test Automation demands considerable investments of money and resources.

## 3. Test Management

### 3.1 Defect Tracking

Testing will be performed post development team release the PBI to QA on the test environment. All the defects found during the testing process will be raised against each PBI's and assigned to the respective developer. Once the defect is fixed and released for testing, test team will perform the testing against the defect followed by regression testing specific to the functionality. All the defects are created and managed in VSTS application.

QA Team needs to set up a meeting to go over:

1. Defect template / Defect naming conventions for the project
2. Definitions of priority/severity
3. Where /how the defects will be logged
4. How to link defects to PBI
5. Explaining the defect lifecycle based on the process followed in VSTS board

**Determining Defect Severity**

![Severity](../../../images/Test_Strategy_Severity.png)

### 3.2 Defect Triage

Defect Triage and remediation should occur promptly during testing. A process for triaging the defects, providing timely feedback to other stakeholders (e.g. Development group), and for communicating fixes are available should be clearly laid out well in advance of the beginning of testing. This process definition should account for reporting issues, triaging issues, escalation, SLA's and the agreed upon communication process between different teams.

## 4. Test Execution Approach

{Mention the layers of the project and describe them all}

The test execution approach varies from layer to layer and the following approach will be followed for each layer.

### 4.1 Web Layer

This layer is the front end of the application. In this layer functionality, usability, interface, compatibility, database, security and performance of the application will be tested.

#### 4.1.1 Functional Testing

Functionality testing will be conducted in order to ensure application developed is as per the specifications. Following testing activities will be conducted

**Test Links** - Testing all the links in the webpages are working correctly and making it sure that there are no broken links. Outgoing links, Internal links, Anchor links and Mail-To links are the links to be tested.

**Test Forms** - In this section testing is conducted to check if Test forms are working as expected. This includes following few scenarios.

- Scripting checks on the forms are working as expected. For Example: If a user does not fill a mandatory field in a form an error message is displayed.
- Checking whether default values are being populated.
- Once the form is submitted, the data in the forms is submitted to database.
- Forms are optimally formatted for better readability

> **[Test HTML and CSS -]** In this section testing is conducted in order to check all the \<applicable\> browsers can render all the HTML and CSS styles applied.
>
> **[Test Business Workflow -]** Business workflow will be tested which includes
>
> - Testing the end to end workflow scenarios which take the user through a series of webpages to complete.
> - Testing negative scenarios like when user executes an unexpected step, an appropriate error message shown.

#### 4.1.2 Usability Testing

> Usability testing will be conducted which includes
>
> **[Test the site Navigation -]** Menus, Buttons and Links to different pages on the pages should be easily visible and consistent on all the pages.
>
> **[Test the Content ]**
>
> * Contents should be correct with no spelling or grammatical errors.
> * If there are images in the web page, it should contain an "alt" message which will be shown when the browser takes time to load the images.

#### 4.1.3 Interface Testing

> Interface Testing includes testing of interface between the web and Data layer. All the layers should be well connected and perform the necessary actions.
>
> **[Web Layer -]** User requests are sent correctly to the API layer or Database layer and get the output correctly which is displayed to the user at front end. If any errors occur, it should be caught by the application and shown to the user as well as logged in the application logs.
>
> **[Database Layer -]** When the user makes the request, depending on the request type database layer is responsible for providing the necessary action like getting the data, saving the new data, updating and deleting the existing data.
>
> **{Please mention the other layers and define it, if applicable\}**

#### 4.1.4 Database Testing

> Database testing is conducted in order to check whether the database is connected to application and able to perform all the necessary data related actions which include
>
> * Test if any, errors occur while executing the queries
> * Checking the data retrieved from database which is shown accurately in the web application

#### 4.1.5 Compatibility Testing

> Compatibility testing is performed in order to make sure that web application is displayed correctly across different devices and browsers as applicable for the project.
>
> **[Browser Compatibility Testing -]** Web application is displayed differently in different browser. Testing is required to ensure web application is displayed correctly across all the
> applicable browsers for the {PROJECT_NAME}
>
> **[Operating System Compatibility -]** Rendering of the web elements like buttons and text fields changes from change in operating system. The application needs to be tested for combination of various operating systems as applicable for the {PROJECT_NAME}
>
> (Ex: iOS, Windows, mac-OS, Android) and web browsers (ex: IE, Edge, and Safari).

#### 4.1.6 Performance Testing

> Basic performance test is conducted by the QA team as part of PBI verification to ensure the response time for various features is within the acceptable time frame. A full-fledged performance test is out of scope for the functional QA team and needs to be supported by performance testing team.

#### 4.1.7 Security Testing

> Security testing is performed in order to make sure the data is secured.
>
> Testing includes:
>
> * Testing the unauthorized access to web application.
> * Testing the access to functionalities depending on user role basis.
> * Checking of the session status when user is inactive.
> * If SSL certificate is used, website should be redirect to encrypted SSL pages.
> * OWASP can be a good source of test case creation
> * An in-depth security testing should be conducted by third-party team as applicable for the project to satisfy confidence in system security.

### 4.2. Database Layer

> **This section is to be updated by Database/ETL Testing team**
>
> Database layer is the back end of the application. In this layer testing will be done in order to make sure all the data related activities are working as per the business requirements. Following  types of database testing will be conducted, in case of Structured
> DB setup. Please follow other set up of required testing if DB used other than the structured DB.

#### 4.2.1 Structural Database Testing

> The Structural database testing involves the validation of all the elements inside the repository that are used primarily for storage of the data. And this data is not allowed to be directly manipulated by the end users.
>
> **[Schema Testing]**
>
> The main aspect of schema testing is to ensure that the schema mapping between the front end and the backend is similar and the data uploaded using the scripts and backend is similar. Following are the few testing actions involved in schema testing
>
> * Validating the mapping format of the table and mapping format present in the user interface level of the application.
> * Validating the mapping format of the table and mapping format of the data uploaded using the scripts.
> * Verify if any unmapped tables, columns or views present in the schema.
>
> **[Database Table and Column Testing]**
>
> * Validating the mapping of data fields and columns in the back end is compatible with those mappings in the front end.
> * Validation of the length and naming conventions of the database fields and columns as per the requirement.
> * Validation of any unused or unmapped database tables or columns present.
> * Validation of compatibility of data types and field lengths of the database columns and with that of those present in the frontend of the application.
> * Validation of the database fields which allows the user to provide the desired user inputs as specified in the business requirements.
>
> **[Constraints Testing]**
>
> * Check whether the required Primary key and Foreign Key constrains is created on the required tables.
> * Check whether the references for foreign keys are valid.
> * Check whether the data type of the primary key and the corresponding foreign keys are same in the two tables
> * Check whether the required naming conventions have been followed for all the keys
> * Check the size and length of the required fields in the table.
>
> **[Database Server Validation]**
>
> * Check the database server configurations are as per the specifications mentioned in business requirement
> * Check the authorization of the required user to perform only those
>   levels of actions which are required by the application.
> * Check whether the database server is able to perform to the needs of maximum allowed number of user transactions as specified in the business requirements.

#### 4.2.2 Functional Database Testing

> The Functional Database Testing is performed to ensure all data related transactions and operations are performed are consistent with the requirement specifications. Following are the test carried out to check the database is functioning as per the requirement.
>
> **[Checking Data Integrity and Consistency]**
>
> Following are the checks conducted in order to make sure the data
> integrity and consistency.
>
> * Check whether the data is logically well organized
> * Check whether the data stored in the tables is correct and as per the business requirements
> * Check whether there are any data redundancy and unnecessary data
> * present in the application under test.
> * Check whether the data obtained from the user interface or from running backend scripts has been stored as per the requirement.
> * Check whether the TRIM operations performed on the data before inserting data into the database.
> * Check whether the transactions have been performed according to the business requirement specifications and the results are as expected.
> * Check whether the data has been properly committed if thetransaction has been successfully executed as per the business requirement.
> * Check whether the data has been roll backed successfully if the transaction has not been executed successfully by the end user or by the backend data inserts scripts not executed properly.

#### 4.2.3 Non Functional Database Testing

> Load testing on the database is categorized under the Non-functional database testing.
>
> **[Load Testing]**
>
> * Load test is performed to determine the database behavior under normal and peak load. Load testing will be conducted considering the following aspects.
> * The response time for executing the transactions for multiple remote users will be checked
> * The most frequently used user transactions have the potential to impact the performance of all the other transactions if they are not efficient
> * Along with normal transactions, one editable transaction will be included in order to check the performance of the database for these types of transactions
> * Along with normal transactions, one non-editing transaction will be included in order to check the performance of the database for these types of transactions
> * The more important transactions that facilitate the core objectives of the system should be included. The impact of failure of these transactions under the load should be checked.
> * Time taken by the database to fetch specific set of records will be checked.

## 5. Test Environment

The below table shows the levels of testing conducted in different environments.

| Dev | QA | UAT/Pre-Prod | Prod |
| - | - | - | - |
| Unit Testing | Functional Testing | User Acceptance Testing | Sanity Testing |
| Buddy Testing | Integration Testing | Regression Testing |  |

## 6. Testing Tool

Below Software's Tools are used to perform testing.

| Layer Name | Software/ Tool |
| - | - |
| Web Application Layer | Web Browser |
| Database Layer | SQL/No-SQL |

## 7. Risk Analysis

{List down all the risk and analyze it to perform better as the
project evolve}

| Risk Reference | Description |
| - | - |
| RS01 |   |
| RS02 |   |

## 8. Dependencies

- VSTS access should be provided
- Test environment should be made available for testing
- Web interface should be available for user interface testing.
- Test Data should be available
- All the assets should be available for testing.

## 9. Review and Approvals

- Product Owner will be responsible for validating and approving all
  test results
- The end users and stake holders will validate and Sign Off on the
  User Acceptance Test results.

## GLOSSARY

- **Rational Deduction** -- Deduction is the sort of rationality that
  is the central concern of traditional logic. It involves deductively
  valid arguments, or arguments in which, if the premises are true,
  then the conclusion must also be true.
- **Quality Assurance(QA) --** is a means and practice of monitoring
  the software engineering processes and methods used in a project to
  ensure proper quality of the software.
- **Stakeholders --** a person, group or company that is directly or
  indirectly involved in the project and who may affect or get
  affected by the outcome of the project.
- **Sprint --** one timeboxed iteration of a continuous development
  cycle.
- **Product Backlog Item(PBI) --** Items (PBIs) are the elements that
  make up the Product Backlog.
- **VSTS --** VSTS is an Application Lifecycle Management (ALM) system
  which helps the entire project team to capture Requirements, Agile
  /Traditional Project Planning, Work Item management, Version
  Control, Build, Deployment, and manual Testing all in a single
  platform.
- **Regression Testing --** defined as a type of software testing to
  confirm that a recent program or code change has not adversely
  affected existing features.
- **Product Owner(PO) --** owner is a role on a product development
  team responsible for managing the product backlog in order to
  achieve the desired outcome that a product development team seeks to
  accomplish.
- **Scrum Master --** the team role responsible for ensuring the team
  lives agile values and principles and follows the processes and
  practices that the team agreed they would use.
- **Triage --** process where tracker issues are screened and
  prioritized. Triage should help ensure we appropriately manage all
  reported issues - bugs as well as improvements and feature requests.
- **SLA --** contract between a service provider and its customers
  that documents what services the provider will furnish and defines
  the service standards the provider is obligated to meet.
- **OWASP --** Open Web Application Security Project is an online
  community that produces freely-available articles, methodologies,
  documentation, tools, and technologies in the field of web
  application security.
- **SSL --** Secure Sockets Layer, is an encryption-based Internet
  security protocol.
- **Repository --** central file storage location. It is used by
  version control systems to store multiple versions of files.
- **Schema --** The database schema of a database is its structure
  described in a formal language supported by the database management
  system. The term \"schema\" refers to the organization of data as a
  blueprint of how the database is constructed.
- **TRIM --** the TRIM() function removes leading and trailing spaces
  from a string.

