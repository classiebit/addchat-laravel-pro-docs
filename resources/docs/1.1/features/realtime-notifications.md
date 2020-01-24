# Realtime Notifications

AddChat Laravel Pro comes with a custom **Internal** notification system & **Pusher** integration for chatting in realtime. 

---

![Realtime notifications](https://addchat-pro-docs.classiebit.com/images/realtime-notification.jpg "Realtime notifications")

---

**Internal** notification is a custom real-time notification system built using VueJs, which does not require any additional server setup. It works smoothly behind the scenes.

<br>

**Internal** notification system sends regular `Asynchronous HTTP/S Requests` to the server for getting the latest messages on the fly. For the geeks who wanna know more, it only runs a **single `SELECT`** database query in a **single `Table`** to fetch the latest messages.

>{info} The **total no. of `records`** fetched from **single `SELECT`** query are equal to the **total no. of users chatting simultaneously**.

---

>{primary} Admin can switch between **Pusher** & **Internal** notification system with just one click.


- [Internal Notifications](#Internal-Notifications)
- [Pusher Notifications](#Pusher-Notifications)
- [Pusher Setup](#Pusher-Setup)


<a name="Internal-Notifications"></a>
## Internal Notifications

Internal notification system fetches the following things in realtime (without page refresh)

1. Latest received messages from multiple users
2. Latest messages while user-to-user chatting
3. The message is seen or not

---

>{primary} **Internal** notification system saves **Pusher** monthly subscription fees.

---


<a name="Pusher-Notifications"></a>
## Pusher Notifications

Pusher notification system fetches the following things in realtime.

1. Latest received messages from multiple users
2. Latest messages while user-to-user chatting
3. The message is seen or not
4. The user is typing...


<a name="Pusher-Setup"></a>
## Pusher Setup

By default, the **Internal** notification system is `enabled`. To switch to `Pusher` notifications, firstly, you (as website Admin) need to [Signup on Pusher](https://pusher.com/signup) and `create an app` and get the Pusher API credentials.

---

![Pusher setup](https://addchat-pro-docs.classiebit.com/images/pusher-setup.jpg "Pusher setup")

---


Once you have the **Pusher** credentials, open AddChat widget and -

1. Go to `Admin Panel -> Settings` & scroll down to **Realtime Notifications** section.

2. Select `Notification Type` to `Pusher Notification`

3. Then enter the fields-
 - Pusher App Id
 - Pusher Key
 - Pusher Secret
 - Pusher Cluster

4. Click on save settings and you're done.

---

>{success} Now, the AddChat widget will fetch real-time notifications using **Pusher**

---