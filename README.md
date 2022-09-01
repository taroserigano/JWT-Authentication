# JWT-Authentication
Authentication using JWS Tokens that can run on multiple ports
Mini-micro-service authentication app 
![alt text](https://github.com/taroserigano/JWT-Authentication/blob/main/tokengenerated.jpg)

Create .env file for this application such as: 

ACCESS_TOKEN_SECRET=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1lIjoiSmltIiwiaWF0IjoxNjM2NDA3MDA4LCJleHAiOjE2MzY0MDc1MDh9.e0aOedcvfYB8CLqxuOm-peStkOF9w_YLvSFoMqIGoLE

REFRESH_TOKEN_SECRET=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1lIjoiSmltIiwiaWF0IjoxNjM2NDA2OTM4fQ.tIQ0VYOjlV7xc-S824m0xebEVOjszDcM_CoPV394DA8


AccessToken = has all the information needed for the registered user in order to pass authentications for requesting data over the internet. JWT lets you maneuver across different sites and ports with this token. 

How to generate AccessToken with RefreshToken
Just send the refreshToken over the /token by POST, it'll verfiy if it's correct refreshToken and then
generate a new AccessToken with ther ({name : user.name }) 
and res back this data. 

Why RefreshToken? 
This is important for security, JWT.signup can have expiration data, once expired,
use this refreshToken in order to generate a new one. 

Why JWT? 
JWT lets you have authentication system without for servers to store session ID (which has all the info for users' credential) 
to make sure you are the right user. JWT use signup and verify, and lets you access across different sites and ports using this technology
without having to store the session cookie data each time. 

How JWT Works: 
JWT contains :1. HEADER (encryption system), 2. payload data (like user.name) 3. secret key 
When the token gets generated, it has aall three componenets encoded. 




