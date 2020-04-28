### Understand the basic

https://auth0.com/docs/getting-started/the-basics

### Setup an APP

https://auth0.com/docs/getting-started/set-up-app

### Setup an API

https://auth0.com/docs/getting-started/set-up-api

### Authorization(Roles and Permissions)

https://auth0.com/docs/authorization/guides/how-to

### Scope

https://auth0.com/docs/scopes/current

https://auth0.com/docs/scopes/current/oidc-scopes
openid, profile, email scope will be used by the application.

https://auth0.com/docs/protocols/oidc#how-it-works

### Scope VS Permssion

https://community.auth0.com/t/permissions-claim-or-scopes/30156/7

### Different Flow

https://auth0.com/docs/flows 
Auth0 use OpenID and oauth 2.0 to authenticate users

https://auth0.com/docs/flows/concepts/device-auth

https://auth0.com/blog/using-m2m-authorization/

### How does server side know how to verify the token?

https://auth0.com/docs/tokens/concepts/jwks

### What token claim may looks like?

https://jwt.io/introduction/

```
{
  "iss": "https://react-auth0-example.auth0.com/", // the issuer of the token
  "sub": "auth0|5e9f05cf07597a0cc7d0702f", // user open id
  "aud": [// the audience who accept this token
    "https://domain-api",
    "https://react-auth0-example.auth0.com/userinfo"
  ],
  "iat": 1588091697,// issue time
  "exp": 1588178097,// expired time
  "azp": "LTC3GfbLXT7LaeMWvV2DwIqFfpZ0P0rs", // the application client id
  "scope": "openid profile email",
  "permissions": [
    "read:messages"
  ]
}
```