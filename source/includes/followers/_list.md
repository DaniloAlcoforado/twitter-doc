## List Followers

```shell
curl --location --request GET "http://localhost:3000/v1/followers" \
     --header "Content-Type: application/json" \
     --header "person: {person_id}" \
     --data-raw "{body}"
```

> Body example

```json
{
    "q": {
        "name_cont": "Moshe"
    },
    "p": {
        "page": 1,
        "per_page": 5
    },
    "s": "name asc"
}
```

> Response JSON structure:

```json
{
    "data": [
        {
            "id": "3",
            "type": "person",
            "attributes": {
                "name": "Douglass Bartoletti",
                "email": "nenita.anderson@example.com",
                "phone": "401.219.9318"
            }
        }
    ],
    "meta": {
        "pagination": {
            "current_page": 1,
            "previous_page": null,
            "next_page": null,
            "total_pages": 1,
            "total_count": 1
        }
    }
}
```

This endpoint return all person that follows the logged in person.

### HTTP Request

`GET http://localhost:3000/v1/followers`

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

### Response Status

Code | Meaning
--------- | -------
200 | Ok
