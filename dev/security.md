# Security

### Concepts

**Encoding** is for maintaining data **usability** and can be reversed by employing the same algorithm that encoded the content, i.e. no key is used.

**Encryption** is for maintaining data **confidentiality** and requires the use of a key (kept secret) in order to return to plaintext.

Also there are two major terms that brings confusion in the world of security **Hashing and Obfuscation**

**Hashing** is for validating the integrity of content by detecting all modification thereof via obvious changes to the hash output.

**Obfuscation** is used to prevent people from understanding the meaning of something, and is often used with computer code to help prevent successful reverse engineering and/or theft of a product’s functionality.

### JWT

JSON web token

![header.payload.signature](../.gitbook/assets/image-1.png)

### OpenID connect

uses JWT and adds some other usefull endpoints

### oAuth2 - it authorizes user

![](<../.gitbook/assets/image (10).png>)

three roles:&#x20;

* USER
* API (authorization server, resource server)
* CLIENT (my app)

CLIENT sends token request to API, gets token, gives to USER, \
USER sends it to API (by another webView), API signs this token, \
USER sends signed token to CLIENT, CLIENT sends it to API, and receives Access Token, \
CLIENT uses this access token to communicate with API without bothering USER

#### Auth stage

#### Login stage

#### Access token request stage

it uses OpenId to autenticate USER
