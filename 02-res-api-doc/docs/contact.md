# Contact API Spesification

## Create Contact API

- Endpoint: POST /api/contacts
- Header : Authorization : Bearer <acess_token>
- Request Body:

```json
{
  "firstName": "Muhammad Rizki",
  "email": "riskideveloper2@gmail.com",
  "phone": "123456789",
  "address": [
    {
      "addressType": "Rumah",
      "street": "Jl. Iskandar Muda",
      "city": "Lhokseumawe",
      "province": "Aceh",
      "country": "Indonesia",
      "zipCode": "12345",
      "contactId": "1"
    }
  ],
  "userId": "xxxxxxxxxxxxx"
}
```

- Response Sucess :

```json
{
  "error": null,
  "message": "Kontak berhasil dibuat",
  "data": [
    {
      "id": 1,
      "firstName": "Muhammad Rizki",
      "lastName": "Syahputra",
      "fullName": "Muhammad Rizki Syahputra",
      "email": "riskideveloper2@gmail.com",
      "phone": "123456789",
      "address": [
        {
          "addressType": "Rumah",
          "street": "Jl. Iskandar Muda",
          "city": "Lhokseumawe",
          "province": "Aceh",
          "country": "Indonesia",
          "zipCode": "12345",
          "contactId": "1"
        }
      ],
      "user_id": "xxxxxxxxxxxxxx"
    }
  ],
  "userId": "xxxxxxxxxxxxx"
}
```

- Response Error :

```json
{
  "error": ["Nama harus diisi", "Email harus diisi"],
  "message": "Kontak gagal dibuat",
  "data": null
}
```

## Search Contact API

- Endpoint : GET /api/contacts
- Header: Authorization : Bearer <acess_token>
- Request Body :

```json
{
  "search": "value"
}
```

- Response Success :

```json
{
  "errors": null,
  "message": "Get contact berhasil",
  "data": [
    {
      "id": 1,
      "firstName": "Muhammad Rizki",
      "lastName": "Syahputra",
      "fullName": "Muhammad Rizki Syahputra",
      "email": "riskideveloper2@gmail.com",
      "phone": "123456789",
      "userId": "xxxxxxxxxxxxxxxxxxxxxxxxx",
      "address": [
        {
          "id": 1,
          "addressType": "Rumah",
          "street": "Jl. Iskandar",
          "city": "Lhokseumawe",
          "province": "Aceh",
          "country": "Indonesia",
          "zipCode": "12345",
          "contactId": 1
        },
        {
          "id": 2,
          "addressType": "Kantor",
          "street": "Jl. Iskandar",
          "city": "Lhokseumawe",
          "province": "Aceh",
          "country": "Indonesia",
          "zipCode": "12345",
          "contactId": 1
        }
      ]
    }
  ]
}
```

- Response Error :

```json
{
  "error": ["Kontak tidak ditemukan"],
  "message": "Get contact gagal",
  "data": null
}
```

## Get Contact API

- Endpoint : GET /api/contact/:id
- Header : Authorization : Bearer <acess_token>
- Request Body :
- Response Sucess :

```json
{
  "errors": null,
  "message": "Get contact berhasil",
  "data": {
    "id": 1,
    "firstName": "Muhammad Rizki",
    "lastName": "Syahputra",
    "fullName": "Muhammad Rizki Syahputra",
    "email": "riskideveloper2@gmail.com",
    "phone": "123456789",
    "userId": "xxxxxxxxxxxxxxxxxxxxxxxxx",
    "address": [
      {
        "id": 1,
        "addressType": "Rumah",
        "street": "Jl. Iskandar",
        "city": "Lhokseumawe",
        "province": "Aceh",
        "country": "Indonesia",
        "zipCode": "12345",
        "contactId": 1
      },
      {
        "id": 2,
        "addressType": "Kantor",
        "street": "Jl. Iskandar",
        "city": "Lhokseumawe",
        "province": "Aceh",
        "country": "Indonesia",
        "zipCode": "12345",
        "contactId": 1
      }
    ]
  }
}
```

- Response Error :

```json
{
  "errors": ["Kontak tidak ditemukan"],
  "message": "Get contact gagal",
  "data": null
}
```

## Update Contact API

- Endpoint : PUT /api/contact/:id
- Header : Authorization : Bearer <acess_token>
- Request Body :

```json
{
  "firstName": "Pojok",
  "lastName": "Code",
  "email": "riskideveloper2@gmail.com",
  "phone": "123456789"
}
```

- Response Sucess :

```json
{
  "errors": null,
  "message": "Update contact berhasil",
  "data": {
    "id": 1,
    "firstName": "Muhammad Rizki",
    "lastName": "Syahputra",
    "fullName": "Muhammad Rizki Syahputra",
    "email": "riskideveloper2@gmail.com",
    "phone": "123456789",
    "userId": "xxxxxxxxxxxxxxxxxxxxxxxxx"
  }
}
```

- Response Error :

```json
{
  "errors": ["Kontak tidak ditemukan"],
  "message": "Update contact gagal",
  "data": null
}
```

## Delete Contact API

- Endpoint : DELETE /api/contact/:id
- Header : Authorization : Bearer <acess_token>
- Request Body :
- Response Sucess :

```json
{
  "errors": null,
  "message": "Delete contact berhasil",
  "data": {
    "id": 1,
    "firstName": "Muhammad Rizki",
    "lastName": "Syahputra",
    "fullName": "Muhammad Rizki Syahputra",
    "email": "riskideveloper2@gmail.com",
    "phone": "123456789"
  }
}
```

- Response Error :

```json
{
  "errors": ["Kontak tidak ditemukan"],
  "message": "Delete contact gagal",
  "data": null
}
```
