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

```php
$api = app('Dingo\Api\Routing\Router');
$api->get('products', 'Catalog/Products@index');
```

Check out the documentation of [Dingo API](https://github.com/dingo/api/wiki/Creating-API-Endpoints) for further details on API endpoints.

### Transformers

Transformers allow you to easily and consistently transform objects into an array. You can find the transformers of Akaunting in the following directory:

```
app/Transformers
```

### API Blueprint

# 📁 Collection: Companies 


## End-point: Companies
### Description: 
Method: GET
>```
>{{akaunting_url}}/companies
>```
### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Get owner of company
### Description: 
Method: GET
>```
>{{akaunting_url}}/companies/{{akaunting_company_id}}/owner
>```
### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Enable company
### Description: 
Method: GET
>```
>{{akaunting_url}}/companies/{{akaunting_company_id}}/enable
>```
### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Disable company
### Description: 
Method: GET
>```
>{{akaunting_url}}/companies/{{akaunting_company_id}}/disable
>```
### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

# 📁 Collection: Items 


## End-point: Items
### Description: 
Method: GET
>```
>{{akaunting_url}}/items?company_id={{akaunting_company_id}}&page={{akaunting_page}}&limit={{akaunting_limit}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|page|{{akaunting_page}}|
|limit|{{akaunting_limit}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Enable item
### Description: 
Method: GET
>```
>{{akaunting_url}}/items/{{akaunting_item_id}}/enable?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Disable item
### Description: 
Method: GET
>```
>{{akaunting_url}}/items/{{akaunting_item_id}}/disable?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Delete item
### Description: 
Method: DELETE
>```
>{{akaunting_url}}/items/{{akaunting_item_id}}/disable?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Get item
### Description: 
Method: GET
>```
>{{akaunting_url}}/items/{{akaunting_item_id}}?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Create item
### Description: 
Method: POST
>```
>{{akaunting_url}}/items?company_id={{akaunting_company_id}}&name=Demo&description=Demo description&sale_price=23.3&purchase_price=21.1&category_id={{akaunting_category_id}}&tax_ids=[]
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|name|Demo|
|description|Demo description|
|sale_price|23.3|
|purchase_price|21.1|
|category_id|{{akaunting_category_id}}|
|tax_ids|[]|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Update item
### Description: 
Method: PUT
>```
>{{akaunting_url}}/items/{{akaunting_item_id}}?company_id={{akaunting_company_id}}&name=Demo&description=Demo description&sale_price=233&purchase_price=211&category_id={{akaunting_category_id}}&tax_ids=[]
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|name|Demo|
|description|Demo description|
|sale_price|233|
|purchase_price|211|
|category_id|{{akaunting_category_id}}|
|tax_ids|[]|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

# 📁 Collection: Accounts 


## End-point: Accounts
### Description: 
Method: GET
>```
>{{akaunting_url}}/accounts?company_id={{akaunting_company_id}}&page={{akaunting_page}}&limit={{akaunting_limit}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|page|{{akaunting_page}}|
|limit|{{akaunting_limit}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Enable account
### Description: 
Method: GET
>```
>{{akaunting_url}}/accounts/{{akaunting_acount_id}}/enable?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Disable account
### Description: 
Method: GET
>```
>{{akaunting_url}}/accounts/{{akaunting_acount_id}}/disable?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Delete account
### Description: 
Method: DELETE
>```
>{{akaunting_url}}/accounts/{{akaunting_acount_id}}/disable?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Get account
### Description: 
Method: GET
>```
>{{akaunting_url}}/accounts/{{akaunting_acount_id}}?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Create account
### Description: 
Method: POST
>```
>{{akaunting_url}}/accounts?company_id={{akaunting_company_id}}&name=Cach&number=1&currency_code=USD&opening_balance=0&bank_name=My Bank&bank_phone=&bank_address=Bank Address&enabled=1
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|name|Cach|
|number|1|
|currency_code|USD|
|opening_balance|0|
|bank_name|My Bank|
|bank_phone||
|bank_address|Bank Address|
|enabled|1|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Update account
### Description: 
Method: PUT
>```
>{{akaunting_url}}/accounts/{{akaunting_acount_id}}?company_id={{akaunting_company_id}}&name=Cach&number=1&currency_code=USD&opening_balance=0&bank_name=My Bank&bank_phone=&bank_address=Bank Address&enabled=1
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|name|Cach|
|number|1|
|currency_code|USD|
|opening_balance|0|
|bank_name|My Bank|
|bank_phone||
|bank_address|Bank Address|
|enabled|1|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

# 📁 Collection: Categories 


## End-point: Categories
### Description: 
Method: GET
>```
>{{akaunting_url}}/categories?company_id={{akaunting_company_id}}&page={{akaunting_page}}&limit={{akaunting_limit}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|page|{{akaunting_page}}|
|limit|{{akaunting_limit}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Enable category
### Description: 
Method: GET
>```
>{{akaunting_url}}/categories/{{akaunting_category_id}}/enable?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Disable category
### Description: 
Method: GET
>```
>{{akaunting_url}}/categories/{{akaunting_category_id}}/enable?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

# 📁 Collection: Currencies 


## End-point: Currencies
### Description: 
Method: GET
>```
>{{akaunting_url}}/currencies?company_id={{akaunting_company_id}}&page={{akaunting_page}}&limit={{akaunting_limit}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|page|{{akaunting_page}}|
|limit|{{akaunting_limit}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Enable currency
### Description: 
Method: GET
>```
>{{akaunting_url}}/currency/{{akaunting_currency_id}}/enable?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Disable currency
### Description: 
Method: GET
>```
>{{akaunting_url}}/currency/{{akaunting_currency_id}}/disable?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

# 📁 Collection: Taxes 


## End-point: Taxes
### Description: 
Method: GET
>```
>{{akaunting_url}}/taxes?company_id={{akaunting_company_id}}&page={{akaunting_page}}&limit={{akaunting_limit}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|page|{{akaunting_page}}|
|limit|{{akaunting_limit}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Enable tax
### Description: 
Method: GET
>```
>{{akaunting_url}}/taxes/{{akaunting_tax_id}}/enable?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Disable tax
### Description: 
Method: GET
>```
>{{akaunting_url}}/taxes/{{akaunting_tax_id}}/disable?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

# 📁 Collection: Payments 


## End-point: Payments
### Description: 
Method: GET
>```
>{{akaunting_url}}/transactions?company_id={{akaunting_company_id}}&search=type:expense&page={{akaunting_page}}&limit={{akaunting_limit}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|search|type:expense|
|page|{{akaunting_page}}|
|limit|{{akaunting_limit}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Paymen details
### Description: 
Method: GET
>```
>{{akaunting_url}}/transactions/{{akaunting_transaction_id}}?company_id={{akaunting_company_id}}&search=type:expense
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|search|type:expense|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

# 📁 Collection: Revenues 


## End-point: Revenues
### Description: 
Method: GET
>```
>{{akaunting_url}}/transactions?company_id={{akaunting_company_id}}&search=type:income&page={{akaunting_page}}&limit={{akaunting_limit}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|search|type:income|
|page|{{akaunting_page}}|
|limit|{{akaunting_limit}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Revenue details
### Description: 
Method: GET
>```
>{{akaunting_url}}/transactions/{{akaunting_transaction_id}}?company_id={{akaunting_company_id}}&search=type:income
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|search|type:income|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

# 📁 Collection: Invoices 


## End-point: Invoices
### Description: 
Method: GET
>```
>{{akaunting_url}}/documents?company_id={{akaunting_company_id}}&search=type:invoice&page={{akaunting_page}}&limit={{akaunting_limit}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|search|type:invoice|
|page|{{akaunting_page}}|
|limit|{{akaunting_limit}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Invoice create
### Description: 
Method: POST
>```
>{{akaunting_url}}/documents?company_id={{akaunting_company_id}}&search=type:invoice
>```
### Body formdata

|Param|value|Type|
|---|---|---|
|type|invoice|text|
|document|invoice|text|
|currency_code|EUR|text|
|company_id|1|text|
|amount|0|text|
|sort_order|ASC|text|
|status|'draft' or 'sent'|text|
|footer||text|
|issued_at|2021-05-10 00:00:00|text|
|due_at|2021-05-10 00:00:00|text|
|recurring_frequency|no|text|
|contact_id|1|text|
|category_id|2|text|
|currency_rate|1|text|
|prefix|sales|text|
|group|sales|text|
|document_number|000010-10|text|
|contact_name||text|
|setting[title]|Invoice|text|
|setting[subheading]||text|
|setting[company_logo][id]||text|
|items[0][item_id]|1|text|
|items[0][name]|item name|text|
|items[0][description]||text|
|items[0][quantity]||text|
|items[0][price]||text|
|items[0][tax_ids][0]||text|
|items[0][discount]||text|
|items[0][total]||text|
|items[0][grand_total]||text|
|item_backup[0][name]||text|
|item_backup[0][quantity]||text|
|item_backup[0][description]||text|
|pre_discount||text|
|discount||text|
|type||text|
|status||text|
|footer||text|
|||text|
|contact_id|1|text|
|contact_email||text|
|contact_tax_number||text|
|contact_phone||text|
|contact_address||text|
| ||text|
|recurring_frequency||text|
|recurring_interval||text|
|recurring_custom_frequency||text|
|recurring_count||text|
|category_id||text|
|currency_rate||text|


### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|currency_code|EUR|
|contact_id|1|
|search|type:invoice|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Invoice details
### Description: 
Method: GET
>```
>{{akaunting_url}}/documents/{{akaunting_documents_id}}?company_id={{akaunting_company_id}}&search=type:invoice
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|search|type:invoice|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

# 📁 Collection: Bills 


## End-point: Invoices
### Description: 
Method: GET
>```
>{{akaunting_url}}/documents?company_id={{akaunting_company_id}}&search=type:bill&page={{akaunting_page}}&limit={{akaunting_limit}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|search|type:bill|
|page|{{akaunting_page}}|
|limit|{{akaunting_limit}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Invoice details
### Description: 
Method: GET
>```
>{{akaunting_url}}/documents/{{akaunting_documents_id}}?company_id={{akaunting_company_id}}&search=type:bill
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|search|type:bill|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

# 📁 Collection: Customers 


## End-point: Customers
### Description: 
Method: GET
>```
>{{akaunting_url}}/contacts?company_id={{akaunting_company_id}}&search=type:customer&page={{akaunting_page}}&limit={{akaunting_limit}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|search|type:customer|
|page|{{akaunting_page}}|
|limit|{{akaunting_limit}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Customer details
### Description: 
Method: GET
>```
>{{akaunting_url}}/contacts/{{akaunting_contact_id}}?company_id={{akaunting_company_id}}&search=type:customer
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|
|search|type:customer|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Ping - check is login ok
### Description: 
Method: GET
>```
>{{akaunting_url}}/ping
>```
### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃


## End-point: Dashboards
### Description: 
Method: GET
>```
>{{akaunting_url}}/dashboards?company_id={{akaunting_company_id}}
>```
### Query Params

|Param|value|
|---|---|
|company_id|{{akaunting_company_id}}|


### 🔑 Authentication basic

|Param|value|Type|
|---|---|---|



⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

_________________________________________________
