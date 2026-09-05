# Fix: DB connection pool exhaustion

Increased pool size for peak (not average) load, and added request queueing with a timeout instead of immediate failure when the pool is momentarily full.
