# Auth security hardening batch

Three related fixes bundled as one hardening pass:
- Password reset now revokes all existing refresh tokens atomically.
- Session cookie Secure flag is unconditional across all environments.
- Request logger redacts Authorization/Cookie/*_token/*_secret/*_key fields.
