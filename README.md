ep_sotauth
==========

Etherpad Lite plugin to trust authentication passed in from X-Forwarded-User HTTP header. This is useful when running behind a reverse proxy (a "series of tubes") that handles authentication. Do not use this plugin unless you have protected the server so that it can only be accessed from the reverse proxy. 