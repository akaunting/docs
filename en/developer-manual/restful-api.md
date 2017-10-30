RESTful API
===========

Akaunting provides a RESTful API to create, read, update and delete (CRUD) all entities of Akaunting.

The API of Akaunting is built on top of [Dingo API](https://github.com/dingo/api) package for Laravel. It provides amazing tools such as Content Negotiation, API Versioning, Rate Limiting, Response Transformers, Internal Requests and a lot more.

### Authentication

The HTTP Basic authentication is used by the Akaunting API. Any user that has `read-api` permission may access the API using their email and password. By default, Akaunting gives `read-api` permission to `admin` role.

Permissions for CRUD actions are based on default [ACL](https://akaunting.com/docs/developer-manual/permissions).

### Routes

The API endpoints/routes of Akaunting are located in the following file:

```
routes/api.php
```

You may also add API endpoints to your module:

```
$api = app('Dingo\Api\Routing\Router');
$api->get('products', 'Catalog/Products@index');
```

Check out the documentation of [Dingo API](https://github.com/dingo/api/wiki/Creating-API-Endpoints) for further details on API endpoints.

### Transformers

Transformers allow you to easily and consistently transform objects into an array. You can find the transforems of Akaunting in the following directory:

```
app/Transforms
```

### API Blueprint

Coming soon..