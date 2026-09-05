# Fix: webhook idempotency

Webhook handler now checks a processed-events table keyed by event ID before applying any charge, making retried deliveries a no-op.
