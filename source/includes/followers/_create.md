# Followers

## Create Follower

```shell
curl --location --request POST "http://localhost:3000/v1/followers" \
     --header "Content-Type: application/json" \
     --header "person: {person_id}" \
     --data-raw "{body}"
```

> Body example

```json
{
    "follower": {
        "followed_id": 3
    }
}
```

> Response JSON structure:

```json
{
    "data": {
        "id": "3",
        "type": "person",
        "attributes": {
            "name": "Douglass Bartoletti",
            "email": "nenita.anderson@example.com",
            "phone": "401.219.9318"
        }
    }
}
```

This endpoint create a follower relation between logged in person and followed person.

### HTTP Request

`POST http://localhost:3000/v1/followers`

### Query Parameters

Parameter | Type | Description
--------- | ------- | -----------
follower | hash | Hash with all following person data.
follower.followed_id | integer | Person to follow.

### Response Status

Code | Meaning
--------- | -------
201 | Created.
