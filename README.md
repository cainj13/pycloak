# Pycloak
### A Simple Keycloak Admin API interface in Python

This Python package is for interacting with the Keycloak admin interface.  So far it only grabs access tokens for you like so:
```
import pycloak.admin
import pycloak.auth

session = pycloak.auth.AuthSession('admin', 'password')
admin = pycloak.admin.Admin(session)
admin.realms
admin.realm('master')
```

More to come soon!

### Hacking

Stand up a KC server locally:
```
docker run --rm -it -e KEYCLOAK_USER=admin -e KEYCLOAK_PASSWORD=password -p 8080:8080 jboss/keycloak
```
