## Delete Followers

```shell
curl --location --request DELETE "http://localhost:3000/v1/following_people/{following_person_id}" \
     --header "Content-Type: application/json" \
     --header "person: {person_id}"
```

This endpoint deletes the following person if it is followed by the logged in person

### HTTP Request

`GET http://localhost:3000/v1/following_people/{following_person_id}`

### URL Parameters

Parameter | Description
--------- | -----------
following_person_id | The ID of the following person to be deleted

### Response Status

Code | Meaning
--------- | -------
204 | No Content.
