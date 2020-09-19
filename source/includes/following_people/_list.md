## List Following People

```shell
curl --location --request GET "http://localhost:3000/v1/following_people" \
     --header "person: 1"
```

> The above command returns JSON structured like this:

```json
{
    "data": [
        {
            "id": "1",
            "type": "following_person",
            "attributes": {
                "created_at": "2020-09-19T12:13:53.833Z",
                "follower": {
                    "data": {
                        "id": "1",
                        "type": "person",
                        "attributes": {
                            "name": "Petrina Dicki IV",
                            "email": "giovanni.schroeder@armstrong.co",
                            "phone": "868.801.1787"
                        }
                    }
                },
                "followed": {
                    "data": {
                        "id": "2",
                        "type": "person",
                        "attributes": {
                            "name": "Moshe Skiles",
                            "email": "angela@beatty-mosciski.name",
                            "phone": "265-771-4092"
                        }
                    }
                }
            }
        },
    ],
    "meta": {
        "pagination": {
            "current_page": 1,
            "previous_page": null,
            "next_page": null,
            "total_pages": 1,
            "total_count": 2
        }
    }
}
```

This endpoint return all person that the logged in person follows.

### HTTP Request

`GET http://localhost:3000/v1/following_people`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
ransack | false | If set to true, the result will also include cats.
