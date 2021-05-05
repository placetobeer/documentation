# 1. CR(U)D Manage Group memberships

## 1.1 Brief Description
This CR(U)D is all about managing users related to a certain group. Each membership defines the user and the group in question and additionally describes the role the user plays in the group. As the update use case can only be performed by group members with role "admin" or higher this is not a complete CRUD. The update use case and the possibility to kick members, are outsourced in the following files:
- [manage admin roles](https://github.com/placetobeer/ptb-documentation/blob/master/use-cases/manage_group_memberships/manageAdminRole.md)
- [kick member](https://github.com/placetobeer/ptb-documentation/blob/master/use-cases/manage_group_memberships/KickMember.md)

# 2. Flow of Events

## 2.1 Create
A user can invite new members to a group. 
- user_1 clicks on button "group settings" -> opens group settings popup 
- user_1 clicks on button "add member to group"
- user_1 enters the to be invited user's email and role
- user_1 clicks on button "send invitation" and creates an invitation for user_2
- two possibilites:
	- user_2 *registered*: in the group navigation bar in the remaining invitation section the new invitation will be added and user_2 has the possiblity to accept or decline the invitation
	- user_2 *not registered* yet: receives an invitation via Email to register and join the group

- if user_2 accepts the initation he or she becomes a member of the created group

### 2.1.1 Activity Diagram
![addMember](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/manage_group_memberships/activityDiagrams/add_member.png)
### 2.1.2 Mock-up
![group settings](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/ui-mockups/groupSettings_complete.png)

![addMember](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/ui-mockups/addMember.png)

![remaining invitations](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/ui-mockups/remainingInvitations.png)

### 2.1.3 Narrative

## 2.2 Read
A user can see the group members.
- user clicks on button "group settings" -> opens group settings popup 
- user sees the list of all group members with their assigned roles and a list with the pending invitations
### 2.2.1 Activity Diagram
![readMember](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/manage_group_memberships/activityDiagrams/read_member.png)

### 2.2.2 Mock-up

![group settings](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/ui-mockups/groupSettings_complete.png)

### 2.2.3 Narrative

## 2.3 Delete
A user can leave a group.
-   user clicks on button "group settings"  -> opens group settings popup 
- user clicks on button "leave group" -> confirmation popup 

### 2.3.1 Activity Diagram
![leave_group](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/manage_group_memberships/activityDiagrams/leave_group.png)

### 2.3.2 Mock-up
![group settings](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/ui-mockups/groupSettings_complete.png)

### 2.3.3 Narrative

## 2.4 Alternative Flows
(n/a)

# 3. Special Requirements
(n/a)

# 4. Preconditions
tbd

# 5. Postconditions
(n/a)
 
# 6. Function Points
FP = 111,6

![enter image description here](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/function-points/manage-group-memberships-fp.png)
![enter image description here](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/function-points/fp-table2.png)




