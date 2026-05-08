# auth-service

Issues JWTs and owns the users collection.

## Endpoints

| Method | Path        | Description                          |
|--------|-------------|--------------------------------------|
| POST   | /register   | Create a new user (default role=driver) |
| POST   | /login      | Verify credentials, return JWT       |
| GET    | /me         | Return the user behind a JWT         |
| GET    | /health     | Liveness check                       |

Swagger UI: <http://localhost:8001/docs>

## Run

```
cp .env.example .env
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8001
```
