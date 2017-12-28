Modules
=======

Akaunting ships with core accounting tools needed to manage the money. It also has a module structure so that you could extend it. Akaunting uses the [nWidart](https://github.com/nWidart/laravel-modules) module package as builder.

Module is like a Laravel package, it has some routes, views, controllers or models. While technical we call it `Module`, we name it `App` for the end-user as that's what they are familiar to.

### Folder Structure

As you can see from the example bellow, the structure of a module is very similar to the core Laravel's one.

```
app/
bootstrap/
config/
database/
modules/
  ├── Blog/
      ├── Assets/
      ├── Config/
      ├── Console/
      ├── Database/
          ├── Migrations/
          ├── Seeders/
      ├── Http/
          ├── Controllers/
          ├── Middleware/
          ├── Requests/
          ├── routes.php
      ├── Listeners/
      ├── Models/
      ├── Providers/
          ├── BlogServiceProvider.php
      ├── Resources/
          ├── lang/
          ├── views/
      ├── Repositories/
      ├── Tests/
      ├── composer.json
      ├── module.json
      ├── start.php
public/
...
vendor/
.env
```

### Creating a module

We preferred nWidart's module package as it has a lot of Artisan commands built-in. For example, let's see how to create a new module:

```
php artisan module:make Blog
```

This will create all files and folders shown in the above example. Now lets install the module using the following command:

```
php artisan module:install blog 1
```

`blog` is the **alias** of the module and `1` is the **company id** that you want to install the module. [Here](https://akaunting.com/docs/user-manual/companies) you can find more about companies in Akaunting.


[Here](https://nwidart.com/laravel-modules/v1/advanced-tools/artisan-commands) you can find the full list of commands.

### module.json file

The `module.json` file contains the main information such as name, version, providers etc about your module.

```
{
    "name": "Blog",
    "alias": "blog",
    "description": "This is my new module.",
    "version": "1.0.0",
    "category": "payment-gateway",
    "keywords": [],
    "active": 1,
    "order": 0,
    "providers": [
        "Modules\\Blog\\Providers\\BlogServiceProvider"
    ],
    "aliases": {},
    "files": [
        "start.php"
    ],
    "requires": [],
    "settings": []
}
```

You can check the **Offline Payments** module built-in Akaunting as a live example.

### Showing to the user

If your module has pages that needs to be shown in the left sidebar then you can check [this](https://akaunting.com/docs/developer-manual/menu) article to learn more about.

### More

nWidart's documentation can help to learn more about the [facade methods](https://nwidart.com/laravel-modules/v1/advanced-tools/facade-methods), [namespace](https://nwidart.com/laravel-modules/v1/basic-usage/custom-namespaces), [module methods](https://nwidart.com/laravel-modules/v1/advanced-tools/module-methods) etc.