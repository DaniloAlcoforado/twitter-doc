## Get Related Tweet

```shell
curl --location --request GET "http://localhost:3000/v1/tweets" \
     --header "person: 1"
```

> The above command returns JSON structured like this:

```json
{
    "data": [
        {
            "id": "32",
            "type": "tweet",
            "attributes": {
                "content": "Organic direct trade meh gentrify artisan. Tofu carry celiac kombucha. Wolf drinking photo booth cliche fixie xoxo. Cornhole fanny pack austin occupy. Roof yuccie master pinterest keytar actually humblebrag williamsburg. Mumblecore lumbersexual church-key shoreditch. Kickstarter.",
                "created_at": "2020-09-19T12:16:17.067Z",
                "person": {
                    "data": {
                        "id": "4",
                        "type": "person",
                        "attributes": {
                            "name": "Xochitl DuBuque",
                            "email": "seymour.harvey@kertzmann-waelchi.co",
                            "phone": "152-255-7539"
                        }
                    }
                }
            }
        }
    ],
    "meta": {
        "pagination": {
            "current_page": 1,
            "previous_page": null,
            "next_page": null,
            "total_pages": 1,
            "total_count": 20
        }
    }
}
```

This endpoint retrieves all logged in person tweet and all following person tweet.

### HTTP Request

`GET http://localhost:3000/v1/tweets`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
ransack | false | If set to true, the result will also include cats.
