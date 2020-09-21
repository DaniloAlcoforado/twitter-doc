# Authentication

> Make sure to replace `{id}` with a created person id.

```shell
curl --location --request GET "api_endpoint_here" \
     --header "person: {id}"
```

<aside class="notice">
This API don't have a authentication endpoint, to simulate a user token you have only to send the person id as person in the request header.
</aside>
