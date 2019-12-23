# security

JWT

OpenID connect

uses JWT and adds some other usefull endpoints

oAuth - it authorizes user

three roles: USER, API \(server\), CLIENT \(my app\)

CLIENT sends token request to API, get token, gives to USER, USER sends it to API \(by another webView\), API signs thi token, USER sends signed token to CLIENT, CLIENT sends it to API, and receives Access Token, then CLIENT uses this access token to communicate with API without bothering USER

it uses OpenId to autenticate USER

