How to use Passport for authentication in web services:

1) Install and configure Passport as per:

    https://laravel.com/docs/master/passport

2) To get the access token, fire the request:

    URL: POST http://lara-passport-api.local/oauth/token
    with parameters:
    - grant_type     password
    - client_id      CLIENT_ID
    - client_secret  CLIENT_SECRET
    - username       USER_EMAIL
    - password       USER_PASSWORD

3) To validate access token:

    URL: GET http://lara-passport-api.local/api/user
    Accept        application/json
    Authorization Bearer ACCESS_TOKEN
