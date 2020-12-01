---
title: "Code Setup"
description: "This document will detail out the necessary steps starting from setup till running the project locally on the development machines"
date: 2020-01-28T00:34:51+09:00
draft: false
weight: -4
---
![RR-Logo](../../../images/Rolls-Royce.jpg)

### Code Setup

Version 1.0

![R2DL-Logo](../../../images/R2DL.jpg)

**Warning**

This is a hard copy of a document maintained on electronic media. It may not be the latest version. Kindly ascertain the latest version from the Document Master List available with the Project Leader.

**REVISION LIST**

| Revision No. | Revision Date | Revision Description | Revision By | Remarks |
| - | - | - | - | - |
| Initial Draft | 03/06/2020 | Initial Setup | Abhishek |   |
| v0.1 | 10/06/2020 | Review Comment Implemented | Abhishek |   |
| v0.2 | 21/06/2020 | Final Review Comment Implemented | Abhishek |   |

**REVIEW LIST**

| Revision No. | Revision Date | Revision By | Remarks |
| - | - | - | - |
| Initial Draft | 04/06/2020 | Mayank Madhukar |   |
| v0.1 | 08/07/2020 | Mayank Madhukar |   |


## 1. Introduction

These sections detail out the overall purpose of the document, the purpose and the target audience who can refer the document and the references used while creating this document.

### 1.1 Purpose

> This document is a template which different projects can follow. This document will detail out the necessary steps starting from setup till running the project locally on the development machines.
> 
> The sole purpose of the document is to define and list down all the necessary requirement and knowledge which the developer should be ready with before actual hands on. This document also contains the knowledge of git push and pulls commands and first time project step up. This document can even be used as project starter for new
> developer or as technical set up handover document

### 1.2 Intended Audience

This document is intended for the following audience:

- **Development Teams** -- As a reference for development team to on how to setup the code initially.
- **New Member/Teams** -- As a reference during handover of the project or if new member joining the team.

## 2. Workflow OR Technical Architectural Diagram

{Please attach the workflow or architecture diagram and explain them
here.}

## 3. List of Softwares

- Software tools which are used in {Project name} are listed below. These software's need to be installed on developer workstation.

**Developer Tools**

| **Database** | DB and Management tool |
| :- | - |
| **Back End /API IDE** | Tool name and version |
| **Front End / UI IDE** | Tool Name and version |
| **Deployment Tool** | Tool Name |
| **Git** | Code Sync up |
| {**Add Others if any**} | {Details Here} |

- Tech stack's which are used in {Project name} are listedbelow:

**Tech Stack**

---

| **Database** | {Details Here} |
| :- | :- |
| **Back End /API with libraries** | {Details Here} |
| **Front End / UI with libraries** | {Details Here} |
| **Docker/Kubernetes/Containerisation(if using)** | {Details Here} |
| **Cloud Services(if using)** | {Details Here} |
| **CI/CD(if Using)** | {Details Here} |
| **Environments Available** | {Details Here} if CI/CD pipeline is not present. Provide a brief summary how to deploy the code. |
| {**Add Others if any**} | {Details Here} |

## 4. Pull Code from VSTS

### 4.1 VSTS Project Repository Information

##### 4.1.1 Diff Codes Area Info

| **Name** | **Link** |
| :- | - |
| **API** | {Link Here} |
| **App** | {Link Here} |
| **DB/Date Engineering** | {Link Here} |
| **If others** | {Link Here} |
| {**Add Others if any**} | {Link Here} |

##### 4.1.2 Latest Branch Info

| **Name of Repo/Type** | **Branch Name** | **Date Created** | **Date updated** |
| - | - | - | - |
| {Name} | {Branch Name} |   |   |

### 4.2 Steps to setup code locally

Setting up the code in Visual studio from VSTS by using the below process/ git commands:

**Steps to setup proxy:**

1. Remove the proxy configuration

> git config \--global \--unset http.proxy

2. Add the proxy configuration

> git config \--global \--add http.proxy [http://:@10.128.0.110:3128](http://:@10.128.0.110:3128)

Please restart system after following above process.

**Steps to set up the already existing repo to your local system for the
First time**

1. Move to proper path where you want to store your code. Preferable is: C:/Users/ username/source/repo.
2. Create above path if doesn't exist already.
3. git clone {URL}
4. Might ask for GIT credentials. Please follow below steps to setup git credentials

> * Open VSTS/Azure dev-ops portal.
> * Click on right top extreme end -- second last icon user settings.
> * Select Alternate Credentials from the menu
> * Setup username and Password and Save it

5. Use the above credentials and you are good to go.

**Steps to set up the repo initially**

1. Move all you codes with proper folder structure to new Directorywith name as Project name.
2. Add GIT and other Ignore Files to the folder.
3. git init
4. git add .
5. git commit --m "{your comments here}"
6. git remote add origin {URL}
7. git push origin master
8. Might ask for GIT credentials. Please follow above mentioned stepsfor setting up git credentials (setup git credentials)

**Note**: *.URL is URL to repo and will be available with the Dev team or scrum master.

## 5. Push Code to VSTS

### 5.1 Steps to push code VSTS

Code changes can be pushed back to VSTS using the following process.

1. First check the code changes by using below command

> **git status**

2. Now check the branch of a solution as below

> **git branch**

3. If want to create a new branch then,

> **git branch {NEW_BRANCH NAME}**

4. To switch any branch,

> **git checkout {BRANCHNAME}**

5. Now commit the changes

> **git add .**
>  **git commit --m** **"{your comments here}"**

6. Push the changes back to VSTS

> **git push origin {BRANCHNAME}**

### 5.2 Create Pull Request

By following above process, push the code to VSTS and then follow the below process for Pull Request.

1. Go to Repos Select Pull Requests New/Create Pull Request
2. Select proper branches in "from" and "into" options resp.
3. Give Title, Description, Reviewers and Work item, if any and then click on Create.
4. Once approved your code will be merged with the latest branch.

## 6. Code Setup

{Please describe all the steps to set up the Application starting from the Database, front end and Backend to local system}

## 7. Miscellaneous

{Please describe all the steps configuration changes need to be done before running the solution locally}

## GLOSSARY
