---
tags: [Getting Started, Postman, Tutorial]
---


# Postman Test Tutorial

This section aims to demonstrate the initial settings that must be applied to Postman's Collection, before making requests to available Fiservs APIs.

If you have not used the Postman tool as an HTTP client to test requests, access the tool's official link for more information: [Postman Official](https://www.postman.com/)

## Import Collection

### 1. Open Postman and click the import button to open the provided collection

![Postman!](/assets/images/postman/postman-tutorial_1.png "Postman")

### 2. After importing the collection, you will see the next one contains the requests divided by folders according to each entity and also initial requests, for example, "Get Access Token"

![Postman!](/assets/images/postman/postman-tutorial_2.png "Postman")

## Create Environment

### 3. In this step we will configure the environment necessary to execute requests in Postman dynamically, as the requests are already configured with environment variables which we will configure next. Click the environments button and follow the next steps

![Postman!](/assets/images/postman/postman-tutorial_3.png "Postman")

### 4. Click on the button again in the Environment section to create an environment to execute requests

![Postman!](/assets/images/postman/postman-tutorial_4.png "Postman")

### 5. Click on the environment and after define the name of this environment

![Postman!](/assets/images/postman/postman-tutorial_5.png "Postman")

## Configure collection

### 6. Now create the variables like the next example with the credentials sent, in this step you can define which variables will be used throughout the use of the Collection, such as endpoint, port and others

![Postman!](/assets/images/postman/postman-tutorial_6.png "Postman")

### 7. In the upper right corner, select the environment created to apply the settings of the environment variables created in the previous step

![Postman!](/assets/images/postman/postman-tutorial_7.png "Postman")

### 8. If you have followed the steps so far correctly, the environment is ready to send requests to the APIs. Click on Get Access Token API to start the API test

![Postman!](/assets/images/postman/postman-tutorial_8.png "Postman")                      

## Execute first request

### 9. Click on send button

![Postman!](/assets/images/postman/postman-tutorial_9.png "Postman")

### 10. You will notice that you have got an "access_token" which is automatically set in the "token" environment variable and has an expiration date. When the token expires, you'll need to repeat the step above

![Postman!](/assets/images/postman/postman-tutorial_10.png "Postman")

You are now ready to start trying out our API!

---

## See Also

- [Getting Started](?path=docs/english/2-getting-started.md)
- [Terminology](?path=docs/english/getting-started/1-terminology.md)
- [Structure](?path=docs/english/getting-started/3-structure.md)

---
