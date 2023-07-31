# Postman collection for Oracle Identity Domains: Easy way to use REST APIs

This Postman collection was forked from the [official SCIM 2.0 Postman collection](https://www.postman.com/postman/workspace/scim/documentation/6248949-de4a96e2-9ebf-426f-bc55-4c5f2de51ab2). With this collection you can easily connect to Oracle Identity Domains via Postman using the SCIM 2.0 endpoints.

To use this collection:

- Import [this Postman collection](https://raw.githubusercontent.com/m1nka/oracle-identity-domains-postman-collection/main/Oracle%20Identity%20Domains%20-%20REST%20API.postman_collection.json) in your Postman client. 
- Open the collection **variables** and enter `url`, `client_id` and `client_secret`.
- Go to **Authorization** and at the bottom click **Get new access token** and then **Use token**.
    

That's it, all requests should work now. Find instructions below on how to create a confidential application in OCI and how to get the variables `url`, `client_id` and `client_secret`.

## Pre-requisites for using this Postman collection

### Step 1: Create a confidential application within your Oracle Identity Domain

Within the Oracle Cloud Infrastructure console, [head to Identity Domains](https://cloud.oracle.com/identity/domains/), choose your root compartment and select your Identity Domain.

- Once your Identity Domain is selected, choose **Applications** and **Add application**.
- Choose **Confidential Application** and enter name for application, for example `identiy-domains-api-access` and click next.
- Choose **Configure this application as a client now** and
    - Under **Authorization**, check **Client credentials**
    - Under **Client type** select **Confidential**
    - Scroll down and in the **Token issuance policy** section, set **Authorized resources** to **Specific**.
    - Select **Add app roles** and choose the roles that you need. All roles [are documented here](https://docs.oracle.com/en/cloud/paas/identity-cloud/uaids/understand-administrator-roles.html#GUID-9B488723-43A1-47B1-ACB0-41FFD780FD5D). In my case, I choose **User administrator**.
    - Choose **Next** and then **Finish** to complete the setup.
    - On the application overview page, click Activate and confirm that you want to activate the application.

### Step 2: Get the client ID, client secret and endpoint URL

- Within in the confidential application that we just created, select **OAuth configuration** (bottom left under resources) and find the **client ID** and **client secret**.
- Next, back to your identity domain (under overview) and **copy** the **Domain URL**. In case the URL includes a port `:443`, you can use the URL without port. Do not use a backslash `/` at the end of the URL.
    

Enter these values into the Postman collection variables and now you are ready to go.
