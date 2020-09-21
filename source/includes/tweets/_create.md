# Tweets

## Create Tweet

```shell
curl --location --request POST "http://localhost:3000/v1/tweets" \
     --header "Content-Type: application/json" \
     --header "person: {id}" \
     --data "{body}"
```

> Body example

```json
{
    "tweet": {
        "content": "Lorem ipsum felis quisque enim tempus, conubia senectus himenaeos ultrices tortor, dapibus diam vulputate pellentesque."
    }
}
```

> Response JSON structure.

```json
{
    "data": {
        "id": "33",
        "type": "tweet",
        "attributes": {
            "content": "Lorem ipsum felis quisque enim tempus, conubia senectus himenaeos ultrices tortor, dapibus diam vulputate pellentesque.",
            "created_at": "2020-09-19T14:49:30.924Z",
            "person": {
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
        }
    }
}
```

This endpoint create a tweet.

### HTTP Request

`POST http://localhost:3000/v1/tweets`

### Query Parameters

Parameter | Type | Description
--------- | ------- | -----------
tweet | hash | Hash with all tweet data.
tweet.content | string | Tweet content text.

### Response Status

Code | Meaning
--------- | -------
201 | Created.
