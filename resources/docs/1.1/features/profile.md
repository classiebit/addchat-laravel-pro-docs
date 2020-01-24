# Profile

---

![Addchat User Profile](https://addchat-pro-docs.classiebit.com/images/user-profile.jpg "Addchat User Profile")

---


AddChat does not modify any of your website's existing database tables or data. It only fetches `user-id` and `email` from `users` table **(read-only)**. AddChat manages every user info like name, profile picture, online status, etc, in a separate table called `ac_profiles`. In the profile, the user can update-

1. Name
2. Profile picture
3. Online status

---

>{info} As of now, the user `online status` is managed manually by the user. In the next version, we'll make it automatic, so that whenever a user comes online the status will be updated automatically.