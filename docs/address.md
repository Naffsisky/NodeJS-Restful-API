# Address API Spec

## Create Address API

Endpoint : POST /api/contacts/:contactId/addresses

Headers :
- Authorization : token

Request Body :
```json
{
    "street" : "Jl. Siliwangi",
    "city" : "Rangkasbitung",
    "province" : "Banten",
    "country" : "Indonesia",
    "postal_code" : "123456"
}
```

Response Body Success : 
```json
{
    "data" : {
        {
            "id" : 1,
            "street" : "Jl. Siliwangi",
            "city" : "Rangkasbitung",
            "province" : "Banten",
            "country" : "Indonesia",
            "postal_code" : "123456"
        }
    }
}
```

Response Body Error : 
```json
{
    "errors" : "Negara is required!"
}
```

## Update Address API

Endpoint : PUT /api/contacts/:contactId/addresses/:addressId

Headers :
- Authorization : token

Request Body :
```json
{
    "street" : "Jl. Siliwangi",
    "city" : "Rangkasbitung",
    "province" : "Banten",
    "country" : "Indonesia",
    "postal_code" : "123456"
}
```

Response Body Success : 
```json
{
    "data" : {
        {
            "id" : 1,
            "street" : "Jl. Siliwangi",
            "city" : "Rangkasbitung",
            "province" : "Banten",
            "country" : "Indonesia",
            "postal_code" : "123456"
        }
    }
}
```

Response Body Error : 
```json
{
    "errors" : "Negara is required!"
}
```

## Get Address API

Endpoint : GET /api/contacts/:contactId/addresses/:addressId

Headers :
- Authorization : token

Response Body Success : 
```json
{
    "data" : {
        {
            "id" : 1,
            "street" : "Jl. Siliwangi",
            "city" : "Rangkasbitung",
            "province" : "Banten",
            "country" : "Indonesia",
            "postal_code" : "123456"
        }
    }
}
```

Response Body Error : 
```json
{
    "errors" : "Contact tidak ada!"
}
```
## List Addresses API

Endpoint : GET /api/contacts/:contactId/addresses

Headers :
- Authorization : token

Response Body Success : 
```json
{
    "data" : [
        {
            "id" : 1,
            "street" : "Jl. Siliwangi",
            "city" : "Rangkasbitung",
            "province" : "Banten",
            "country" : "Indonesia",
            "postal_code" : "123456"
        },
        {
            "id" : 2,
            "street" : "Jl. Siliwangi",
            "city" : "Rangkasbitung",
            "province" : "Banten",
            "country" : "Indonesia",
            "postal_code" : "123456"
        }
    ]
    
}
```

Response Body Error : 
```json
{
    "errors" : "Contact tidak ada!"
}
```

## Remove Address API

Endpoint : DELETE /api/contacts/:contactId/addresses/:addressId

Headers :
- Authorization : token

Response Body Success : 
```json
{
    "data" : "OK"
}
```

Response Body Error : 
```json
{
    "errors" : "Contact tidak ada!"
}
```