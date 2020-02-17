# Upgrade to v1.1.x

Updating AddChat Laravel Pro is simple. Just download the latest version of AddChat Laravel Pro from [Classiebit.com - Downloads page](https://classiebit.com/downloads) after login into your account.

- [Steps to upgrade](#Steps-to-upgrade)
- [Developer upgrade](#Developer-upgrade)

<a name="Steps-to-upgrade"></a> 
## Steps to upgrade

* Extract the **addchat-laravel-pro-1.1.x.zip** file. 
* Copy the **addchat-laravel-pro** folder and go to your website directory.
* Delete the current **addchat-laravel-pro** folder & replace it by the new one.
* Then run the composer update command

    ```php
    composer update
    ```

* On production (live) server, run this command as well

    ```php
    composer install --optimize-autoloader --no-dev
    ```

* Run this command to publish updated AddChat assets to your project. This will only update the files in `public/addchat` folder.

    ```php
    php artisan vendor:publish --tag=addchat_public --force
    ```

* At last, run these cache clear commands

    ```php
    php artisan config:clear
    php artisan cache:clear
    php artisan view:clear
    php artisan route:clear
    ```

<a name="Developer-upgrade"></a> 
## Developer upgrade

If you've used **Developer Installation**, then also follow these steps.

* Copy the **addchat-vuejs-pro** folder and go to your website directory.

* Delete the current **addchat-vuejs-pro** folder & replace it by the new one.

* Run the below command to update AddChat vuejs plugin

    ```php
    npm update
    ```

* Run this command to publish updated AddChat assets to your project. This will only update the files in `public/addchat` folder.

    ```php
    php artisan vendor:publish --tag=addchat_public --force
    ```

* At last, run these cache clear commands

    ```php
    php artisan config:clear
    php artisan cache:clear
    php artisan view:clear
    php artisan route:clear
    ```