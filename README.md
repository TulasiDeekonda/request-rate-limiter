# Request Rate Limiter

Middleware component for applying request rate limits to FastAPI services.

The limiter tracks request counts per client using Redis and blocks requests that exceed the configured threshold within a defined time window.

---

## Structure

```
limiter/
 ├── middleware.py
 ├── storage.py
 ├── config.py
 └── utils.py

examples/
 └── fastapi_app.py
```

---

## Integration

```python
from fastapi import FastAPI
from limiter.middleware import RateLimiter

app = FastAPI()
app.add_middleware(RateLimiter)
```

---

## Notes

* Request counters stored in Redis
* Limits and time window configurable
* Designed for integration with existing API services

---

## Stack

Python
FastAPI
Redis
