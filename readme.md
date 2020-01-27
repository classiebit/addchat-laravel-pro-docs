# Addchat Laravel Pro Docs

Welcome to AddChat Laravel Pro documentation.

- Read the docs live **[AddChat Laravel Pro Docs](https://addchat-laravel-pro-docs.classiebit.com)**

---

### All-in-one multi-purpose Chat Widget For Laravel website

AddChat is a new chatting friend of Laravel. It's a standalone Chat widget that uses the website's existing `users` base, and let website users chat with each other. 

<br>

You get full source-code, hence AddChat lives and runs on your server/hosting including database. And therefore, you get complete privacy over your data. Either you're a big corporate sector or a small business. AddChat is for everyone.


## Pro Version

**AddChat Laravel Pro Version** comes with **Commercial** license. Pro version is fully loaded with a lot of useful and exciting features.

+ [Live (addchat-laravel-pro.classiebit.com)](https://addchat-laravel-pro.classiebit.com) - Visit pro version live.
+ [Purchase (classiebit.com/addchat-laravel-pro)](https://classiebit.com/addchat-laravel-pro) - Purchase pro version here.


# Installation

AddChat can be installed via composer. Awesome... ✌️. Now, as of v1.1.0 release. You as a developer can customize the AddChat VueJS code as well.


- [Prerequisites](#Prerequisites)
- [Non-developer Installation](#Non-developer-Installation)
- [Developer Installation](#Developer-Installation)


## Prerequisites

* Laravel version 5.5 / 5.6 / 5.7 / 5.8 / 6.x
* Make sure to install the AddChat package on a **Fresh** or **Existing** Laravel application. 
* We also assume that you've set up the database.
* If you're running MySql version older than < 5.7 then disable strict mode in your Laravel app.
 - Go to `config/database.php` and update `'strict' => false` in `mysql` section.


## Non-developer Installation

1. If installing AddChat on an existing Laravel application and you already have **Auth** system then **skip this step**

 If installing on a **Fresh Laravel application** then run 

 **For Laravel 5.5 to 5.8**

 ```php
 php artisan make:auth

 php artisan migrate
 ```

 **For Laravel 6.x**

 ```php
 composer require laravel/ui --dev

 php artisan ui vue --auth

 npm install && npm run dev

 php artisan migrate
 ```


2. Unzip the `addchat-laravel-pro.zip` file, copy the `addchat-laravel-pro` folder and place it in your Laravel application root directory.

---

The folder name must be `addchat-laravel-pro` in your Laravel website directory.

---


3. Open your Laravel application `composer.json` file and paste the below code in the end (right before last curly `}` bracket)

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



4. Install AddChat Laravel Pro via Composer

 ```php
 composer require classiebit/addchat-laravel-pro
 ```

5. Run AddChat install command

 ```php
 php artisan addchat:install
 ```

6. While installation, it will ask you for the license code. Enter the license code to complete the installation process.

---

Remember, one license code is valid for one domain only. Contact support for more details.

---


7. Open the common layout file, mostly the common layout file is the file that contains the HTML & BODY tags.

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

For Info, the `php artisan addchat:install` publishes AddChat assets to your application `public` directory

---


## Developer Installation

This is an advanced installation method. This method will help you customizing the AddChat VueJS code. We recommend this method only if-

* You're a developer.
* If you're already using VueJS into your website.

<br>

1. If installing AddChat on an existing Laravel application and you already have **Auth** system then **skip this step**.

 If installing on a **Fresh Laravel application** then run 

 **For Laravel 5.5 to 5.8**

 ```php
 php artisan make:auth

 php artisan migrate
 ```

 **For Laravel 6.x**

 ```php
 composer require laravel/ui --dev

 php artisan ui vue --auth

 npm install && npm run dev

 php artisan migrate
 ```


2. Unzip the `addchat-laravel-pro.zip` file. Copy `addchat-laravel-pro` & `addchat-vuejs-pro` and paste them into Laravel website root directory.

---

The folder name must be same as `addchat-laravel-pro` and `addchat-vuejs-pro`.

---
 

3. Open your Laravel application `composer.json` file and paste the below code in the end (right before last curly `}` bracket)

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

4. Install AddChat Laravel Pro via Composer

 ```php
 composer require classiebit/addchat-laravel-pro
 ```

5. **(NEW STEP)** Install AddChat VueJS Pro via NPM

 ```php
 npm install addchat-vuejs-pro
 ```

6. Run AddChat install command

 ```php
 php artisan addchat:install
 ```


7. While installation, it will ask you for the license code. Enter the license code to complete the installation process.

---

Remember, one license code is valid for one domain only. Contact support for more details.

---


8. Now, you need to import the AddChat VueJS plugin into your VueJS app. 

 - Go to your website `resources/js/app.js` and import the AddChat VueJS plugin.

 ```js
 import AddchatVuejsPro from 'addchat-vuejs-pro';
 Vue.use(AddchatVuejsPro);
 ```

 - Then run 

 ```js
 npm run dev
 ```


9. In the last step, you only need to include `addchat.min.css` and VueJS widget code.

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

Please replace PHP tag by curly brackets.

---

Setup finishes here, now heads-up straight to **[Configurations](https://addchat-laravel-pro-docs.classiebit.com/docs/1.1/configurations)** docs

---

