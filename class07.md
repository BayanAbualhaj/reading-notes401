# Reading-Notes 
## Bearer Authorization
![br](https://developer.atlassian.com/cloud/connect/images/connect-oauth-impersonation-flow.png)


### Write the following steps in the correct order:
- Register your application to get a client_id and client_secret
- Ask the client if they want to sign in via a third party
- Redirect to a third party authentication endpoint
- Make a request to the third-party API endpoint
- Receive authorization code
- Make a request to the access token endpoint
- Receive access token

### What can you do with an authorization code
1. Authorization codes are used for any transaction or entry that has restrictions on which users are entitled to access. 
2. Authorization codes are transmitted digitally and are used to accelerate credit card processing.
3. Although authorization codes may be permanently used over the length of an employee's tenure, they more often require routine refreshment.
4. authorization codes are integral control mechanisms that can be used to help combat employee fraud or the misappropriation of funds.
5. Authorization codes have also become commonly used in professional workplaces to maintain information security.


### [What can you do with an access token?](https://auth0.com/docs/tokens/access-tokens/use-access-tokens)
![token](https://i1.wp.com/css-tricks.com/wp-content/uploads/2020/03/oauth-client-credentials-flow.png?fit=1024%2C316&ssl=1)

* Access tokens are used in token-based authentication to allow an application to access an API. Once an application has received an access token, it will include that token as a credential when making API requests. 


### [What’s a benefit of using OAuth instead of your own basic authentication?](https://nordicapis.com/the-difference-between-http-auth-api-keys-and-oauth/)

* Multi-factor authentication can be used.
* Claims about the user can be delivered to the service directly through the request. No additional lookups required.
* specifies alternative flows for obtaining tokens in server-to-server environments.


### Vocabulary Terms?

* Client ID :is a public identifier for apps.

* Client Secret:is a secret used by the OAuth Client to Authenticate to the Authorization Server.

* Authentication Endpoint: s used to interact with the resource owner and get the authorization to access the protected resource. 

* Access Token endpoint: is used by the application in order to get an access token or a refresh token. It is used by all flows except for the Implicit Flow because in that case an access token is issued directly.

* An API endpoint :is a point at which an application program interface (API) -- the code that allows two software programs to communicate with each other -- connects with the software program.

* Authorization code: is a temporary code that the client will exchange for an access token. The code itself is obtained from the authorization server where the user gets a chance to see what the information the client is requesting, and approve or deny the request.

* An access token: is an object encapsulating the security identity of a process or thread. A token is used to make security decisions and to store tamper-proof information about some system entity.


### [What is JSON Web Token?](https://jwt.io/introduction/)

* JSON Web Token (JWT) is an open standard that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.

* JWTs can be encrypted to also provide secrecy between parties, we will focus on signed tokens.

* When tokens are signed using public/private key pairs, the signature also certifies that only the party holding the private key is the one that signed it.

**When should you use JSON Web Tokens?**

1. Authorization: This is the most common scenario for using JWT. 
2. nformation Exchange: JSON Web Tokens are a good way of securely transmitting information between parties.

**What is the JSON Web Token structure**
JSON Web Tokens consist of three parts separated by dots
    - Header
    - Payload:
         There are three types of claims: 
         1. registered
         2. public
         3. private claims.
    - Signature


**How do JSON Web Tokens work**

In authentication, when the user successfully logs in using their credentials, a JSON Web Token will be returned. Since tokens are credentials, great care must be taken to prevent security issues. In general, you should not keep tokens longer than required.


![faf](https://cdn2.auth0.com/docs/media/articles/api-auth/client-credentials-grant.png)


**Why should we use JSON Web Tokens**

1. less verbose 
2. Security-wise
3.  they map directly to objects. 
4.  is used at Internet scale.





