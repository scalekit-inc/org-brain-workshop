# Fix: staging deploy cache key

Cache key is now derived purely from the lockfile hash instead of including a timestamp, so the dependency cache actually hits.
