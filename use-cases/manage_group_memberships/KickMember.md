# 1. Kick member (Update group membership)

## 1.1 Brief Description
In the group settings popup an admin and the owner have the right to kick a member from the group. Then the membership will be deleted.

# 2. Flow of Events
## 2.1 Basic Flow
user must be of role "admin" or higher
- user clicks on button "group settings" -> opens group settings popup
- user sees the list of all group members with their assigned roles
- user clicks on member with a role lower than user's
- user clicks on "kick member" button -> selected member is removed from the group
### 2.1.1 Activity Diagram
![kickMember](https://raw.githubusercontent.com/placetobeer/ptb-documentation/master/use-cases/manage_group_memberships/activityDiagrams/kick_member.png)

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
