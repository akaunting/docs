Modules
=======

Akaunting ships with core accounting tools needed to manage money. It also has a module structure so that you could extend it. We use our own [akaunting/module](https://github.com/akaunting/module) package as builder.

A module is like a Laravel package, it has some routes, views, controllers, and models. While technically we call it `Module`, we name it `App` in the UI for the end-user as that's what they are familiar with.

### Folder Structure

As you can see from the example below, the structure of a module is very similar to a basic Laravel app.

```
app/
bootstrap/
config/
database/
modules/
  ├── MyBlog/
      ├── Console/
      ├── Database/
          ├── Migrations/
          ├── Seeds/
      ├── Http/
          ├── Controllers/
          ├── Requests/
      ├── Jobs/
      ├── Listeners/
      ├── Models/
      ├── Providers/
          ├── Main.php
      ├── Resources/
          ├── assets/
          ├── lang/
          ├── views/
      ├── Routes/
          ├── admin.php
          ├── portal.php
      ├── composer.json
      ├── module.json
      ├── package.json
      ├── webpack.mix.js
public/
...
vendor/
.env
```

### Creating a module

There are loads of Artisan commands built-in the module package. For example, let's see how to create a new module:

```bash
php artisan module:make my-blog
```

This will create all files and folders shown in the above example. Now let's install the module using the following command:

```bash
php artisan module:install my-blog 1
```

`my-blog` is the **alias** of the module and `1` is the **company id** that you want to install the module. [Here](https://akaunting.com/docs/user-manual/companies) you can find more about companies in Akaunting.

Alias is the unique name of the module as is used everywhere in Akaunting.

### module.json file

The `module.json` file contains the main information about your module such as name, version, providers, etc..

```json
{
    "alias": "my-blog",
    "icon": "fas fa-pen",
    "version": "1.0.0",
    "active": 1,
    "providers": [
        "Modules\\MyBlog\\Providers\\Main"
    ],
    "aliases": {},
    "files": [],
    "requires": [],
    "reports": [],
    "widgets": [],
    "settings": []
}
```

You can check the **Offline Payments** module built into the Akaunting core as a live example.

### Showing to the user

If your module has pages that need to be shown in the left sidebar, you can check [this](https://akaunting.com/docs/developer-manual/menu) article to learn more.

### More

[Module](https://github.com/akaunting/module/wiki) documentation can help to understand how the system works.
