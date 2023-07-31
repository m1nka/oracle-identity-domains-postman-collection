# Postman collection for Oracle Identity Domains: Easy way to use REST APIs

> You can find a [tutorial on how to use this Postman collection](https://maximilian.tech/2023/07/31/postman-collection-for-oracle-identity-domains-easy-way-to-use-rest-apis/) in my blog. 

This Postman collection was forked from the [official SCIM 2.0 Postman collection](https://www.postman.com/postman/workspace/scim/documentation/6248949-de4a96e2-9ebf-426f-bc55-4c5f2de51ab2). With this collection you can easily connect to Oracle Identity Domains via Postman using the SCIM 2.0 endpoints.

To use this collection:

- Import [this Postman collection](https://raw.githubusercontent.com/m1nka/oracle-identity-domains-postman-collection/main/Oracle%20Identity%20Domains%20-%20REST%20API.postman_collection.json) in your Postman client. 
- Open the collection **variables** and enter `url`, `client_id` and `client_secret`. More info on how to get these variables [in my blog article](https://maximilian.tech/2023/07/31/postman-collection-for-oracle-identity-domains-easy-way-to-use-rest-apis/). 
- Go to **Authorization** and at the bottom click **Get new access token** and then **Use token**.
    
That's it, hopefully all requests should work now.
