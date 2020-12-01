---
title: "Branching Strategy"
description: "The sole purpose of the document is to setup and define the project specific strategy for branching and release."
date: 2020-01-28T00:34:51+09:00
draft: false
weight: -4
---
![RR-Logo](../../../images/Rolls-Royce.jpg)

### Branching Strategy

Version 1.0

![R2DL-Logo](../../../images/R2DL.jpg)

**Warning**

This is a hard copy of a document maintained on electronic media. It may not be the latest version. Kindly ascertain the latest version from the Document Master List available with the Project Leader.

**REVISION LIST**

| Revision No. | Revision Date | Revision Description | Revision By | Remarks |
| - | - | - | - | - |
| Initial Draft | 03/06/2020 | Initial Setup | Abhishek |   |
| v0.1 | 10/06/2020 | Review Comment Implemented | Abhishek |   |
| v0.1 | 20/06/2020 | Final Review Comment Implemented | Abhishek |   |

**REVIEW LIST**

| Revision No. | Revision Date | Revision By | Remarks |
| - | - | - | - |
| Initial Draft | 04/06/2020 | Mayank Madhukar |   |
| v0.1 | 08/07/2020 | Mayank Madhukar |   |


## 1. Introduction

These sections detail out the overall purpose of the document, the purpose and the target audience who can refer the document and the references used while creating this document.

### 1.1 Purpose

> This document is the guideline that can be followed as a base for any type of project in any of the stream. This document will require the pre knowledge with very basic understanding of GIT and the process.
> 
> The sole purpose of the document is to setup and define the project specific strategy for branching and release. By following the basic structure setup from this document different teams/ developer can setup the strategy in their respective projects and would be able to achieve the full stabilized workflow/code with very less branches which implies less cost and almost zero complexity to maintain and handle the branch on the local as well on the remote repositories.

### 1.2 Intended Audience

This document is intended for the following audience:

- **Development Teams** -- as guidelines for development team to how to start with VSTS/Azure Dev-ops and follow branching hierarchy for development and release.
- **Deployment Teams** -- To locate the stable branch and to get the stable code to deploy over multiple environments.

## 2. Branching Strategy

### 2.1 GIT

**GIT** is an Open Source **Distributed Version Control System**. This basically means that GIT is a content tracker. GIT mostly used to store content and helps different teams and developer in handling code changes by maintaining a history of what changes have happened and when and by whom.

GIT simplifies the process of sharing and manage code and helps teams working with other people to collaborate on projects in very easy manner. Team members can work on files and easily merge their changes in with the other branches of the project. This allows multiple people to work on the same files at the same time and helps remove discrepancies
when arises.

![Branching_Strategy_Prerequsite](../../../images/Branching_Strategy_Prerequsite.PNG)

**Steps to set up the repo initially**

1. Move all you codes with proper folder structure to new directory with name as Project name.
2. Add GIT and other Ignore Files to the folder.
3. git init
4. git add .
5. git commit --m "{your comments here}"
6. git remote add origin {URL}
7. git push origin master
8. Might ask for GIT credentials. Please follow below mentioned steps for setting up git credentials (setup git credentials)
9. Move to proper path where you want to store your code. Preferable is: C:/Users/ username/source/repo.

> - Create above path if doesn't exist already.
> - git clone {URL}
> - Might ask for GIT credentials. Please follow below steps to setup git credentials
> - Open VSTS/Azure dev-ops portal.
> - Click on right top extreme end - second last icon user settings.
> - Select Alternate Credentials from the menu
> - Setup username and Password and Save it.
> - Use the above credentials and you are good to go.

### 2.2 Branches and Hierarchy

![Branching_Strategy_Hieararchy](../../../images/Branching_Strategy_Hieararchy.PNG)

## 3. Release Workflow

![Branching_Strategy_Release](../../../images/Branching_Strategy_Release.PNG)

## 4. Workflow Details

- During Sprint, developer will create the branches depending upon theamount of work assigned from task/story.

e.g. **160385-DiscussBranching**.

- After the developer delivers the story and buddy testing is done, he needs to create Pull request (**PR**) to merge the local branch(**160385-DiscussBranching**) into the current Sprint branch (**Sprint1**). The Peer / Lead will review his/her code and then after approval the branches will be merged.
- Once, the developer level branch (**160385-DiscussBranching**) is merged with Sprint level branch (**Sprint1**), it is ready for the new release to Test/QA environment.
- After proper integration testing on the sprint branch (**Sprint1**), the branch is ready to be merged with**UAT** branch. This branch would carry out the regression testing along with integration. This branch is focused to get the user acceptance.
- Once all the testing is done on**UAT**, the branch is good enough to be merged with the Pre-Prod where performance and regression testing will be performed.
- After successful results from the**Pre-Prod** at the final stage, it will be merged with "**master**" branch and ready to go for production.

Also, Depending upon the project requirement and availability of resource(Infra environment) QA/UAT and Pre-prod can be merged into single one and you can set up the policies on the Azure Dev-ops on different branch with multiple condition like no. of reviewers, approvers etc.

**Note**: By following the above hierarchy we'll always have the stable branch at each stage in the different release and at any point of time the released can be reversed to last stable version.

## GLOSSARY

- **GIT -** Git is a platform to share the code among teams. For more information, please click[here](https://git-scm.com/doc)
- **Branching --** Way to organize different version of codes
- **Remote Repository --** Centralized storage available over the cloud with GIT
- **Azure/VSTS --** Project Management platform to run and track projects and even store codes
- **Deploy --** Moving the project code to a place where it will be accessible as application to wider group
- **Distributed --** spread/shared across different areas
- **Version Control System --** Version Control System helps in handling changes by maintaining a history of what changes have happened
- **GitHub --** A remote host storage location accessible among different teams
- **Pull Request (PR) --** A Mechanism for a developer to notify team members that they have completed a feature and want to merge with latest version of code
- **QA --** QA means Quality Assurance and here it is referred as one of the Environment of application on which QA team will be working and testing code
- **UAT --** UAT means User Acceptance Testing and here it is referred as one of the Environment of application on which group of user team will be working and testing code and check if everything as per expectation
- **Pre-Prod --** Pre-Prod as it name defines is an environment for testing before it actually goes to final Production for actual use case
- **Buddy Testing --** A mechanism where testers will sit with the developers and test the application to ensure business logic is enforced
- **Peer Review --** A mechanism where peer developer will review the code to ensure everything is followed including standards before it is been actually go to Lead for Pull Request.
- **Integration Testing --** End to end testing of all the features conducted by test team
- **Acceptance Testing --** User Acceptance Testing performed by the end user before the application will go live.
- **Regression Testing --** Testing to ensure the defect fixes and new features developed in different version of release have not impacted the existing functionality
- **Automation Testing --** Automation Testing means using an automation tool to execute your test case suite
- **User Story --** a user story is a formal, natural language description of one or more features of a software system.
- **Product Backlog Item (PBI) --** PBI is just the name of user story.

