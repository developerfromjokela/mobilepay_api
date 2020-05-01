## Authentication
Authentication is an essential part for security, and Mobile Pay has done quite good job at it.

### Authentication headers
Mobile Pay uses these headers for authentication with the API:

- __X-IBM-Client-Id__
- __X-IBM-Client-Secret__
- __X-Authorization__
- __Authorization__

Let's go deeply into each one.

X-IBM-Client-Id
---
This is like a API Key, but it consists of two parts, client ID and client secret, this one is the ID.

*Where you can get it*? Extract it from Mobile Pay app's resources (```intrepid_ibm_client_id_prod```), or copy this:
```f2fe38f2-0656-4320-ac53-db22a9630af2```

X-IBM-Client-Secret
---
This is like a API Key, but it consists of two parts, client ID and client secret, this one is the secret.

*Where you can get it*? Extract it from Mobile Pay app's resources (```intrepid_ibm_client_secret_prod```), or copy this:
```Q3aT3rD8bB8jB4iH6gY4nT3lF5vU4gY4kD5kU5uO1wF5eH7dB6```

X-Authorization and Authorization
---

I don't honestly know (yet) where does the value originate, I guess when you authenticate.

But we know the X-Authorization is an auth token, because of its structure:
```X-Authorization: MobilePayToken [AND HERE SHOULD BE THE AUTH TOKEN]```

I have no clue right now about the *Authorization*,
you get this error response, when it's invalid:
```

{
    "httpCode": "401",
    "httpMessage": "Unauthorized",
    "moreInformation": "JWT has no resource scopes"
}

```

More information will appear here, when I'll find out where it originates.
