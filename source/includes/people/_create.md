# People

## Create Person

```shell
curl --location --request POST "http://localhost:3000/v1/people" \
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

> The above command returns JSON structured like this:

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

Parameter | Default | Description
--------- | ------- | -----------
person | hash | Hash with all person data.
person.name | string | Person name.
person.email | string | Person e-mail.
person.phone | string | Person phone number.
