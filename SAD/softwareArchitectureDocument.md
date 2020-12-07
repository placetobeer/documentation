
# Software Architecture Document


## 1. Introduction 

### 1.1 Purpose

This document provides a comprehensive architectural overview of the system, using a number of different architectural views to depict different aspects of the system. It is intended to capture and convey the significant architectural decisions which have been made on the system.

### 1.2 Scope
The document applies to the project PlaceToBeer. Detailed information about the project can be found in the [SRS](https://github.com/placetobeer/ptb-documentation/blob/master/SRS.md).



### 1.3 Definitions, Acronyms and Abbreviations



| abbreviation| |
| -------- | -------- |
| **SRS**  | Software Requirements Specification |
| **UCS**   | Use Case Specification |
| **MVC** | Model View Controller |
| **(n/a)** | not applicable



### 1.4 References



| Title                                                                                                 | Date       |
| ---------- | ---------- |
| [Blog](https://placetobeer475840703.wordpress.com/)                                         | 19/10/2020 |
| [GitHub](https://github.com/placetobeer)                                                              | 19/10/2020 |
| [Use Case Diagram](https://github.com/placetobeer/documentation/blob/master/PlaceToBeer%20UCD.png)    | 19/10/2020 |
| [SRS](https://github.com/placetobeer/ptb-documentation/blob/master/SRS.md) | 07/12/2020
### 1.5 Overview
In the following chapters different views on the project are described by the help of several diagrams. It contains the architectural, use case, logical, deployment and data view. 

## 2. Architectural Representation
This project's architecture is based on the MVC - Pattern. Both Spring in the back-end and Angular in the front-end are structured in the following way:

![Model View Controller](https://github.com/placetobeer/ptb-documentation/blob/master/SAD/MVC-schema-overview.png) 
[Source](https://www.techyourchance.com/wp-content/uploads/2015/06/MVC_MVP.png)

Thereby the back-end's controller has access on the database and the back-end's View represents the whole front-end (which is a MVC itself).
## 3. Architectural Goals and Constraints 
### Back-end
For the back-end the framework of our choice is Spring Boot, which does support all aspects of MVC (whereby the controllers are included in Spring Web). To access the H2 - database we are using Spring JPA and String Security is planned to manage the account system. 
### Front-end
For the frontend we use Angular so no extra MVC-tools are needed.
## 4. Use Case View 
![Overall use case diagramm](https://github.com/placetobeer/ptb-documentation/blob/master/PlaceToBeer%20UCD.png)
## 5. Logical View
![MVC-with-classes](https://github.com/placetobeer/ptb-documentation/blob/master/SAD/MVC-Ptb.png)
## 6. Process View
(n/a)

## 7. Deployment View
![Deployment View](https://github.com/placetobeer/ptb-documentation/blob/master/SAD/deploymentView.png)
## 8. Implementation View
### 8.1 Overview
(n/a)
### 8.2 Layers
(n/a)
## 9. Data View
#### Backend class diagram
![Backend class diagram](https://github.com/placetobeer/ptb-documentation/blob/master/classDiagram.png)
#### Database schema
##### Entity Relationship Model
![ERM](https://github.com/placetobeer/ptb-documentation/blob/master/DBMS/groupSystem.png)
##### Relational Database Model
![rDBM](https://github.com/placetobeer/ptb-documentation/blob/master/DBMS/groupSystem_rDBM.png)
## 10. Size and Performance
(n/a)

## 11. Quality
(n/a)
