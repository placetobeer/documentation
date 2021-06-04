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

[comment]: <> (The purpose of the Iteration Test Plan is to gather all the information necessary to plan and control the test effort for a given iteration. It describes the approach to testing the software.)

[comment]: <> (This Test Plan for PlaceToBeer supports the following objectives:)

[comment]: <> (- Identifies the items that should be targeted by the tests.)

[comment]: <> (- Identifies the motivation for and ideas behind the test areas to be covered.)

[comment]: <> (- Outlines the testing approach that will be used.)

[comment]: <> (- Identifies the required resources and provides an estimate of the test efforts.)
-tbd
### 1.2 Scope

[comment]: <> (This test plan will cover tests assuring the functionality of the application's front end, back end and the communication between the two.)

[comment]: <> (This document shows the following types of testing:)

-tbd


### 1.3 Intended Audience

[comment]: <> (This test plan is written primarily for internal documentation reasons. It is meant to provide orientation to the developers to work from and as a documentation to measure the fullfillment of quality requirements against.)

### 1.4 Document Terminology and Acronyms

| Abbr | Abbreviation                        |
|------|-------------------------------------|
| tbd  | to be determined                    |


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

[comment]: <> (Testing serves to ensure that the written code does what it is intended to do. It also prevents future code changes to break existing functionality unnoticed. In the context of integration it can also prevent broken software states to be merged into secured VC branches)
tbd
### 2.2 Evaluation Mission

[comment]: <> (Testing is a crucial phase in the development cycle. It is necessary in order to fix technical bugs and important functional problems. With TDD we define the test first and can fix bugs before they even occur.)
tbd
### 2.3 Test Motivators

[comment]: <> (The tests are done to ensure quality and mitigate risks and fulfill functional requirements. Their purpose is to provide stability for our application.)
tbd
## 3. Target Test Items

[comment]: <> (- Android frontend)

[comment]: <> (- Server backend &#40;and APIs&#41;)
tbd
## 4. Outline of Planned Tests

### 4.1 Outline of Test Inclusions
<!--
*Frontend: Android Client*:

- UI testing of views/fragments
- Unit testing

*Backend: Spring Boot Application*:

- Unit testing
- Integration testing
- Api testing

![Testing overview](./testing_overview.png)  

The tests themself will not be tested and will not account into code coverage.
-->
tbd

### 4.2 Outline of Other Candidates for Potential Inclusion

n/a

### 4.3 Outline of Test Exclusions
<!--
Because of time and resource constraints we will not do:

- Stress test
- Load/performance tests
- Usability tests
- any further tests
-->
tbd
## 5. Test Approach

### 5.1 Testing Techniques and Types

#### 5.1.1 Unit Testing
<!--
Unit testing ensures, that the tested sourcecode works as expected. Therefore small parts of the sourcecode are tested independently.

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    | Ensure that the implemented code works as expected                  |
|Technique              | Implement test methods using JUnit Framework (Frontend & Backend)   |
|Oracles                | Test execution logs results to the command line, logs in CI/CD Tool (Travis) |
|Required Tools         | JUnit 4 & 5 Dependencies in Frontend and Backend                    |
|Success Criteria       | All tests pass. Coverage is above 10% (Frontend) / 60% (Backend)    |
|                       | CI/CD Pipeline with test stages for Frontend and Backend: [Travis CI](https://travis-ci.com/nilskre/CommonPlayground)|
|Special Considerations | -                                                                   |
-->
tbd
#### 5.1.2 User Interface Testing
<!--
By UI testing the application is tested from the perspective of the user. The goal of UI testing is to ensure that the UI behaves as expected.

|                       | Description                                                          |
|-----------------------|----------------------------------------------------------------------|
|Technique Objective    | Test application automated from the perspective of the user through UI Test |
|Technique              | Writing Gherkin `.feature` files with clearly defined steps and the expected result. The test implementation of the steps use the Android Espresso library to serve the emulator. [Further information](https://commonplayground.wordpress.com/week-5-testing-with-cucumber//) |
|Oracles                | Expect that the steps of the test are executed successfully and the UI behaves as planned. Test execution logs results to the command line, logs in CI/CD Tool (Travis) |
|Required Tools         | Dependencies of Cucumber and Espresso (official Android UI test library) and an Implementation of a test runner based on JUnit 4 to execute UI tests with Cucumber and Espresso |
|Success Criteria       | All UI tests pass.
|                       | CI/CD Pipeline with test stages for Frontend and Backend: [Travis CI](https://travis-ci.com/nilskre/CommonPlayground)   |
|Special Considerations | - |
-->
tbd
#### 5.1.3 Integration Testing (API Testing)
<!--
Api Testing is part of integration testing. Integration tests test multiple modules of an application together. The main goal of Api testing is to ensure, that the provided Apis of the Backend behave as expected.

|                       | Description                                                          |
|-----------------------|----------------------------------------------------------------------|
|Technique Objective    | Test the provided Apis with Cucumber                                 |
|Technique              | For every meaningful api a Gherkin `.feature` exists and the steps are implemented.  |            |
|Oracles                | Test execution logs results to the command line, Logs in CI/CD Tool (Travis) |
|Required Tools         | JUnit, Cucumber, Rest assured, Hamcrest                                     |
|Success Criteria       | All tests pass. Coverage is above 60%                                |
|                       | CI/CD Pipeline with test stages for Frontend and Backend: [Travis CI](https://travis-ci.com/nilskre/CommonPlayground) |
|Special Considerations | -                                                                    |
-->
tbd
## 6. Entry and Exit Criteria

### 6.1 Test Plan

#### 6.1.1 Test Plan Entry Criteria

n/a

#### 6.1.2 Test Plan Exit Criteria

n/a

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
<!--
For reporting our test coverage we use Jacoco and Codacy. 

Code Test Coverage: [![Codacy Badge](https://api.codacy.com/project/badge/Coverage/7fdcfeca10b94f4c9b6bc1a809669c2b)](https://www.codacy.com/app/CommonPlayground/CommonPlayground?utm_source=github.com&utm_medium=referral&utm_content=nilskre/CommonPlayground&utm_campaign=Badge_Coverage)
-->
tbd
## 7.3 Perceived Quality Reports
<!--
The code quality tool is Codacy. [![Codacy Badge](https://api.codacy.com/project/badge/Grade/7fdcfeca10b94f4c9b6bc1a809669c2b)](https://www.codacy.com/app/CommonPlayground/CommonPlayground?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=nilskre/CommonPlayground&amp;utm_campaign=Badge_Grade)
-->
tbd
## 7.4 Incident Logs and Change Requests
<!--
We integrated the tools mentioned above into our GitHub pull request workflow. If a build fails this is directly visible in the PR. Furthermore the team is alerted by an email.
The screenshot shows the integration:

![GitHub PR integrated tools](./integrated_tools.png)
-->
tbd
## 7.5 Smoke Test Suite and Supporting Test Scripts
<!--
The automated test execution in our CI/CD Pipeline enables regression testing. With this approach it is clearly visible when changes break existing functions and affect the correct behaviour of the application.
-->
tbd
## 8. Testing Workflow
<!--
1) Local testing in the IDE
2) Commit and Push triggers build and test exection in the CI/CD Pipeline
3) Each PR triggers the pipeline (build and test)
4) Before the automated deployment the build and test stages are executed
-->
tbd
## 9. Environmental Needs

### 9.1 Base System Hardware
<!--
The following table sets forth the system resources for the test effort presented in this Test Plan.

| Resource              | Quantity | Name and Type                |
|-----------------------|:--------:|------------------------------|
| CI/CD server          |    1     | Travis CI Cloud              |
| local test machine    |    1     | notebook (Inga, Celina, Denis, Nils)       |
| Android test device   |    1     | Android device (Inga, Celina, Denis, Nils) |
-->
tbd
### 9.2 Base Software Elements in the Test Environment
<!--
The following base software elements are required in the test environment for this Test Plan.

| Software Element Name |  Type and Other Notes                        |
|-----------------------|----------------------------------------------|
| Android Studio        | Test Runner / IDE                            |
| IntelliJ              | Test Runner / IDE                            |
| JUnit 4 & 5           | Unit testing library                         |
| Espresso              | UI testing library                           |
| Cucumber              | human readable test definitions              |
-->
tbd
### 9.3 Productivity and Support Tools
<!--
The following tools will be employed to support the test process for this Test Plan.

| Tool Category or Type | Tool Brand Name                              |
|-----------------------|----------------------------------------------|
| Repository            | [github.com](http://github.com/)             |
| Test Coverage Monitor | [codacy](https://app.codacy.com/)            |
| CI/CD Service         | [Travis CI](http://travis-ci.org/)           |
| Metrics Tool          | [codacy](https://app.codacy.com/)            |
-->
tbd
## 10. Responsibilities, Staffing, and Training Needs

### 10.1 People and Roles
<!--
| Role          | Person Assigned |  Specific Responsibilities or Comments |
|---------------|:--------------:|----------------------------------------|
| Test Manager | Denis, Inga | Provides management oversight. |
| Test Designer | Denis, Celina | Defines the technical approach to the implementation of the test effort. |
| Test System Administrator | Nils | Ensures test environment and assets are managed and maintained. |
-->
tbd
### 10.2 Staffing and Training Needs

n/a

## 11. Iteration Milestones

We want to keep over 80% code coverage.

## 12. Risks, Dependencies, Assumptions, and Constraints
<!--
| Risk | Mitigation Strategy | Contingency (Risk is realized) |
|------|---------------------|--------------------------------|
| Code has lots of side effects | Refactor code (Clean Code principles) | publish new refactored tests |
| Test Runner is not able to execute tests | Use standard libraries which include working Test Runner | fix test execution configuration |
| UI tests fail | Refactor test | publish refactored test and restart |
-->
tbd
## 13. Management Process and Procedures

n/a
