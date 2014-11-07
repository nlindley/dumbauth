# Dumb Auth

This is a really dumb module that allow you to hit a Drupal server to authenticate and retrieve a user.

## Usage

POST to `/dumbauth` with a payload containing the username and password. You must also set `X-DumbAuth-Token` to whatever is in your Dumb Auth settings.

```
curl --data 'username=myawesomeuser&password=supersecretpassword' --header 'X-DumbAuth-Token: b26f935e-bb38-484d-873b-67ae984dfdf8' http://example.com/dumbauth
```

This will return `false` if the user is not found or authenticated, and a JSON representation of the user if authentication succeeds.
