---
title: "Buisness Understanding"
description: "API Documentation Template"
date: 2020-01-28T00:34:51+09:00
draft: false
weight: -4
---


<sup>Security Classification: Private - Rolls-Royce Content Only - Not Subject to Export Control</sup>

![RR-Logo](../../../images/Rolls-Royce.jpg)

### Buisness Understanding

Version 1.0

![R2DL-Logo](../../../images/R2DL.jpg)

This documents explains in detail the __Business Understanding__ phase of the __Data Science Life-Cycle Process__

## Objective

---

The primary objective of the Business Understanding phase is to translate business need into a project/technical requirement.

## Diagram

---

A block diagram representation of the Business Understanding phase is shown the diagram below.

![Business Understanding](images/Business_Understanding.png)

## Activities

---

There activities in this stage are:

- Define Objectives
- Identify Data Sources
- Hypotheses Exploration

### __Define Objectives__

This phase involves working with customer and stakeholders to understand and identify the business problem that needs to be solved. Relevant questions needs to be formulated that define the business goals which can be analysed using the data science techniques.

A central objective of this step is to identify the key business variables that the analysis need to predict i.e., identify the target variable. Based on the target variable and the problem statement, identify the type of analysis, i.e., regression or classification or clustering or recommendation. A project team needs to be formed with roles and responsibilities assigned to each team member.

This step also includes identifying the metrics, for example, the model shall provide an accuracy of ‘x’ or ‘y’ hypothesis is valid. But it should be noted that the identified metric is not a measure of success of the project itself. At the end of the project we may not be achieving the accuracy that was defined at the start which might be due to any number of factors such as unavailability or insufficient data.

Defining the metric will help us decide the next course of action based on the model evaluation results. It should also be noted that the metric is not a fixed number, but based on the final output, the metric can be revised.

In brief, the objective should help identify:

- Target variable
- Type of analysis (Classification/Regression/Clustering)
- Metric against which the model will be evaluated
- Project team and roles and responsibility of each team member

### __Identify Data Sources__

Relevant data needs to be identified that will help answer the questions that will help in defining the objectives of the project. Identify the data source and the data that is relevant to the question that needs to be solved.

### __Hypothesis Exploration__

For most projects, you need to test your hypothesis before building the model. And for some data science projects, proving or disproving a hypothesis in itself would be the objective of the project, rather than building a model. In those cases, the hypothesis should be made as part of the objective along with the description of what question is being answered and how the conclusion from the hypothesis would affect the problem statement.

## Outputs

---

The output from this phase is the clearly defined problem statement along with a basic understanding of the data. The output artefacts from this phase are:

1. _Project Charter_

    The charter document captures the objectives that are identified in this phase of the life-cycle. The charter is a live document. The key is to update the charter document, as the project progresses through the life-cycle. The customers and stakeholders needs to be informed of the changes to the charter document along with the rationale for the change.

2. _Raw Data source and dictionary_

    Document the source and location of the raw data along with a data dictionary that defines data parameters in the raw data.

3. _Requirement Specification Document (Optional)_

    If the customer or stakeholder has well defined requirements that need to be implemented as part of the data science solution, then those can be captures in a formal “Requirement Specification Document”.

## Exit Criteria

---

This phase will be considered done when:

1. Project charter is generated, reviewed and signed-off by the relevant stakeholders.

2. Raw data source and location are identified and documented along with the raw data dictionary.

## Controls

---

The following table provides the list of controls that apply to the Business Understanding phase

| Reference No. | Document Name                                 | Type      | Mandatory   |
|---------------|-----------------------------------------------|-----------|-------------|
| DS-BU-G-00X   | Guideline for defining the project objectives | Guideline | Per Project |
| DE-DD-S-00X   | Standard for defining the Data Dictionary     | Standard  | Y           |
| DS-BU-T-00X   | Template for Project Charter                  | Template  | Y           |
| DS-BU-S-00X   | Standard for writing technical requirement    | Standard  | Per Project |

__TODO:__

- [ ] Update Revision History, Date, Reviewer, Approver
- [ ] Update Definitions Table
- [ ] Add links to the table under Controls section
- [ ] Remove TODO list before committing.

---
Copyright (c) 2020 R<sup>2</sup> Data Labs, Rolls-Royce plc

---
