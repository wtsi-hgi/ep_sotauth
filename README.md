ep_sotauth
==========

Etherpad Lite plugin to trust authentication passed in from X-Forwarded-User HTTP header. This is useful when running behind a reverse proxy (a "series of tubes") that handles authentication. Do not use this plugin unless you have protected the server so that it can only be accessed from the reverse proxy.

## Configuration

Configuration is optional, without configuration ep_sotauth uses the `x-forwarded-user` header as username and displayname.
To adjust the header name use the following configuration:

Add to settings.json:

    "users": {
      "sotauth": {
        "password": "changeme1",
        "is_admin": false,
        "usernameHeader": "x-auth-username",
        "displaynameHeader": "x-auth-name"
      }
    }


Users who are in the matches group have *admin* access to
etherpad-lite.
