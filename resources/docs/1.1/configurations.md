# Configurations

In v1.1. The AddChat database settings are moved to the `addchat` config file. You can find in your application `config/addchat.php`.


- [Brand Identity](#Brand-Identity)
- [Upload Path](#Upload-Path)
- [Users Table](#Users-Table)
- [Super Admin](#Super-Admin)
- [User Groups Table](#User-Groups-Table)
- [Guest Mode](#Guest-Mode)
- [Customize Default Behaviour](#Customize-Default-Behaviour)
- [Pagination](#Pagination)
- [Include/Exclude URLs](#Include-Exclude-URLs)
- [Notification Type](#Notification-Type)
- [AddChat Migrations](#AddChat-Migrations)

--- 

<a name="Brand-Identity"></a>
## Brand Identity

Add your website identity & branding to the AddChat widget. These changes are for the AddChat widget only and have nothing to do with the main website.


|Setting Name|Type|Default|Description|
|:-|:-|
|widget_name|`required`|`AddChat Laravel Pro`|Brand/Website name|
|widget_logo|`required`|`addchat/img/addchat-logo-white.png`|Logo for AddChat widget and admin panel|
|widget_icon|`required`|`addchat/img/addchat-shadow.png`|Logo for the widget icon|
|widget_user_avatar|`required`|`addchat/img/avatar.png`|Images placeholder|
|widget_notify_sound|`required`|`addchat/sound/notification.mp3`|Notification sound|
|widget_footer_text|`optional`|`AddChat | by Classiebit`|Give chat widget your own brand name|
|widget_footer_url|`optional`|`https://classiebit.com/addchat-laravel-pro`|Brand website URL|


<a name="Upload-Path"></a>
## Upload Path

AddChat uploads User profile pics & Messages attachments in `storage/public` folder.


|Setting Name|Type|Default|Description|
|:-|:-|
|upload_path|`required`|`storage/addchat`|Profile pics & message attachments uploading path|


<a name="Users-Table"></a>
## Users Table

AddChat fetches your website's existing users from the **users** table. If your **users** table and it's **user-id** & **email** column names are different, then you can add them below.

|Setting Name|Type|Default|Description|
|:-|:-|
|users_table|`required`|`users`|Users table name|
|users_col_id|`required`|`id`|Users table column name of id|
|users_col_email|`required`|`email`|Users table column name of email|


>{success} AddChat never modify any data the `users` table and never read the `password` or any other sensitive column except `user id` and `email`

---


<a name="Super-Admin"></a>
## Super Admin

As of now, AddChat can have only one **Super Admin** (will make it to multiple Admins in upcoming versions).

|Setting Name|Type|Default|Description|
|:-|:-|
|admin_user_id|`required`|`1`|Default Super Admin is the User with User-id = 1|



<a name="User-Groups-Table"></a>
## User Groups/Roles Table

To enable the AddChat multi-user groups feature. Your website database must have a User-Groups table and a pivot table that connects Users to a group. AddChat also supports a user belongs to multiple groups. Just mention those tables' names below.

---

>{primary} Please read **[User Groups](/{{route}}/{{version}}/features/user-groups)** for more info about `Groups` Function

---

Enter `groups` table name and columns name, so that AddChat can fetch & use your existing user groups.

---

>{success} AddChat never modify any data in the `groups` table and never assign any `group` to any `user`

---

>{info} This feature is optional if you don't wanna enable User groups feature, keep the below configurations `NULL

---

|Setting Name|Type|Default|Description|
|:-|:-|
|groups_table|`optional`|`NULL`|User-groups table name e.g `groups` or `roles`|
|groups_col_id|`string`|`NULL`|User-groups table column name of id|
|groups_col_name|`string`|`NULL`|User-groups table column name of group name/title|
|ug_table|`string`|`NULL`|User-groups pivot table name e. `users_groups` or `users_roles`|
|ug_col_user_id|`string`|`NULL`|User-groups pivot table column name of user-id|
|ug_col_group_id|`string`|`NULL`|User-groups pivot table column name of group-id e.g `group_id` or `role_id` |

---


<a name="Guest-Mode"></a>
## Guest Mode

Guest mode allows your website visitors to use the AddChat widget to send messages without signup or login. As like Chat support.

---

>{primary} Please read **[Customer Support](/{{route}}/{{version}}/features/customer-support)** section for more info about `Guest Mode`.

---

>{info} This feature is optional if you don't wanna enable Guest mode feature, keep the below configuration `NULL

---

Enter `Guest/Support Group` id (value), the group who chats with the `Guests` (the users who are not registered or logged in into your website).
To enable guest mode, AddChat only requires a User Group which will chat with the guests. You can create a separate User Group and add that group's id.


|Setting Name|Type|Default|Description|
|:-|:-|
|guest_group_id|`optional`|`NULL`|Guest/Support Group id e.g `8`|



<a name="Customize-Default-Behaviour"></a>
## Customize Default Behaviour

|Setting Name|Type|Default|Description|
|:-|:-|
|hide_email|`TRUE/FALSE`|`FALSE`|Whether to show users email in throughout the widget|
|enter_send|`TRUE/FALSE`|`TRUE`|Whether to send a message on pressing Enter|
|open_chat_on_notification|`TRUE/FALSE`|`FALSE`|Whether to automatically open user chat window when a new message arrives.|



<a name="Pagination"></a>
## Pagination

Set AddChat widget global pagination limit.

---

>{warning} Greater value = More loading time

---

|Setting Name|Type|Default|Description|
|:-|:-|
|pagination_limit|`required|Greater than 0`|`5`|The total number of records to be fetched from the database at a single time|



<a name="Include-Exclude-URLs"></a>
## Include/Exclude URLs

Control whether to show or not to show AddChat widget on specific URLs

---

>{primary} Please read **[User Groups](/{{route}}/{{version}}/features/include-exclude-urls)** for more info.

---


|Setting Name|Type|Default|Description|
|:-|:-|
|include_url|`optional`|`array()`|Show AddChat widget only on these URLs.|
|exclude_url|`optional`|`array()`|Hide AddChat widget only on these URLs.|


<a name="Notification-Type"></a>
## Notification Type

By default, AddChat works on a custom internal real-time notification system build with VueJs.

---

>{primary} Please read **[Realtime Notifications](/{{route}}/{{version}}/features/realtime-notifications)** for more info.

---

AddChat comes with integrated Pusher service. To switch to Pusher real-time notifications, add the Pusher API credentials and change notification_type to `pusher`


|Setting Name|Type|Default|Description|
|:-|:-|
|notification_type|`internal/pusher`|`internal`|switch between notification systems|
|pusher_app_id|`optional`|`NULL`|Pusher App id|
|pusher_key|`optional`|`NULL`|Pusher key|
|pusher_secret|`optional`|`NULL`|Pusher secret|
|pusher_cluster|`optional`|`NULL`|Pusher cluster|


<a name="AddChat-Migrations"></a>
## AddChat Migrations

Whether to autoload AddChat migrations. 

- **Default is TRUE (enabled) RECOMMENDED**

    When enabled, AddChat migrations managed automatically on running migration command. AddChat migrations will autorun even when updating to a new AddChat version. When updating AddChat, AddChat migrations will auto-run on running migration command and it'll update it's database tables without losing or modifying existing data in DB.


- **If it's FALSE (disabled)**

    You'll need to copy AddChat migrations files to your app migrations folder. Then, you can manage the migration files yourself. This will be the case when you're customizing the AddChat on your own.

