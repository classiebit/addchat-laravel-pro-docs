# Include/Exclude URLs

Include/Exclude URLs feature is useful in cases, where to show AddChat widget on some URLs and where not to.

---

For Example

1. There are some pages, where AddChat widget needs not to be shown. Like on about us, terms, privacy policy, etc pages. 

2. And in some cases, when the website has a lot of pages, and AddChat widget needs to be shown on some specific pages only. Like profile page, product page, etc. 

---

>{danger} Either Exclude URL or Include URL can be used at a time.

---

>{primary} By default the **Include/Exclude URLs** feature is `Off`, it needs to be turned `On` from the `Admin Panel`


- [Setup Include URLs](#Setup-Include-URLs)
- [Setup Exclude URLs](#Setup-Exclude-URLs)



<a name="Setup-Include-URLs"></a>
## Setup Include URLs

To `Show` AddChat widget only on some specific URLs.

1. Go to `config/addchat.php` and scroll to **Include/Exclude URLs** section.
2. Add multiple paths (URL segments only) in array format and save the file.
3. Now, AddChat widget will show only on those paths of your website.


<a name="Setup-Exclude-URLs"></a>
## Setup Exclude URLs

To `Hide` AddChat widget only on specific URLs.

1. Go to `config/addchat.php` and scroll to **Include/Exclude URLs** section.
2. Add multiple paths (URL segments only) in array format and save the file.
3. Now, AddChat widget will be shown except those paths of your website.

---

>{warning} Enter the `Path` only and not the full website `URL`

---

>{primary} This gives more control over the AddChat widget functioning over your website.