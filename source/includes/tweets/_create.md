# Tweets

## Create Tweet

```shell
curl --location --request POST "http://localhost:3000/v1/tweets" \
     --data-raw 'body'
```

> Body example

```json
{
    "tweet": {
        "content": "Lorem ipsum felis quisque enim tempus, conubia senectus himenaeos ultrices tortor, dapibus diam vulputate pellentesque."
    }
}
```

> The above command returns JSON structured like this:

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

Parameter | Default | Description
--------- | ------- | -----------
tweet | hash | Hash with all person data.
tweet.content | string | Tweet content text.
