
# ﻿PlaceToBeer - Software Requirements Specification

## Table of Contents



-   [Flashcard Community - Software Requirements Specification](#flashcard-community---software-requirements-specification)



    -   [Table of Contents](#table-of-contents)



    -   [1. Introduction](#1-introduction)



        -   [1.1 Purpose](#11-purpose)

        -   [1.2 Scope](#12-scope)

        -   [1.3 Definitions, Acronyms and Abbreviations](#13-definitions-acronyms-and-abbreviations)

        -   [1.4 References](#14-references)

        -   [1.5 Overview](#15-overview)



    -   [2. Overall Description](#2-overall-description)

		

		 -   [2.1 Vision](#21-vision)

		 -   [2.2 Use Case Diagram](#22-use-case-diagram)

		 -   [2.3 Technology Stack](#23-technology-stack)



    -   [3. Specific Requirements](#3-specific-requirements)



        -   [3.1 Functionality](#31-functionality)

        -   [3.2 Usability](#33-usability)



        -   [3.3 Reliability](#34-reliability)



        -   [3.4 Performance](#35-performance)



        -   [3.5 Supportability](#36-supportability)



        -   [3.6 Design Constraints](#37-design-constraints)



        -   [3.7 Online User Documentation and Help System Requirements](#38-online-user-documentation-and-help-system-requirements)



        -   [3.8 Purchased Components](#39-purchased-components)



        -   [3.9 Interfaces](#310-interfaces)



            -   [3.9.1 User Interfaces](#3101-user-interfaces)

            -   [3.9.2 Hardware Interfaces](#3102-hardware-interfaces)

            -   [3.9.3 Software Interfaces](#3103-software-interfaces)

            -   [3.9.4 Communications Interfaces](#3104-communications-interfaces)



        -   [3.10 Licensing Requirements](#311-licensing-requirements)



        -   [3.11 Legal, Copyright and other Notices](#312-legal-copyright-and-other-notices)



        -   [3.12 Applicable Standards](#313-applicable-standards)



    -   [4. Supporting Information](#4-supporting-information)



## 1. Introduction



### 1.1 Purpose

In the following Software Requirements Specification (SRS) functional and quality requirements for the webapplication PlaceToBeer will be descriped.


### 1.2 Scope
The PlaceToBeer Webapplication contains several subsystems. The account system guarantees a user to be recognized every time logging in. The group system manage to put users together so they can add and rate places using the rating system. Last but not least the suggestion generator allows to pick one place to visit the next time meeting your friends group.



### 1.3 Definitions, Acronyms and Abbreviations



| abbreviation| |
| -------- | -------- |
| **SRS**  | Software Requirements Specification |
| **UCS**   | Use Case Specification |
| **VM**   | Virtual Machine |

<!--
| **API**  | Application Programming Interface   |
| **MTBF** | Mean Time Between Failures          |
| **MTTR** | Mean Time To Repair                 |
| **DTO**  | Data Transfer Object                |
| **HTTP** | Hypertext Transfer Protocol         |
| **FAQ**  | Frequently Asked Questions          |
| **REST** | Representational State Transfer     |
-->


### 1.4 References



| Title                                                                                                 | Date       |
| ---------- | ---------- |
| [Blog](https://placetobeer475840703.wordpress.com/)                                         | 19/10/2020 |
| [GitHub](https://github.com/placetobeer)                                                              | 19/10/2020 |
| [Use Case Diagram](https://github.com/placetobeer/documentation/blob/master/PlaceToBeer%20UCD.png)    | 19/10/2020 |
<!--
| [Spring Boot](n/a)                                                                                    | (n/a)      |
| [ReactJS](https://reactjs.org/)                                                                       | (n/a)      |
-->




### 1.5 Overview
The following chapter of the SRS describes precisely the professional requirements of the project. With the help of a Use Case Diagram we name all events and their relations. The third chapter defines the functionalities and interfaces, as well as the desired performance of the webapplication. To end up and make the SRS easier to use the last chapter adds supporting information.

## 2. Overall Description



### 2.1 Vision

PlaceToBeer is a webbased platform to propose and rate places and events in your friend group. The idea is to individually rate bars, pubs, clubs, restaurants or wherever you can have fun together located in Karlsruhe.



In the webapp you can create and manage groups with different users. All users should be able to submit newly discovered places to hang out. Each group member can rate places so "best-of" lists can be generated. Automatic suggestions can be generated based on ratings and set filters. After the visit, every member can give a further and more specific rating, which serves to fill another "best-of" list.



### 2.2 Use Case Diagram
![](https://github.com/placetobeer/documentation/blob/master/PlaceToBeer%20UCD.png)

### 2.3 Technology Stack



#### 2.3.1 Frontend

- Framework: Angular 2.0
- Language: TypeScript
- IDE: WebStorm
- Testing: Jasmine Unit Tests
- Test coverage report: Istanbul (Karma)



#### 2.3.2 Backend

- Framework: Spring
- Language: Kotlin
- IDE: IntellJ
- Testing: JUnit4
- Test coverage report: Jacoco
- Database: H2



#### 2.3.2 Projectmanagement

- Project management tool: YouTrack
- Version control: Git and GitHub
- CI builduing tool: GitHub actions
- Test coverage & code analysis: codacy
- Organizing: Evernote
- Presentation tool: ZOHO show


## 3. Specific Requirements



### 3.1 Functionality
The project includes the following subsystems. Below the brief description of the systems links to the associated use case specifications (UCS) are provided.

#### 3.1.1 Account system
A user can register an account and change the acccount settings. On the login the saved credentials will be verified. The data is saved in a database.

##### UCS
- CRUD manage account
- login/logout

#### 3.1.2 Group system
Each user has the possibilty to create groups. The user can then invite already registered users or invite new ones by a generated email. The creater receives the owner role for the group. Following group roles exists:
- Owner:
	The owner has full rights to modify all group settings. This includes granting and revoking admin roles and deleting     the group.
 - Admin:
    An admin extends the rights of the regular member by being able to remove other admins and members from the group.
  - Member:
    This is the default role for all newly added users. They can modify the group name and invite users. Of course they can leave the group at any time.

##### UCS
- [CRUD manage group](https://github.com/placetobeer/ptb-documentation/blob/master/use-cases/manage_group/manageGroup.md)
- [delete group](https://github.com/placetobeer/ptb-documentation/blob/master/use-cases/manage_group_delete_group/deleteGroup.md)
- [manage admin role](https://github.com/placetobeer/ptb-documentation/blob/master/use-cases/manage_group_memberships/manageAdminRole.md)
- [kick member (update group membership)](https://github.com/placetobeer/ptb-documentation/blob/master/use-cases/manage_group_memberships/KickMember.md)
- [CR(U)D manage group memberships](https://github.com/placetobeer/ptb-documentation/blob/master/use-cases/manage_group_memberships/manageGroupMemberships.md)

#### 3.1.3 Rating system:
Each group member should be able to add locations to the rating list. The rating list contains every proposal ready to be rated. It is devided into two sublists:
- The <b>unvisited proposals</b> can be marked with "thumbs-up", "neutral", or "thumbs-down". This rating should be based on one's very first impression and indicates the group's attitude towards a proposal.
- The <b>visited proposals</b> can be rated using a 1 to 5 stars system based on experiences. All this information is used to generate two best-of lists which will be displayed on the dashboard.

The rating workflow starts with the possibility to add a proposal. During this process the user can set the name of the proposal, define the kind of activity (bar, restaurant, etc.), the address, and if it has already been visited. Furthermore, one can choose to which group or groups the location should be proposed. Depending on the selected "visited" status, the location is ordered in the fitting rating sublist.
After the rating process described above they are moved to the corresponding best-of list. The **best-of unvisited proposals** list offers to mark proposals as "already visited". If done so, the proposal returns to the **rating list** but will now appear in the **unvisited proposals** list.

The whole dashboard can be filtered by the activity of the proposal.

##### UCS
- [create proposal](https://github.com/placetobeer/ptb-documentation/blob/master/use-cases/create_proposal/createProposal.md)
- [rate proposal](https://github.com/placetobeer/ptb-documentation/blob/master/use-cases/rate_proposal/rateProposal.md)

#### 3.1.4 Suggestion generation system
This system can be used by a group to automatically generate a suggestion depending on the ratings. Any member can initialize this process. To personalize the results to the groups preferences filters can be used to select specific kinds of activities. Moreover it is possible to decide between visited and unvisited proposals.

#### 3.1.5 Group navigation system
A user can switch between the groups he or she is a member of. The system offers possibilities to accept and decline group invitations and create new groups.

### 3.2 Usability
The goal is to make the webapplication as intuitive as possible. To achieve this the control over the platform simultates the behavior of common applications. The user interface provides known icons and items are placed in an accustomed way.

The required time for a normal user to get used to all features and get an overview of the offered possibilities should be 15 minutes. A group owner may need 10 minutes more to figure out how to handle the group system. 


### 3.3 Reliability
The general availability should be at least 95%. This can be achieved by start and monitoring scripts:
- Once a day, ideally when there is the lowest traffic, the whole application should be restarted.
- If a component crashes, the application should also be restarted automatically. However, if this happens several times in a row (e.g. 5 times), the restart attempts should be stopped and the system admin should be informed (e.g. via email).
- In general, all start and restart activities and the general output of the application should be logged. This will help the system admin to find out more quickly what the problem is in case of a fatal error.

Since the frontend, backend and database are all expected to run on the same system, communication problems between the systems must be eliminated.

### 3.4 Performance
The response time should be kept as short as possible. It is not yet possible to give exact details, the application should still approach the average 3.5 ms. However, since all components run on the same virtual machine (VM), the latencies between the systems can be estimated to be close to zero.

The total memory management should be able to store up to 1000 users and 100 groups. The actual system throughput for simultaneous use should be 100 users.

These values are initial estimates. During the deployment phase and the testing of the actual system, it will become clear to what extent the resources provided can cope with the requirements.

### 3.5 Supportability
Once the development begins we will start to define clean code standarts, naming conventions and other measurements to preserve the supportability of our project.

### 3.6 Design Constraints
tbd

### 3.7 Online User Documentation and Help System Requirements
tbd

### 3.8 Purchased Components
tbd

### 3.9 Interfaces


#### 3.9.1 User Interfaces
- start page
	- description of the webapplication
	- register field
	- login field
- hubpage
	- header: icon to generate automatic suggestion; icon to open accountsettings
	- group navigation bar (on the right)
	- rating area: header to filter by activities; three columns with the best of and rating  lists
- add proposal
- suggestion generator
- account settings
- group settings



#### 3.9.2 Hardware Interfaces
(n/a)

#### 3.9.3 Software Interfaces
We plan to develop our Webapp based on test results using the current version of Google Chrome and Firefox. So users should have one of these browsers installed to guarantee that the software will work as intended.

#### 3.9.4 Communications Interfaces
The web application will run on a single VM, with its own memory and hardware. Therefore, there are no exact interfaces to be defined.

### 3.10 Licensing Requirements
tbd

### 3.11 Legal, Copyright and other Notices
tbd

### 3.12 Applicable Standards
tbd

## 4. Supporting Information
Further information is provided in our [blog](https://placetobeer475840703.wordpress.com/) .
To contact the PlaceToBeer visit our [contact page](https://placetobeer475840703.wordpress.com/contact/) or send us an email at *project.placetobeer@gmail.com*.
