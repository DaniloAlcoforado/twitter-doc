## Delete Tweet

```shell
curl --location --request GET "http://localhost:3000/v1/tweets/:id" \
     --header "person: 1"
```

> The above command returns a empty body.

This endpoint delete the tweet if belongs to logged in person

### HTTP Request

`GET http://localhost:3000/v1/tweets/:id`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the tweet to delete
