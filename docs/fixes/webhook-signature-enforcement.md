# Fix: webhook signature enforcement

Signature verification is now mandatory in every environment except explicit local dev - closes the staging exception that allowed unsigned payloads through.
