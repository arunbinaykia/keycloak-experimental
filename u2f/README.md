NOTES
-----

* Requires HTTPS. U2F will fail otherwise
* Credentials are stored in-mem. Lost on KC restart
* Requires Theme Resource Provider SPI


TODO
----

* Use credential provider to store credentials

Usage
-----

1. Deploy to Keycloak:

    mvn clean install wildfly:deploy

2. Login to admin console and create authentication flow with U2F

3. Add `Configure U2F` required action to admin user

4. Logout

5. Login as admin and configure U2F when requested

6. Logout

7. Login again and you should now be requested to touch the U2F token to continue