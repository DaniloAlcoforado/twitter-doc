## Get All Person

```shell
curl --location --request GET "http://localhost:3000/v1/people" \
     --header "person: 1"
```

> The above command returns JSON structured like this:

```json
{
    "data": [
        {
            "id": "2",
            "type": "person",
            "attributes": {
                "name": "Moshe Skiles",
                "email": "angela@beatty-mosciski.name",
                "phone": "265-771-4092"
            }
        }
    ],
    "meta": {
        "pagination": {
            "current_page": 1,
            "previous_page": null,
            "next_page": null,
            "total_pages": 1,
            "total_count": 3
        }
    }
}
```

This endpoint retrieves all people excepted the logged in person.

### HTTP Request

`GET http://localhost:3000/v1/people`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
ransack | false | If set to true, the result will also include cats.
