# 1. Manage admin role

## 1.1 Brief Description
In the group settings popup an admin and the owner have the right to grant the admin role to a group member. The owner has as well the possibility to revoke the admin role from an admin of the group. 

# 2. Flow of Events
## 2.1 Basic Flow
user must be owner of target group
- user clicks on button "group settings" -> opens group settings popup
- user sees the list of all group members with their assigned roles
- user clicks on member
- two possibilites:
    - selected member of role *"member"*: user clicks on "grant admin role" button -> selected member becomes "admin" of group
    - selected member of role *"admin"*: user clicks on "revoke admin role" button -> selected member becomes "member" of group
### 2.1.1 Activity Diagram
![manageAdmin](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/manage_group_memberships/activityDiagrams/grant_admin.png)

### 2.1.2 Mock-up
**Group settings popup - admin view**

![groupsettings-admin.png](https://github.com/placetobeer/ptb-documentation/blob/master/use-cases/ui-mockups/groupsettings-admin.png?raw=true)

**Group settings popup - owner view**

![groupsettings-owner.png](https://github.com/placetobeer/ptb-documentation/blob/master/use-cases/ui-mockups/groupsettings-owner.png?raw=true)
### 2.1.3 Narrative

## 2.2 Alternative Flows
(n/a)

# 3. Special Requirements
(n/a)

# 4. Preconditions
tbd

# 5. Postconditions
(n/a)
 
# 6. Functional Points
