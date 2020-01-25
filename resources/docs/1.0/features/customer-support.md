# Customer Support

Customer support, chat support, live support, guest chatting, whatever you say it, will match-up with every situation. A user can also chat without even logging in into your website.

---

![Live Customer support, Helpdesk, live chat support](https://addchat-laravel-pro-docs.classiebit.com/images/customer-support.jpg "Live Customer support, Helpdesk, live chat support")

---

**Guest Mode** in which the user does not need to be logged in to chat, they only need to enter their `name` & `email` to continue chatting.


- [Setup Guest Mode](#Setup-Guest-Mode)
- [Guest Login](#Guest-Login)
- [Auto-conversion](#Auto-conversion)



<a name="Setup-Guest-Mode"></a>
## Setup Guest Mode

**Guest Mode** is `disabled` by default. You need to set it up first to `enable` it. But before that, it is required to set up and `enable` **User Groups**

---

![Setup customer support or guest mode](https://addchat-laravel-pro-docs.classiebit.com/images/setup-guest-mode.jpg "Setup customer support or guest mode")

---

>{info} Read the **[User Groups](/{{route}}/{{version}}/features/user-groups)** feature before continuing to below steps.

---

It's very simple to `enable` the **Guest Mode**, you only need to -

1. Go to `Admin Panel -> Settings`
2. Scroll down to **GUEST MODE** section
3. Click on the `Guest Mode` checkbox, to turn it `on/off`
4. Finally, enter the **Guest Group Id** (value), the User-group that can chat with Guests (users who are not logged in)


>{success} After the above step completes, `Admin` & `Guest-group` users can see a **Guest/Customer Support** tab on the chat widget.

---


<a name="Guest-Login"></a>
## Guest Login

Let's see how a Guest can start chatting without logging into the website.

---

![Guest login](https://addchat-laravel-pro-docs.classiebit.com/images/start-guest-chat.jpg "Guest login")

---

1. When a Guest visits your website and clicks on the AddChat widget.

2. A form window will open in the AddChat widget, asking about their `Name` & `Email`.

3. After submitting, the Guest can start chatting.


>{primary} When Guest sends a message, it gets forwarded to all the Guest-group users.

---


<a name="Auto-conversion"></a>
## Auto-conversion

AddChat auto-convert the Guest conversations to Registered user conversations, when the Guest **Register** on the website with the same `Email` that he/she used as a Guest. Let's see what it is-


- Suppose a Guest started chatting.

- And on next day, when the guest returns and opens the chat, then he/she can continue from the previous conversation.

- Now suppose the same guest **Signup** on the website with the same `email`

- And, when the guest **Login** into the website, and open the Chat widget, then he/she can see all the previous conversations that were sent as **Guest**.


>{primary} This is useful when your leads become your customers.
 