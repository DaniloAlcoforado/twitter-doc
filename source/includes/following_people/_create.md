# Following People

## Create Follower Person

```shell
curl --location --request POST "http://localhost:3000/v1/following_people" \
     --data-raw "{body}"
```

> Body example

```json
{
    "following_person": {
        "person_id": 3
    }
}
```

> The above command returns JSON structured like this:

```json
{
    "data": {
        "id": "3",
        "type": "following_person",
        "attributes": {
            "created_at": "2020-09-19T14:53:29.082Z",
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
                    "id": "3",
                    "type": "person",
                    "attributes": {
                        "name": "In Lemke",
                        "email": "estrella@bayer.info",
                        "phone": "1-719-214-7274"
                    }
                }
            }
        }
    }
}
```

This endpoint create a follower relation between logged in person and sended person.

### HTTP Request

`POST http://localhost:3000/v1/following_people`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
following_person | hash | Hash with all person data.
following_person.person_id | integer | Person to follow.
