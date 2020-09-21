## Show Person

```shell
curl --location --request GET "http://localhost:3000/v1/people/{person_id}" \
     --header "Content-Type: application/json" \
     --header "person: {person_id}"
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

This endpoint retrieves a person.

### HTTP Request

`GET http://localhost:3000/v1/people/{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the person to retrieve

### Response Status

Code | Meaning
--------- | -------
200 | Ok
