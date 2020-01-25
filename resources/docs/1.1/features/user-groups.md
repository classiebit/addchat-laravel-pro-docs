# User Groups

AddChat's one of the most awaited features. AddChat automatically detects the website's **User-Groups**. Admin can set permissions for the groups from AddChat Admin-panel. Like, which group can chat with which.

---

![Multiple User Groups](https://addchat-pro-docs.classiebit.com/images/user-groups.jpg "Multiple User Groups")

---

>{success} AddChat supports multiple user groups e.g a user can belong to multiple groups.


- [Setup User Groups](#Setup-User-Groups)
- [Set Groups Permissions](#Set-Groups-Permissions)
- [Groups List](#Groups-List)


<a name="Setup-User-Groups"></a>
## Setup User Groups

**User-groups** option is by default `disabled`. You can `enable` it from AddChat config `config/addchat.php`. And to enable **User-groups** option, the website must meet the following **requirements**.

1. `Groups` or `Roles` table.

2. **Pivot** table for `Users` & `Groups` or `Roles` table, which contains sets of `User Id` and `Group Id` or `Role Id`.

---

>{primary} We've developed the Group system according to most common & standard User Groups/Roles functionality.

---

After completing the above requirements, the **Groups** can be `enabled` by following steps-

1. Go to `config/addchat.php` and scroll to `User Groups Table` section.
2. Enter the `groups/roles` and `user_groups/user_roles` pivot table & their column names.
3. Save the file, and you're good to go.

---

>{primary} Read the configurations for more info - **[User Groups Configurations](/{{route}}/{{version}}/configurations#User-Groups-Table)**

---

> {danger} All the above form fields are required to `enable` Group functionality.

---

> {success} After completing all the above steps, click on &nbsp;<larecipe-button type="white" size="sm" radius="full">Save Settings</larecipe-button> and logout & login again.

---



<a name="Set-Groups-Permissions"></a>
## Set Groups Permissions

Once after setting up Groups configuration successfully, you'll see all your website `Groups` in the `Admin Panel -> Chat Groups` and there you can set the **permissions** that which groups can chat with which group. 

---

![Set User Groups Permissions](https://addchat-pro-docs.classiebit.com/images/user-groups-permissions.jpg "Set User Groups Permissions")

---

Follow these baby steps to set group **permissions**

1. On the `Admin Panel`, go to `Chat Groups`

2. Click on &nbsp;<larecipe-button type="primary" size="sm" rounded>Permissions</larecipe-button> on any Group, e.g Members

3. A Popup will open, simply check the checkbox with which groups, the e.g Members group can chat.

4. Click on &nbsp;<larecipe-button type="primary" size="sm" radius="full">Save Permissions</larecipe-button>


---

>{primary} Admin Group users can chat with everyone (zero restrictions).

---


<a name="Groups-List"></a>
## Groups List

Once everything is done, when the users click on the AddChat widget `User Groups` tab, they'll see all the `Groups` according to the `Groups Permissions`. 

---

![Chat within User groups](https://addchat-pro-docs.classiebit.com/images/user-groups-show.jpg "Chat within User groups")

---

And also when the user clicks on each `Group`, they'll see all the `Users` in the `Group` and can chat with them.


>{success} This is also useful when a new user joins your website and wants to chat with any other user.