# External Send Message Button

Introducing a new feature in v1.1. You can send message to a user using an external button with JavaScript function.

---

![External send message button](https://addchat-laravel-pro-docs.classiebit.com/images/external-button.png "External send message button")

---

To use this feature, follow the below steps-

1. Add a button anywhere on your website where AddChat widget is active (showing).
2. Add a JavaScript onclick event on the button and call the AddChat function and pass the user-id to whom, to send the message.

```html
<button type="button" onclick="openAddChatBuddy(<user_id>)">
```