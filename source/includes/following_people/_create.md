# Following People

## Create Follower Person

```shell
curl --location --request POST "http://localhost:3000/v1/following_people" \
     --header "Content-Type: application/json" \
     --header "person: {person_id}" \
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

> Response JSON structure:

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

Parameter | Type | Description
--------- | ------- | -----------
following_person | hash | Hash with all following person data.
following_person.person_id | integer | Person to follow.
