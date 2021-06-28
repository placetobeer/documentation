# Test plan

- [Test plan](#test-plan)
    - [1. Introduction](#1-introduction)
        - [1.1 Purpose](#11-purpose)
        - [1.2 Scope](#12-scope)
        - [1.3 Intended Audience](#13-intended-audience)
        - [1.4 Document Terminology and Acronyms](#14-document-terminology-and-acronyms)
        - [1.5  References](#15--references)
        - [1.6 Document Structure](#16-document-structure)
    - [2. Evaluation Mission and Test Motivation](#2-evaluation-mission-and-test-motivation)
        - [2.1 Background](#21-background)
        - [2.2 Evaluation Mission](#22-evaluation-mission)
        - [2.3 Test Motivators](#23-test-motivators)
    - [3. Target Test Items](#3-target-test-items)
    - [4. Outline of Planned Tests](#4-outline-of-planned-tests)
        - [4.1 Outline of Test Inclusions](#41-outline-of-test-inclusions)
        - [4.2 Outline of Other Candidates for Potential Inclusion](#42-outline-of-other-candidates-for-potential-inclusion)
        - [4.3 Outline of Test Exclusions](#43-outline-of-test-exclusions)
    - [5. Test Approach](#5-test-approach)
        - [5.1 Testing Techniques and Types](#51-testing-techniques-and-types)
            - [5.1.1 Unit Testing](#511-unit-testing)
            - [5.1.2 User Interface Testing](#512-user-interface-testing)
            - [5.1.3 Integration Testing (API Testing)](#513-integration-testing-api-testing)
    - [6. Entry and Exit Criteria](#6-entry-and-exit-criteria)
        - [6.1 Test Plan](#61-test-plan)
            - [6.1.1 Test Plan Entry Criteria](#611-test-plan-entry-criteria)
            - [6.1.2 Test Plan Exit Criteria](#612-test-plan-exit-criteria)
    - [7. Deliverables](#7-deliverables)
        - [7.1 Test Evaluation Summaries](#71-test-evaluation-summaries)
        - [7.2 Reporting on Test Coverage](#72-reporting-on-test-coverage)
        - [7.3 Perceived Quality Reports](#73-perceived-quality-reports)
        - [7.4 Incident Logs and Change Requests](#74-incident-logs-and-change-requests)
        - [7.5 Smoke Test Suite and Supporting Test Scripts](#75-smoke-test-suite-and-supporting-test-scripts)
    - [8. Testing Workflow](#8-testing-workflow)
    - [9. Environmental Needs](#9-environmental-needs)
        - [9.1 Base System Hardware](#91-base-system-hardware)
        - [9.2 Base Software Elements in the Test Environment](#92-base-software-elements-in-the-test-environment)
        - [9.3 Productivity and Support Tools](#93-productivity-and-support-tools)
    - [10. Responsibilities, Staffing, and Training Needs](#10-responsibilities-staffing-and-training-needs)
        - [10.1 People and Roles](#101-people-and-roles)
        - [10.2 Staffing and Training Needs](#102-staffing-and-training-needs)
    - [11. Iteration Milestones](#11-iteration-milestones)
    - [12. Risks, Dependencies, Assumptions, and Constraints](#12-risks-dependencies-assumptions-and-constraints)
    - [13. Management Process and Procedures](#13-management-process-and-procedures)

## 1. Introduction

### 1.1 Purpose

This Test Plan's purpose is to deliver all the information necessary to steadily plan and supervise tests for the software. Here, different approaches to testing are described.

The following objectives are covered:

- Describe what items should be tested and explain the reason for that.

- Identifies the motivation for and ideas behind the test areas to be covered.

- Outline what different ways are taken to test those areas.

- Identifies the required resources and provides an estimate of the test efforts.

-tbd
### 1.2 Scope

This test plan will cover tests assuring the functionality of the application's front end, back end and the communication between the two.

This document shows the following types of testing:

- API-Tests

- Unit tests & Integration tests

- User tests


### 1.3 Intended Audience

Since this document's purpose is to provide orientation to the developers to work from and as a documentation to measure the fullfillment of quality requirements against, it is meant for internal use.

### 1.4 Document Terminology and Acronyms

| Abbr | Abbreviation                        |
|------|-------------------------------------|
| tbd  | to be determined                    |
| UC   | Use Case                            |
| SRS  | Software Requirements Specification |
| SAD  | Software Architecture Document      |
| API  | Software Architecture Document      |
| HTTP | Hypertext Transfer Protocol         |


### 1.5  References

| Title                                                                   | Date       | Publishing organization   |
| ------------------------------------------------------------------------|:----------:| ------------------------- |
| [Blog](https://placetobeer475840703.wordpress.com/)                     | 2020       | PlaceToBeer               |
| [GitHub Repository](https://github.com/placetobeer)                     | 2020       | PlaceToBeer               |
| [UC create_proposal](https://github.com/placetobeer/ptb-documentation/tree/master/use-cases/create_proposal)               | 2021   | PlaceToBeer               |
| [UC filter_view_by_activities](https://github.com/placetobeer/ptb-documentation/tree/master/use-cases/filter_view_by_activities)               | 2021  | PlaceToBeer               |
| [UC manage_group](https://github.com/placetobeer/ptb-documentation/tree/master/use-cases/manage_group)            | 2020  | PlaceToBeer               |
| [UC manage_group_delete_group](https://github.com/placetobeer/ptb-documentation/tree/master/use-cases/manage_group_delete_group)             | 2020  | PlaceToBeer               |
| [UC manage_group_memberships](https://github.com/placetobeer/ptb-documentation/tree/master/use-cases/manage_group_memberships)                                  | 2021  | PlaceToBeer               |
| [UC rate_proposal](https://github.com/placetobeer/ptb-documentation/tree/master/use-cases/rate_proposal)                                |  2021  | PlaceToBeer               |
| [Test Plan](https://github.com/placetobeer/ptb-documentation/tree/master/test-plan/TestPlan.md)                                              | 2021  | PlaceToBeer               |
| [SRS](https://github.com/placetobeer/ptb-documentation/blob/master/SRS.md)                          | 2020  | PlaceToBeer               |
| [SAD](https://github.com/placetobeer/ptb-documentation/blob/master/SAD/softwareArchitectureDocument.md)                               | 2020  | PlaceToBeer               |

### 1.6 Document Structure

n/a

## 2. Evaluation Mission and Test Motivation

### 2.1 Background

Testing is crucial to ensure keeping the quality of code up as well as making sure all the functionalities do work just as they are supposed to, after every implementation step.
### 2.2 Evaluation Mission

[comment]: <> (Testing is a crucial phase in the development cycle. It is necessary in order to fix technical bugs and important functional problems. With TDD we define the test first and can fix bugs before they even occur.)
This test plan serves to describe what we have to do to prevent any failures during the implementation or alteration of code.
### 2.3 Test Motivators

[comment]: <> (The tests are done to ensure quality and mitigate risks and fulfill functional requirements. Their purpose is to provide stability for our application.)
The reason these tests are done is to:
- ensure quality
- mitigate risks
- fulfill requirements
## 3. Target Test Items
Items for Testing:
- SpringBoot - Backend
- Angular - Frontend

[comment]: <> (- Android frontend)

[comment]: <> (- Server backend &#40;and APIs&#41;)

## 4. Outline of Planned Tests

### 4.1 Outline of Test Inclusions
*Frontend: Angular*:

- Installation testing

*Backend: Spring Boot Application*:

- Unit testing
- API testing (Integration testing)

The tests themself will not be tested and will not account into code coverage.


### 4.2 Outline of Other Candidates for Potential Inclusion

n/a

### 4.3 Outline of Test Exclusions
We will not do:

- UI tests
- Stress test
- Load/performance tests
- Usability tests
- any further tests

## 5. Test Approach

### 5.1 Testing Techniques and Types

#### 5.1.1 Unit Testing

Unit testing means, that small parts of the sourcecode are tested independently. This ensures, that the core code works properly.
This does mostly apply to the backend.

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    | The implemented code should work as expected                  |
|Technique              | Create test methods using JUnit and Mockito   |
|Oracles                | Test execution logs results to the IDE's command line, logs in CI/CD Tool (Codacy) |
|Required Tools         | JUnit Dependencies in Backend                    |
|Success Criteria       | All tests pass. Coverage is above 10% (Frontend) / 80% (Backend)    |
|                       | CI/CD Pipeline with test stages for Backend: [Codacy](https://app.codacy.com/gh/placetobeer/ptb-backend/dashboard?branch=master)|
|Special Considerations | -                                                                   |

#### 5.1.2 Installation Testing

By Installation Testing a person, who has in no way got in contact with the project before, gegt's handed the project's current stand and tries to install and use it.

|                       | Description                                                          |
|-----------------------|----------------------------------------------------------------------|
|Technique Objective    | Test the frontend composition and logical connections by an external user |
|Technique              | Creating an installation guide and test cases which cover the critical functionalities of the project - add what is expected to happen|
|Oracles                | Save Protocols/ filled out Formulars of users |
|Required Tools         | MS Forms |
|Success Criteria       | All test cases are marked as "works"
|Special Considerations | - |

#### 5.1.3 Integration Testing (API Testing)

API testing is a part of integration Testing as it tests multiple components of the backends together. Here we make sure the communication from Backend-Server to the frontend works as expected.

|                       | Description                                                          |
|-----------------------|----------------------------------------------------------------------|
|Technique Objective    | Test the provided Apis using Swagger                                 |
|Technique              | We can check out every meaningful api with with test data and see if the http messages contain the expected information   |           
|Oracles                | Backend gets filled with (fake) mockup data and check if the result gets simulated correctly in the Swagger Overview |
|Required Tools         | Swagger                                     |
|Success Criteria       | All tests pass.                               | |
|Special Considerations | -                                                                    |

## 6. Entry and Exit Criteria

### 6.1 Test Plan

#### 6.1.1 Test Plan Entry Criteria

Pushing new commits to gitHub on the master branch in the backend will trigger the CI/CD pipeline

#### 6.1.2 Test Plan Exit Criteria

All tests pass without an exception

## 7. Deliverables

## 7.1 Test Evaluation Summaries


<!--
The project owns a certain amount of tests in the Frontend and Backend. Each pushed commit triggers our CI/CD Pipeline, which builds the application and executes the tests. Furthermore a code analysis with Codacy is triggered. We use a monorepo which includes the docs and the sourcecode for our Backend and Frontend. That´s why we have one CI/CD Pipeline for our whole project. 

Continuous Integration/Delivery/Deployment Pipeline based on Travis CI: [Travis CI](https://travis-ci.com/nilskre/CommonPlayground) [![Build Status](https://travis-ci.com/nilskre/CommonPlayground.svg?branch=master)](https://travis-ci.com/nilskre/CommonPlayground)

Code Analysis with Codacy: [Codacy](https://app.codacy.com/project/DRiXD/CommonPlayground/dashboard) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/aff81896be354fc48280efd8135fb3ef)](https://app.codacy.com/app/DRiXD/CommonPlayground?utm_source=github.com&utm_medium=referral&utm_content=nilskre/CommonPlayground&utm_campaign=Badge_Grade_Settings)

CI/CD Pipeline stages: Build, Test, Deploy(only on the master branch):  
![CI/CD Pipeline stages: Build, Test, Deploy(only on the master branch) ](./CICD_stages.png)  
Integration of CI/CD Pipeline pipeline with github:  
![Integration of CI/CD Pipeline pipeline with github](./CICD_github_commits.png)  
Frontend IDE test execution:  
![Frontend IDE test execution](./frontend_test_execution.png)  
Backend IDE test execution:  
![Backend IDE test execution](./backend_test_execution.png)
-->
tbd
## 7.2 Reporting on Test Coverage

In the backend we use Jacoco to generate the reports. In the frontend the reports are generated with Istanbul which is a tool of Karma. The reports are then sent to codacy which analyses them and creates a badge:
[
![Codacy Badge](https://app.codacy.com/project/badge/Coverage/28956f6679584cbf86e940ccba27ece5)](https://www.codacy.com/gh/placetobeer/ptb-backend/dashboard?utm_source=github.com&utm_medium=referral&utm_content=placetobeer/ptb-backend&utm_campaign=Badge_Coverage)

## 7.3 Perceived Quality Reports
The code quality is guaranteed through the tool codacy as well.

 [![Codacy Badge](https://app.codacy.com/project/badge/Grade/28956f6679584cbf86e940ccba27ece5)](https://www.codacy.com/gh/placetobeer/ptb-backend/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=placetobeer/ptb-backend&amp;utm_campaign=Badge_Grade)
 
**Metrics**
During the automated deployment process codacy calculates different metrics:
- cylomatic complexity
- duplication

Based on the results of the metrics the code is refactored regularly.

## 7.4 Incident Logs and Change Requests
<!--
We integrated the tools mentioned above into our GitHub pull request workflow. If a build fails this is directly visible in the PR. Furthermore the team is alerted by an email.
The screenshot shows the integration:

![GitHub PR integrated tools](./integrated_tools.png)
-->
tbd
## 7.5 Smoke Test Suite and Supporting Test Scripts
With the automated test execution in the CI/CD Pipeline we ensure to immediatly check if a functionality doesn't work any more when changes are made.

## 8. Testing Workflow
Every team member does run all tests local in the IDE before commiting and
Commit and Push triggers build and test exection in the CI/CD Pipeline
Each PR triggers the pipeline (build and test)????

## 9. Environmental Needs

### 9.1 Base System Hardware

The following table sets forth the system resources for the test effort presented in this Test Plan.

| Resource              | Quantity | Name and Type                |
|-----------------------|:--------:|------------------------------|
| CI/CD server          |    1     | Codacy Cloud                 |
| local test machine    |    1     | Windows PC        |

### 9.2 Base Software Elements in the Test Environment

The following base software elements are required in the test environment for this Test Plan.

| Software Element Name |  Type and Other Notes                        |
|-----------------------|----------------------------------------------|
| IntelliJ              | Test Runner / IDE                            |
| JUnit                 | Unit testing library                         |
| Swagger               | API Documentation/ Testing Tool              |

### 9.3 Productivity and Support Tools

The following tools will be employed to support the test process for this Test Plan.

| Tool Category or Type | Tool Brand Name                              |
|-----------------------|----------------------------------------------|
| Repository            | [github.com](http://github.com/)             |
| Test Coverage Monitor | [codacy](https://app.codacy.com/)            |
| CI/CD Service         | GitHub Actions   |
| Metrics Tool          | [codacy](https://app.codacy.com/)            |

## 10. Responsibilities, Staffing, and Training Needs

### 10.1 People and Roles

| Role          | Person Assigned |  Specific Responsibilities or Comments |
|---------------|:--------------:|----------------------------------------|
| Test Manager | Tom  | Keeps track of the testing processes |

[comment]: <> (| Test Designer | Denis, Celina | Defines the technical approach to the implementation of the test effort. |)

[comment]: <> (| Test System Administrator | Nils | Ensures test environment and assets are managed and maintained. |)

### 10.2 Staffing and Training Needs

n/a

## 11. Iteration Milestones

We want to keep over 80% code coverage.

## 12. Risks, Dependencies, Assumptions, and Constraints

| Risk | Mitigation Strategy | Contingency (Risk is realized) |
|------|---------------------|--------------------------------|
|Fundamental issues in code base|code review; early and regularly refactoring; pair programming|Check in logs or repository to fix bugs|

[comment]: <> (| Code has lots of side effects | Refactor code &#40;Clean Code principles&#41; | publish new refactored tests |)

[comment]: <> (| Test Runner is not able to execute tests | Use standard libraries which include working Test Runner | fix test execution configuration |)

[comment]: <> (| UI tests fail | Refactor test | publish refactored test and restart |)

## 13. Management Process and Procedures

n/a
