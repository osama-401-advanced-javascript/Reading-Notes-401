## Bearer Authorization

**Write the following steps in the correct order:**
_Register your application to get a client_id and client_secret_
_Ask the client if they want to sign in via a third party_
_Receive authorization code_
_Redirect to a third party authentication endpoint_
_Make a request to the access token endpoint_
_Make a request to a third-party API endpoint_
_Receive access token_

**What can you do with an authorization code?** _to exchange it for an access token. The code itself is obtained from the authorization server._
**What can you do with an access token?** _The access token represents the authorization of a specific application to access specific parts of a user’s data._
**What’s a benefit of using OAuth instead of your own basic authentication?** _OAuth doesn’t share password data but instead uses authorization tokens to prove an identity between consumers and service providers_

### terms

**Client ID :** _is public code identifier for apps_
**Client Secret:** _is a secret code used by the OAuth Client to Authenticate to the Authorization Server_
**Authentication Endpoint:** _where the authentication for the users is granted_
**Access Token Endpoint:** _used by an appliction to use/ acsses the token_
**API Endpoint:** _the point of entry in a communiction channel_
**Authorization Code** _is a temporary code that the client will exchange for an access token_
**Access Token** _an opaque string that identifies a user, app, or Page and can be used by the app to make graph API calls_

### JSON Web Tokens

_Adapted from [https://jwt.io/introduction/](https://jwt.io/introduction/)_

- JSON Web Token (JWT) is an open standard that defines a compact and self-contained way for securely transmitting information between parties (servers, clients, etc.) as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

- Although JWTs can be encrypted to also provide secrecy between parties, we will focus on signed tokens. Signed tokens can verify the integrity of the claims contained within them, while encrypted tokens hide those claims from other parties. When tokens are signed using public/private key pairs, the signature also certifies that only the party holding the private key is the one that signed it.

- NOTE: Signing a token does not secure its contents. They are viewable, so be careful of the information that you include in the JSON data. A properly signed token is verified. In other words, you can be assured it wasn't modified in any way during transport and you can be certain that the generator of the token was trusted (as they have the same hey that you do).

### When should you use JWTs?

- Authorization: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access the routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because if its small overhead and its ability to be easily used across different domains.

- Information Exchange: JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed - for example, using public/private key pairs - you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.
