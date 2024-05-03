---
tags: [Getting Started, API Key, API Credential]
---

# Getting Started

This portal contains the API docs and the reference guide to understand it. This page guides you through use and test our Payments API. REST API provides a powerful, convenient, and simple Web services API. Its advantages include ease of integration and development, and it’s an excellent choice of technology for use with mobile applications and Web 2.0 projects.

After these steps, you're ready to start test the Payments API.

## Step 1: Get your API Key

1. Provide the bank’s or financial institution’s name, user/users full name and e-mail address and submit to latamAPIs@fiserv.com and your assigned Account Manager or Commercial representative. If you are new user please share your name and e-mail address to latamAPIs@fiserv.com and we will contact you. 

2. Expect a confirmation e-mail from Fiserv’s assigned Account Manager or Client Partner with the assigned credentials.

### How to get an API Credential?

<img width="1917" alt="apikey1" src="https://github.com/Fiserv/firstvision-latam/assets/111396588/57282a38-45fe-4537-94d6-f7bd11a91cbd">

## Step 2: Explore our API

This section deals with how to access the request execution page in an HTTP client, if you already have the API credentials available, follow the steps below to understand the structure and how each part works.

### 1. Select the API group that you want explore

![image](https://user-images.githubusercontent.com/111396588/223824143-0d2577da-4e91-476d-821e-9c665dd01457.png)

### 2. This button will redirect you to the API docs

You can see the different APIs available for the corresponding group, on the right side you can explore the model detailed definition.

![image](https://user-images.githubusercontent.com/111396588/223824184-806af113-9dbe-4a01-808a-24cdff61630f.png)

### 3. API Structure - On the page of any API resource, there is a division into segments, namely

- Method
- API description
- Download API specification
- Download Postman collection
- Request parameters
- Request body
- Response body
- Response code
- Try out section

<img width="765" alt="postman 3" src="https://github.com/Fiserv/firstvision-latam/assets/111396588/04ccefa1-eb1e-4f03-b143-36314496ce3b">

### 4. Example of body fields

![image](https://user-images.githubusercontent.com/111396588/223824246-d2174d9c-9d0a-4e1b-a287-2ba18d02514d.png)

### 5. Example of response fields

“hasError” - boolean that indicates if there was any error during the execution
“errors” - array that will be filled in case of errorque solo tendrá contenido en caso de error detallando el/los errores que sucedieron. Data contendrá la respuesta del endpoint en caso de éxito. Más que nada porque el “Response” del portal solo contiene la estructura data, y no es la estructura que nosotros retornamos.

![image](https://user-images.githubusercontent.com/111396588/223824287-f11215ff-a306-4522-ad54-9c254e24dd5b.png)

### 6. Example of code errors

![image](https://user-images.githubusercontent.com/111396588/223824322-689bbbd6-c8b5-4d85-8f14-70fb6a7bf91e.png)

### 7. Example of try out section

Is important to fill the headers before Try out.

![image](https://user-images.githubusercontent.com/111396588/223824344-69875caf-2cae-4b95-bac5-1b8d715bef43.png)

---

## See Also

- [Messages List](?path=docs/english/getting-started/messages-list.md)
- [Postman Tutorial](?path=docs/english/getting-started/postman.md)
- [Structure](?path=docs/english/getting-started/structure.md)
- [Terminology](?path=docs/english/getting-started/terminology.md)

---
