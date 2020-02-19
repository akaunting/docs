Modules
=======

Akaunting ships with core accounting tools needed to manage money. It also has a module structure so that you could extend it. We use our own [akaunting/module](https://github.com/akaunting/module) package as builder.

A module is like a Laravel package, it has some routes, views, controllers, and models. While technically we call it `Module`, we name it `App` in the front-end for the end-user as that's what they are familiar to.

### Folder Structure

As you can see from the example bellow, the structure of a module is very similar to the core Laravel's one.

```
app/
bootstrap/
config/
database/
modules/
  ├── Blog/
      ├── Console/
      ├── Database/
          ├── Migrations/
          ├── Seeders/
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

```
php artisan module:make blog
```

This will create all files and folders shown in the above example. Now lets install the module using the following command:

```
php artisan module:install blog 1
```

`blog` is the **alias** of the module and `1` is the **company id** that you want to install the module. [Here](https://akaunting.com/docs/user-manual/companies) you can find more about companies in Akaunting.

Alias is the unique name of the module as is used everywhere into Akaunting.

### module.json file

The `module.json` file contains the main information such as name, version, providers etc about your module.

```
{
    "alias": "blog",
    "icon": "fas fa-pen",
    "version": "1.0.0",
    "category": "accounting",
    "active": 1,
    "providers": [
        "Modules\\Blog\\Providers\\Main"
    ],
    "aliases": {},
    "files": [],
    "requires": [],
    "reports": [],
    "widgets": [],
    "settings": []
}
```

You can check the **Offline Payments** module built-in Akaunting as a live example.

### Showing to the user

If your module has pages that needs to be shown in the left sidebar then you can check [this](https://akaunting.com/docs/developer-manual/menu) article to learn more about.

### More

[Module](https://github.com/akaunting/module/wiki) documentation can help to understand the how the system works.
