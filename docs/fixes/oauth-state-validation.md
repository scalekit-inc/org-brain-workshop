# Fix: OAuth callback state validation

Adds explicit validation of the `state` query param on the OAuth callback. A missing or mismatched state now returns 400 before any session is created, instead of silently falling through to a success path.
