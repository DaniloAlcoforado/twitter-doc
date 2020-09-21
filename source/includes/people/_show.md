## Show Person

```shell
curl --location --request GET "http://localhost:3000/v1/people/{id}" \
  --header "person: {id}"
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

This endpoint retrieves a person.

### HTTP Request

`GET http://localhost:3000/v1/people/{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the person to retrieve
