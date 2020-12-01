---
title: "DB Glossary"
description: "This document is a template which different projects can follow. This document will detail out the glossary for the DB set up of the project."
date: 2020-01-28T00:34:51+09:00
draft: false
weight: -4
---
![RR-Logo](../../../images/Rolls-Royce.jpg)

### DB Glossary

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

> This document is a template which different projects can follow. This document will detail out the glossary for the DB set up of the project.
> 
> The sole purpose of the document is to list down all the necessary information related to Db getting used in the project. This Document will have the list of all the tables and the full details along with attributes and necessity of them along with what type of info is getting stored in the table.
> 
> Also, it will have information about all the other entities which can be a part of the DB Structure which includes Stored Procedure,Functions and Triggers and so on.

### 1.2 Intended Audience

This document is intended for the following audience:

- **Development Teams** -- As a reference for development team to on how to setup the DATABASE.
- **Technical subject matter experts (SMEs) from Rolls-Royce** -- To locate the technical details for DATABASE setup for the project.
- **Database Administrators (DBA)** -- As a reference document for DBA to setup and maintain the DATABASE.
- **Application Maintenance Team**s -- As a reference doc to update and maintain the DATABASE.

## 2. Server and Repo Details

### 2.1 Repository Details

| Name | Latest Branch | Link | Comments |
| :- | :- | :- | :- |
| {Name of the git repo} | {Branch name having latest updated code under repo} | {Please paste the link of the repo here} |   |

### 2.2 Server Info

| Name | Latest Branch | Link |
| :- | :- | :- |
| **Dev** | {Please add server name} | {Please paste the connection string here} |
| **QA** | {Please add server name} | {Please paste the connection string here} |
| **Pre-Prod** | {Please add server name} | {Please paste the connection string here} |
| **Prod** | {Please add server name} | {Please paste the connection string here} |

## 3. Entity Relationship Diagram

Entity Relationship Diagram, also known as ERD, ER Diagram or ER model, is a type of structural diagram for use in database design. An ERD contains different symbols and connectors that visualize two important information: **The major entities within the system scope**, and the **inter-relationships among these entities.**

{Please paste the ER diagram here or give a link for the same}

## 4. Tables

### Table - Table Name

{Give the brief details about the table and data stored for different purpose. Please refer below the dummy structure of the table and list down all the tables in same format}

| Name | Data Type | Constraint | Description |
| :- | :- | :- | :- |
| **Id** | bigint | Identity(1, 1), Not Null | Primary Key |
| **Name** | varchar(max) | Not Null | Name Required |
| **...** | ... | Reference(Other  Table) | Foreign Key |
| **IsActive** | bit | Not Null | Soft delete |

***UNIQUE Key Constraint**: Combination of unique attributes used for creating Unique Constraints.

### Table - Table Name

and So On......

## 5. Stored Procedure And Functions And Views

### 5.1 Procedure

A stored procedure is a prepared SQL code that you can save, so the code can be reused over and over again. So if you have an SQL query that you write over and over again, save it as a stored procedure, and then just call it to execute it.

##### Procedure - Stored Procedure Name

**Input**: { Input expected by the stored procedure. }

**Output:** { Output by Stored Procedure. }

### 5.2 Function

Function is a database object in SQL Server. Basically, it is a set of SQL statements that accept only input parameters, perform actions and return the result. Function can return an only single value or a table

##### Function - Function Name

**Input:** { Input expected by the function. }

**Output:** { Output by function. }

### 5.3 Views

In SQL, a view is a virtual table based on the result-set of an SQL statement. A view contains rows and columns, just like a real table. The fields in a view are fields from one or more real tables in the database. You can add SQL functions, WHERE, and JOIN statements to a view and present the data as if the data were coming from one single table.

## 6. Triggers

A trigger is a special type of stored procedure that automatically runs when an event occurs in the database server. DML triggers run when a user tries to modify data through a data manipulation language (DML) event. DML events are INSERT, UPDATE, or DELETE statements on a table or view. These triggers fire when any valid event fires, whether table rows are affected or not.

##### Trigger - TriggerName

{Please list down all the trigger getting used/ setup in the DB Env.}

## 7. SQL Agent OR Windows Jobs

A job is a specified series of operations performed sequentially by SQL Server Agent. A job can perform a wide range of activities, including running Transact-SQL scripts, commandprompt applications, Microsoft ActiveX scripts, Integration Services packages, Analysis Services commands and queries, or Replication tasks. Jobs can run repetitive or schedulable tasks, and they can automatically notify users of job status by generating alerts, thereby greatly simplifying SQL Server administration.

##### Job -Job Name

{Please list down all the jobs setup on Database with the details here. }

## GLOSSARY

- **Attributes --** a piece of information which determines theproperties of a field or tag in a database
- **Connection String --** a connection string is a string thatspecifies information about a data source and the meansof connecting to it
- **Data Type --** a  particular kind of data item, as defined by thevalues it can take
- **Constraint --** a limitation or restriction on the Table structure with attributes

