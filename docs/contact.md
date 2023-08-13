# Contact API Spec

## Create Contact API

Endpoint : POST /api/contacts

Headers : 
- Authorization : token

Request Body : 
```json
{
    "first_name" : "Naff",
    "last_name" : "Sisky",
    "email" : "nap@mail.com",
    "phone" : "123456"
}
```

Response Body Success : 
```json
{
    "data" : {
        "id" : 1,
        "first_name" : "Naff",
        "last_name" : "Sisky",
        "email" : "nap@mail.com",
        "phone" : "123456"
    }
}
```

Response Body Error : 
```json
{
    "errors" : "Format email tidak valid!"
}
```
## Update Contact API

Endpoint : PUT /api/contacts

Headers : 
- Authorization : token

Request Body :
```json
{
    "first_name" : "Naff",
    "last_name" : "Sisky",
    "email" : "nap@mail.com",
    "phone" : "123456"
}
```

Response Body Success : 
```json
{
    "data" : {
        "id" : 1,
        "first_name" : "Naff",
        "last_name" : "Sisky",
        "email" : "nap@mail.com",
        "phone" : "123456"
    }
}
```
Response Body Error : 
```json
{
    "errors" : "Format email tidak valid!"
}
```
## Get Contact API

Endpoint : GET /api/contacts/:id

Headers : 
- Authorization : token

Response Body Success : 
```json
{
    "data" : {
        "id" : 1,
        "first_name" : "Naff",
        "last_name" : "Sisky",
        "email" : "nap@mail.com",
        "phone" : "123456"
    }
}
```

Response Body Error : 
```json
{
    "errors" : "Kontak tidak ditemukan!"
}
```

## Search Contact API

Endpoint : GET /api/contacts

Headers : 
- Authorization : token

Query params : 
- name : Search by first or last name, using like, opsional
- email : Search by email, using like, opsional
- phone : Search by phone, using like, opsional
- page : number of page, default 1
- size : size of page, default 10

Response Body Success : 
```json
{
    "data" : [
        {
            "id" : 1,
            "first_name" : "Naff",
            "last_name" : "Sisky",
            "email" : "nap@mail.com",
            "phone" : "123456"
        },
        {
            "id" : 2,
            "first_name" : "Naff",
            "last_name" : "Sisky",
            "email" : "nap@mail.com",
            "phone" : "123456"
        }
    ],
    "pagging" : {
        "page" : 1, 
        "total_page" : 3,
        "total_item" : 30
    }
}
```

Response Body Error : 

# Remove Contact API

Endpoint : DELETE /api/contacts/:id

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
    "errors" : "Kontak tidak ditemukan!"
}
``` 