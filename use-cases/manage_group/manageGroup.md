# 1. Manage Group

## 1.1 Brief Description
Manage group covers the creation, reading, updating and deleting of a group (CRUD). But not all use cases of the CRUD 'manage group' can be fullfilled by every role. Therefore we decided to seperate the delete part and one update use case for which both require the 'admin' role at least. The update use case covers the possiblity to invite new members. Further changes in the entity are preserved to the 'owner' and 'admin' role.


# 2. Flow of Events
![Flow of Events CRUD](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/manage_group/flow_of_event_CRUD.png)
## 2.1 Create
* User clicks on "create group" button
* User fills the "create group" page - title, adding members (optional)
- User clicks on "create" button and will be forwarded to the group's hubpage
- User clicks on "cancel" button and will be sent back to the page he or she visited before
### 2.1.1 Activity Diagram
![Create Group](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/manage_group/create_group.png)
### 2.1.2 Mock-up
##### Group navigation bar
![Group navigation bar](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/ui-mockups/groupNavigationBar.png)
##### Create group
![Create group](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/ui-mockups/createGroup.png
)
##### Create group - error input
![create group error](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/ui-mockups/createGroupError.png)

### 2.1.3 Narrative
Click [here](https://github.com/placetobeer/ptb-cucumber/blob/master/target/test-classes/features/createGroup.feature) to see in code!
```gherkin
Feature: Create group  
  As a USER  
  I want to create a group with at least two members  
  
  Scenario Outline: create group successfully  
    Given I am logged in and open the create group site  
    When I fill in the <group name> field  
    And I click on the create button  
    Then the app should create a new group with the input values  
    And send the data to the backend  
    And return to the hubpage  
  
    Examples:  
      | group name | email |  
      | study-buddies | project.placetobeer@gmail.com | 
  
 Scenario Outline: user tries to add member which is already in group  
    Given I am logged in and open the create group site  
    When I fill in the <group name> field  
    And I fill in the <email> field  
    And I click on the add to group button  
    And I fill in the <email> field the same email address as before  
    And I click on the add to group button  
    Then error message of the member being already in the group  
  
    Examples:  
      | group name | email |  
      | study-buddies | project.placetobeer@gmail.com |
```

## 2.2 Read
- User clicks on "group settings" button
- User can see the name of the group, the descripiton, the defined settings, and the list of group members
- User clicks on "cancel" button and will be sent back to the page he or she visited before
### 2.2.1 Activity Diagram
### 2.1.2 Mock-up
##### Group settings - owner view
![Group settings - owner view](https://github.com/placetobeer/ptb-documentation/blob/master/use-cases/ui-mockups/groupsettings-owner.png)
##### Group settings - admin view
![Group settings - admin view](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/ui-mockups/groupsettings-admin.png)
##### Group settings - member view
![Group settings - member view](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/ui-mockups/groupsettings-owner.png)


### 2.1.3 Narrative

## 2.3 Update
- User clicks on "group settings" button
- User clicks on "Edit" button next to the group name to type in a new group name
- User clicks on "add member" button
- User fills the form with the person's email - the system checks if the email is already registered or the without an account
- User clicks on "invite" button and will be sent back to the "group settings" page - the system sends an invitation email
### 2.3.1 Activity Diagram
![Add Member](https://github.com/placetobeer/documentation/blob/master/use_cases/manage_group/add_member.png)
### 2.3.2 Mock-up
Mock-ups for group settings same as mock-ups for read view (compare 2.1.2).

##### Add member pop-up
![Add Member Pop-Up](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/ui-mockups/addMember.png)
### 2.3.3 Narrative
Click [here](https://github.com/placetobeer/ptb-cucumber/blob/master/target/test-classes/features/updateGroup.feature) to see in code!
```gherkin
Feature: Update Group  
  As a MEMBER  
  I want to update a group entity I am a member of  
  
  Scenario Outline: change name  
    Given I opened page "groupSettings"  
    And I am logged in as a member of the group  
    When I click button "editGroupName"  
    And I enter <new name> in the input "changeName"  
    When I press enter or click button "apply"  
    Then the group should have name <new name>  
  
    Examples:  
      | new name |  
      | name2 	 |  
  
  
 Scenario Outline: add member successfully  
    Given I opened page "groupSettings"  
    And I am logged in as a member of the group  
    When I click button "addMember"  
    When I enter <email address> in the input "newMember"  
    And I click button "confirmAddMember"  
    Then <email address> receives an invitation email (for this group entity)  
  
    Examples:  
      | email address 				  |
      | project.placetobeer@gmail.com |
```

```gherkin
Feature: Update Group
  As a ADMIN
  I want to update a group entity I am a member of

  Scenario Outline: add member with admin role
    Given I opened page "groupSettings"
    And I am logged in as a member of the group
    When I click button "addMember"
    When I enter <email address> in the input "newMember"
    And I check the checkbox "addAsAdmin"
    And I click button "confirmAddMember"
    Then <email address> receives an invitation email (for this group entity)

    Examples:
      | email address 				  | 
      | project.placetobeer@gmail.com |
      
```

## 2.4 Alternative Flows
(n/a)

# 3. Special Requirements
(n/a)

# 4. Preconditions
tbd

# 5. Postconditions
(n/a)
 
# 6. Function Points
FP = 76,5

![enter image description here](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/function-points/manage-group-fp.png)![enter image description here](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/function-points/fp-table2.png)



