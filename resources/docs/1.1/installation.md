# Installation

AddChat can be installed via composer. Awesome... ✌️. Now, as of v1.1.0 release. You as a developer can customize the AddChat VueJS code as well.

---

> {info.fa-youtube} A complete video tutorial guide for getting started quickly is **Coming Soon**

---

- [Prerequisites](#Prerequisites)
- [Non-developer Installation](#Non-developer-Installation)
- [Developer Installation](#Developer-Installation)
- [Purchased From Codecanyon](#Purchased-From-Codecanyon)


<a name="Prerequisites"></a>
## Prerequisites

* Laravel version 5.5 / 5.6 / 5.7 / 5.8 / 6.x / 7.x / 8.x
* Laravel Authentication must be installed.
* Make sure to install the AddChat package on a **Fresh** or **Existing** Laravel application. 
* We also assume that you've set up the database.
* If you're running MySql version older than < 5.7 then disable strict mode in your Laravel app.
 - Go to `config/database.php` and update `'strict' => false` in `mysql` section.

---

> {primary} Laravel installation guide **[Laravel Installation](https://laravel.com/docs/)** 👈

---


<a name="Non-developer-Installation"></a>
## Non-developer Installation

1. Unzip the `addchat-laravel-pro-1.1.0.zip` file you downloaded. Then unzip the `addchat-laravel-pro.zip` file and copy the `addchat-laravel-pro` folder and place it in your Laravel application root directory.

2. Open your Laravel application `composer.json` file and paste the below code in the end (right before last curly `}` bracket)

 ```json
 "repositories": [{
  "type": "path",
  "url": "addchat-laravel-pro/"
 }]
 ```

 (once you complete, the `composer.json` file will look something like this) 

 ```json
 {
  .
  .
  .
  .
  .
  
  
  "repositories": [{
  "type": "path",
  "url": "addchat-laravel-pro/"
  }]

 }

 ```



3. Install AddChat Laravel Pro via Composer

 ```php
 composer require classiebit/addchat-laravel-pro
 ```

4. Run AddChat install command

 ```php
 php artisan addchat:install
 ```

5. While installation, it will ask you for the license code. Enter the license code to complete the installation process.

 >{info} Remember, one license code is valid for one domain only. Contact support for more details.


6. Open the common layout file, mostly the common layout file is the file that contains the HTML & BODY tags.

 - Copy AddChat CSS code and paste it right before closing **&lt;/head&gt;** tag

 ```php
 <!-- 1. Addchat css -->
 <link href="<?= asset('addchat/css/addchat.min.css') ?>" rel="stylesheet">
 ```
 
 - Copy AddChat Widget code and paste it right after opening **&lt;body&gt;** tag

 ```php
 <!-- 2. AddChat widget -->
 <div id="addchat_app" 
  data-baseurl="<?= url('') ?>"
  data-csrfname="<?= 'X-CSRF-Token' ?>"
  data-csrftoken="<?= csrf_token() ?>"
 ></div>
 ```

 - Copy AddChat JS code and paste it right before closing **&lt;/body&gt;** tag

 ```php
 <!-- 3. AddChat JS -->
 <script src="<?= asset('addchat/js/addchat.min.js') ?>"></script>
 ```

 <br>

 #### The final layout will look something like this

 ```php
 <head>

  <!-- **** your site other content **** -->

  <!-- 1. Addchat css -->
  <link href="<?= asset('assets/addchat/css/addchat.min.css') ?>" rel="stylesheet">

 </head>
 <body>

  <!-- 2. AddChat widget -->
  <div id="addchat_app" 
  data-baseurl="<?= url('') ?>"
  data-csrfname="<?= 'X-CSRF-Token' ?>"
  data-csrftoken="<?= csrf_token() ?>"
  ></div>

  <!-- **** your site other content **** -->

  <!-- 3. AddChat JS -->
  <script src="<?= asset('addchat/js/addchat.min.js') ?>"></script>
  
 </body>
 ```

---

>{info} For Info, the `php artisan addchat:install` publishes AddChat assets to your application `public` directory




<a name="Developer-Installation"></a>
## Developer Installation

This is an advanced installation method. This method will help you customizing the AddChat VueJS code. We recommend this method only if-

* You're a developer.
* If you're already using VueJS into your website.

<br>

1. Unzip the `addchat-laravel-pro-1.1.0.zip` file you downloaded. Then unzip the `addchat-laravel-pro.zip` & `addchat-vuejs-pro.zip` files and copy the `addchat-laravel-pro` & `addchat-vuejs-pro` folder and place it in your Laravel application root directory (near **vendor** folder).

2. Open your Laravel application `composer.json` file and paste the below code in the end (right before last curly `}` bracket)

 ```json
 "repositories": [{
  "type": "path",
  "url": "addchat-laravel-pro/"
 }]
 ```

 (once you complete, the `composer.json` file will look something like this) 

 ```json
 {
  .
  .
  .
  .
  .
  
  "repositories": [{
  "type": "path",
  "url": "addchat-laravel-pro/"
  }]

 }

 ```

3. Install AddChat Laravel Pro via Composer

 ```php
 composer require classiebit/addchat-laravel-pro
 ```

4. **(NEW STEP)** Install AddChat VueJS Pro via NPM

 ```php
 npm install addchat-vuejs-pro
 ```

5. Run AddChat install command

 ```php
 php artisan addchat:install
 ```


6. While installation, it will ask you for the license code. Enter the license code to complete the installation process.

 >{info} Remember, one license code is valid for one domain only. Contact support for more details.

7. Now, you need to import the AddChat VueJS plugin into your VueJS app. 

 - Go to your website `resources/js/app.js` and import the AddChat VueJS plugin.

 ```js
 import AddchatVuejsPro from 'addchat-vuejs-pro';
 Vue.use(AddchatVuejsPro);
 ```

 - Then run 

 ```js
 npm run dev
 ```


8. In the last step, you only need to include `addchat.min.css` and VueJS widget code.

 - Copy AddChat CSS code and paste it right before closing **&lt;/head&gt;** tag

 ```php
 <!-- 1. Addchat css -->
 <link href="<?= asset('addchat/css/addchat.min.css') ?>" rel="stylesheet">
 ```
 
 - Copy AddChat Widget code and paste it right after opening **&lt;body&gt;** tag

 ```php
 <!-- 2. AddChat widget -->
 <div id="addchat_app" 
  data-baseurl="<?= url('') ?>"
  data-csrfname="'X-CSRF-Token'"
  data-csrftoken="<?= csrf_token() ?>"
 ></div>
 ```

 - At this point, we assume that you've already included `app.js`.

 ```php
 <script src="<?= asset('js/app.js') ?>"></script>
 ```

---

>{warning} Please replace PHP tag by curly brackets.

---

>{success} Setup finishes here, now heads-up straight to **[Configurations](/{{route}}/{{version}}/configurations)** docs

---

<a name="Purchased-From-Codecanyon"></a>
## Purchased From Codecanyon

If you've purchased AddChat Laravel Pro from Codecanyon `codecanyon.net` then follow these simple steps-

1. Enter `Purchase-code` as a License key in the AddChat Laravel Pro installer.
2. Visit [classiebit.com](https://classiebit.com), signup as new user and go to [Downloads](https://classiebit.com/downloads)
3. Click on <larecipe-button radius="half" type="black">Purchased from Codecanyon?</larecipe-button>
4. In the popup, enter the Purchase-code and submit. You'll see the product on the download list.
5. At last, add the authorized domain. And you're good to go. 👍