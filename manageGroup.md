# 1. Manage Group

## 1.1 Brief Description
Manage group covers the creation, reading, updating and deleting of a group (CRUD). But not all use cases of the CRUD 'manage group' can be fullfilled by every role. Therefore we decided to seperate the delete part and one update use case for which both require the 'admin' role at least. The update use case covers the possiblity to invite new members. Further changes in the entity are preserved to the 'owner' and 'admin' role.


# 2. Flow of Events
## 2.1 Create
* User clicks on "create group" button
* User fills the "create group" page - title, adding members (optional)
- User clicks on "create" button and will be forwarded to the group's hubpage
- User clicks on "cancel" button and will be sent back to the page he or she visited before
### 2.1.1 Activity Diagram
![](https://github.com/placetobeer/documentation/blob/master/manageGroupUML.png)
### 2.1.2 Mock-up
![Group navigation bar](https://github.com/placetobeer/documentation/blob/master/use_cases/ui-mockups/groupNavigationBar.png)
![Create group](https://github.com/placetobeer/documentation/blob/master/use_cases/ui-mockups/createGroup.png)
### 2.1.3 Narrative

## 2.2 Read
- User clicks on "group settings" button
- User can see the name of the group, the descripiton, the defined settings, and the list of group members
- User clicks on "cancel" button and will be sent back to the page he or she visited before
### 2.2.1 Activity Diagram
### 2.1.2 Mock-up
![Group settings - member view](https://github.com/placetobeer/documentation/blob/master/use_cases/ui-mockups/groupsettings.png)
![Group settings - admin view](https://github.com/placetobeer/documentation/blob/master/use_cases/ui-mockups/groupsettings-admin.png)
![Group settings - owner view](https://github.com/placetobeer/documentation/blob/master/use_cases/ui-mockups/groupsettings-owner.png)
### 2.1.3 Narrative

## 2.3 Update
- User clicks on "group settings" button
- User clicks on "Edit" button next to the group name to type in a new group name
- User clicks on "add member" button
- User fills the form with the person's email - the system checks if the email is already registered or the without an account
- User clicks on "invite" button and will be sent back to the "group settings" page - the system sends an invitation email
### 2.3.1 Activity Diagram
### 2.3.2 Mock-up
Mock-ups for group settings same as mock-ups for read view (compare 2.1.2).

![Add Member Pop-Up](https://github.com/placetobeer/documentation/blob/master/use_cases/ui-mockups/addMember.png)
### 2.3.3 Narrative

## 2.4 Alternative Flows
(n/a)

# 3. Special Requirements
(n/a)

# 4. Preconditions
tbd

# 5. Postconditions
(n/a)
 
# 6. Extension Points
(n/a)



