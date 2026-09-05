# Fix: tenant redirect after logout

Logout now clears the tenant-hint cookie alongside the session cookie, fixing SSO logins landing users back in a previous tenant.
