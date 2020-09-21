# People

## Create Person

```shell
curl --location --request POST "http://localhost:3000/v1/people" \
     --header "Content-Type: application/json" \
     --data-raw "{body}"
```

> Body example

```json
{
  "person": {
    "name": "Petrina Dicki IV",
    "email": "giovanni.schroeder@armstrong.co",
    "phone": "868.801.1787"
  }
}
```

> Response JSON structure:

```json
{
    "data": {
        "id": "1",
        "type": "person",
        "attributes": {
            "name": "Petrina Dicki IV",
            "email": "giovanni.schroeder@armstrong.co",
            "phone": "868.801.1787"
        }
    }
}
```

This endpoint create a person.

### HTTP Request

`POST http://localhost:3000/v1/people`

### Query Parameters

Parameter | Type | Description
--------- | ------- | -----------
person | hash | Hash with all person data.
person.name | string | Person name.
person.email | string | Person e-mail.
person.phone | string | Person phone number.

<aside class="warning">
You don't need to pass the person id at header to create a person.
</aside>