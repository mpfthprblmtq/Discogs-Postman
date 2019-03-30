# Discogs Postman
A Postman collection for Discogs public API. 
## Steps to get up and running
Follow these steps to quickly get up and running with the Discogs public API and Postman:

### 1. Import the Discogs collection and environment into Postman
Click the button below and select the Desktop version of Postman (Chrome extension doesn't support environment variables):

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/ed71222b7df2030db1d2#?env%5BDiscogs%5D=W3sia2V5IjoidXJsIiwidmFsdWUiOiJodHRwczovL2FwaS5kaXNjb2dzLmNvbSIsImRlc2NyaXB0aW9uIjoiIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJ1c2VyX2FnZW50IiwidmFsdWUiOiJQb3N0bWFuRGlzY29ncy8xLjAiLCJkZXNjcmlwdGlvbiI6IiIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiY29uc3VtZXJfa2V5IiwidmFsdWUiOiIiLCJkZXNjcmlwdGlvbiI6IiIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiY29uc3VtZXJfc2VjcmV0IiwidmFsdWUiOiIiLCJkZXNjcmlwdGlvbiI6IiIsImVuYWJsZWQiOnRydWV9LHsidmFsdWUiOiIiLCJrZXkiOiJvYXV0aF90b2tlbiIsImVuYWJsZWQiOnRydWV9LHsidmFsdWUiOiIiLCJrZXkiOiJvYXV0aF90b2tlbl9zZWNyZXQiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6Im9hdXRoX3ZlcmlmaWVyIiwidmFsdWUiOiIiLCJkZXNjcmlwdGlvbiI6IiIsImVuYWJsZWQiOnRydWV9XQ==)

### 2. Create a public app at https://www.discogs.com/settings/developers
Go to the Discogs developer portal and create a public app.

![create a public app](images/create-app.png)

### 3. Add your consumer key and consumer secret to the Discogs environment variables in Postman
Copy the consumer key and consumer secret of your app into the `consumer_key` and `consumer_secret` environment variables in Postman.

![get credentials](images/credentials.png)

![manage environment](images/environment.png)

### 4. Select the Discogs environment
Select Discogs from the environment drop-down menu in Postman

![select environment](images/select-enviroment.png)

### 5. Get your request token
Open the Authentication folder and send GET Request Token call in Postman. 

In the response section go to the Test Results tab and copy the authorization url.

![GET request token](images/request-token.png)

### 6. Get your oauth verifier
Paste the authorization url into your browser, login to Discogs and authorize the application.

![Authorize application](images/authorize-application.png)

If the application doesn't have a valid callback url, you will be redirected to a 404 page. You find the `oauth_verifier` as last parameter of the webpage url, copy the value and paste it into the `oauth_verifier` environment variable in Postman.

![Application callback](images/application-callback.png)
![Copy and paste the oauth_verifier](images/enviroment-verifier.png)


### 7. Get your access token
Open the Authentication folder and send POST Access Token call in Postman. 

![POST access token](images/access-token.png)

Congrats! You're now authenticated and can start making API calls.

### 8. Make your first API call!
Open the User identity folder and click Send on the GET Identity request to make your first API call.

## Discogs public API documentation
You find more informations regarding Discogs public APIs ![here](https://www.discogs.com/developers/)

## Contibuting
Contribution are very welcome 
If you spot any bug, open a new issue or pull request.

## Licence
MIT
