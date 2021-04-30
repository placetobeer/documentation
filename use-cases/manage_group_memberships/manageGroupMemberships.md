# 1. Manage Group memberships

## 1.1 Brief Description
This use case is all about managing users related to a certain group. Each membership defines the user and the group in question and additionally describes the role the user plays in the group. As the update and delete use cases can only be performed by group members with role "admin" or higher, we decided to cover them in extra use cases 
TODO: put in links for use cases "grant/ revoke admin role" and "kick member"here

# 2. Flow of Events

## 2.1 Create
- User_1 clicks on "group settings" button
- User_1 clicks on "add member to group" button
- User_1 enters the to be invited user's email and role
- User_1 clicks on "invite" button and creates an invitation for User_2
- User_2 receives an invitation
- User_2 clicks on "accept" button and becomes a member of the inviting group

### 2.1.1 Activity Diagram

### 2.1.2 Mock-up

### 2.1.3 Narrative

## 2.2 Read
- User clicks on "group settings" button
- User sees the list of all group members with their assigned roles
### 2.2.1 Activity Diagram

### 2.1.2 Mock-up

### 2.1.3 Narrative

![addMember](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use_cases/ui-mockups/addMember.png)


![remaining invitations](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use_cases/ui-mockups/remainingInvitations.png)

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




