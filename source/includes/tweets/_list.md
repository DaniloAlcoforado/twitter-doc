## list Tweets

```shell
curl --location --request GET "http://localhost:3000/v1/tweets" \
     --header "Content-Type: application/json" \
     --header "person: {person_id}" \
     --data-raw "{body}"
```

> Body example

```json
{
    "q": {
        "content_cont": "Organic"
    },
    "p": {
        "page": 1,
        "per_page": 5
    },
    "s": "created_at desc"
}
```

> Response JSON structure.

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

This endpoint retrieves all tweets of the logged in person and all tweets of the people this person follows.

### HTTP Request

`GET http://localhost:3000/v1/tweets`

### Query Parameters

Ransank is being used for searching, paginate and sorting the data,
Click below to see the condition list for searching

[Filter List](https://github.com/activerecord-hackery/ransack#search-matchers)

Parameter | Type | Description
--------- | ------- | -----------
q | hash | Ransack search content data
q.{field}_{condition} | text | Search parameters
s | text | Ransack sort data
p | hash | Ransack pagination data
q.page | integer | List page number
q.per_page | integer | Data quantity per page

### Response Status

Code | Meaning
--------- | -------
200 | Ok
