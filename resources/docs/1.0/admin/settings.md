# Settings

Manage AddChat global settings here.

---

![Addchat Settings](https://addchat-laravel-pro-docs.classiebit.com/images/addchat-pro-settings.jpg "Addchat Settings")

---

>{primary} To visit `Admin Panel` click on profile icon and then click <larecipe-button type="white">Admin Panel</larecipe-button>


- [General](#General)
- [Widget Config](#Widget-Config)
- [Users Table](#Users-Table)
- [User Groups Table](#User-Groups-Table)
- [Guest Mode](#Guest-Mode)
- [Show/Hide User Email](#Show-Hide-User-Email)

--- 

<a name="General"></a>
## General Settings

Setup brand identity.


|Setting Name|Type|Description|
|:-|:-|
|Site Name|`alpha-numeric`|Brand/Website name|
|Site Logo|`image:jpg|jpeg|png`|Logo for AddChat widget and admin panel|
|Chat Icon|`image:jpg|jpeg|png`|Logo for the widget icon|
|Footer Text|`alpha-numeric`|Give chat widget your own brand name|
|Footer URL|`alpha-numeric`|Brand website URL|



<a name="Widget-Config"></a>
## Widget Config

These are the AddChat widget main configurations


|Setting Name|Type|Description|
|:-|:-|
|Admin User Id|`integer`|Admin-User-Id **VALUE** from the users table (by default **Admin-User-id** is **1**)|
|Pagination Limit|`integer`|The total number of records to be fetched at a single time (greater the value, greater load)|
|Upload Path|`integer`|The profile pics will be uploaded to this path|
|Assets Path|`integer`|AddChat assets path, AddChat will pick up the fonts, placeholder image and notification sound from this path|

---

>{danger} Please be sure to keep the `Upload Path` writable, or else it'll through an error while uploading images



<a name="Users-Table"></a>
## Users Table

Enter your website `users` table name and it's `user-id` & `email` column names.

|Setting Name|Type|Description|
|:-|:-|
|Users table name|`string`|`users` table name|
|User Id|`string`|`user-id` column name in the users table|
|User Email|`string`|`email` column name in the users table|


>{success} AddChat never modify any data the `users` table and never read the `password` or any other sensitive column except `user id` and `email`

---



<a name="User-Groups-Table"></a>
## User Groups Table

---

>{warning} Please read **[User Groups](/{{route}}/{{version}}/features/user-groups)** for more info about `Groups` Function

---

Enter `groups` table name and columns name, so that AddChat can fetch & use your existing user groups.

>{success} AddChat never modify any data in the `groups` table and never assign any `group` to any `user`


|Setting Name|Type|Description|
|:-|:-|
|Groups|`bool`|Check/Uncheck the checkbox to enable/disable groups function|
|Groups Table Name|`string`|Enter the groups table name|
|Group Id|`string`|Enter the groups table's Group Id column name|
|Group Name|`string`|Enter the groups table's Group Name column name|
|Users & Groups Pivot Table Name|`string`|enter name of your users & groups pivot table e.g users_groups|
|Pivot table User Id|`string`|enter Pivot table User Id column name e.g user_id|
|Pivot table Group Id|`string`|enter Pivot table Group Id column name e.g group_id|

---



<a name="Guest-Mode"></a>
## Guest Mode

>{warning} Please read **[Customer Support](/{{route}}/{{version}}/features/customer-support)** section for more info about `Guest Mode` Function

Enter `Guest/Support Group` id (value), the group who chats with the `Guests` (the users who are not registered or logged in into the your website)


|Setting Name|Type|Description|
|:-|:-|
|Guest Mode|`bool`|Check/Uncheck the checkbox to enable/disable Guest Mode function|
|Guest Group Id|`integer`|Enter the Guest/Support Group id (value)|



<a name="Show-Hide-User-Email"></a>
## Show/Hide User Email

If you want to show or hide the email under the user names in contact list.


---

> {warning} Please read the guidelines provided below each setting, and follow exactly mentioned, or else it may break down your site.

---

> {primary} After updating settings, please log out and log in again to see the effects.