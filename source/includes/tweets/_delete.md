## Delete Tweet

```shell
curl --location --request DELETE "http://localhost:3000/v1/tweets/{tweet_id}" \
     --header "Content-Type: application/json" \
     --header "person: {person_id}"
```

> Response JSON structure.

This endpoint deletes the tweet if it belongs to the logged in person

### HTTP Request

`GET http://localhost:3000/v1/tweets/{tweet_id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the tweet to be deleted

### Response Status

Code | Meaning
--------- | -------
204 | No Content.
