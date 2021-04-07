# 1. Delete Group

## 1.1 Brief Description
Delete Group is the "Delete" - part of the CRUD "manage Group".
The right to delete a group is reserved to members of the group with the role 'owner'.


# 2. Flow of Events
## 2.1 Basic Flow
- owner clicks on "group settings" button
- owner clicks on "delete group" button and will be sent back to the front page - this action will delete the group entity
### 2.1.1 Activity Diagram
![](https://github.com/placetobeer/documentation/blob/master/use_cases/manage_group_delete_group/delete_group.png)
### 2.1.2 Mock-up
#### groupsettings - owner 
This view includes the delete button (right top).

![](https://github.com/placetobeer/documentation/blob/master/use_cases/ui-mockups/groupsettings-owner.png)
### 2.1.3 Narrative
Click [here](https://github.com/placetobeer/ptb-cucumber/blob/master/target/test-classes/features/deleteGroup.feature) to see in code!
```gherkin
Feature: Delete Group
  As a owner of a group
  I want to delete that group

  Scenario Outline: Delete group successfully, while owner has membership in other group
    Given I am logged in
    When I select the <to delete group> group
    Then It should show the hubpage of <group name> group
    And I click on the edit group button
    Then It should show the edit group site with the delete button
    When I click on the delete button
    Then It will show the "are you shure to delete" dialog popup
    When I click on the ok button
    Then It should show the "group was deleted" message
    When I click on the ok button
    Then It should close the popup
    And It should show the placeholder hubpage


    Examples:
      | to delete group |
      | study-buddies   |
      
```

## 2.2 Alternative Flows
(n/a)

# 3. Special Requirements
(n/a)

# 4. Preconditions
tbd

# 5. Postconditions
(n/a)
 
# 6. Extension Points
(n/a)



