#Basics

When working with the API, you will need to know which endpoints are available and how to interact with them. This section provides an overview of the basic API functionality and how to use it effectively.

## Endpoints

### Authentication

The only REST endpoint is `auth/google` which is used for Google OAuth2 authentication. Since this is challenging to make it work with graphql, we have decided to use REST for this endpoint. This endpoint is used to authenticate users using their Google account. Ones authenticated, the user will be redirected to the frontend with a JWT token in the URL. You can ask for spesific callBackURL by adding `?callbackUri=YOUR_URL

**Try it out:**

[http://local.qq.api.com/auth/google?callbackUri=https://homelab-kaleici.space] (http://local.qq.api.com/auth/google?callbackUri=https://homelab-kaleici.space)

You dont need to be authenticated to use this endpoint. But this is the only endpoint that you can use without authentication. Rest of it it needs a api key.

```bash
curl -X GET "any" -H "qq-api-key: YOUR_API_KEY"
```

### GraphQL

The GraphQL endpoint is `/graphql` which is used for all other API requests. This endpoint is used to query and mutate data in the system. You can use tools like GraphiQL or Postman to interact with the API. But you dont need to set a tool to use it. You can use it directly from the browser. 

**Try it out:**
[http://local.qq.api.com/graphql](http://local.qq.api.com/graphql)


