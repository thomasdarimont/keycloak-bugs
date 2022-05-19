Authentication Execution Order not consistent with Authentication Flow definition
----

Keycloak Version: 18.0.0
Bug: https://github.com/keycloak/keycloak/issues/12102

# Steps to reproduce
- Start example environment via `docker-compose up`
- Browse to http://localhost:8080/auth/realms/acme-passwordless/account/ 
- Click sign-in
- Use username `tester` with password `test`
- In the account-console, click "Signing in"
- Click "Set up Security Key"
- Insert your WebAuthN compatible device (Yubico, etc.) & click register and 
- Logout from account-console
- - Click sign-in
- Use username `tester`
-> Bug: password form is shown instead of passwordless form.
