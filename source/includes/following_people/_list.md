## List Following People

```shell
curl --location --request GET "http://localhost:3000/v1/following_people" \
     --header "Content-Type: application/json" \
     --header "person: {person_id}" \
     --data-raw "{body}"
```

> Body example

```json
{
    "q": {
        "person_name_cont": "Moshe"
    },
    "p": {
        "page": 1,
        "per_page": 5
    },
    "s": "person_name asc"
}
```

> Response JSON structure:

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

We are using ransack for searching, paginate and sorting the data,
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
