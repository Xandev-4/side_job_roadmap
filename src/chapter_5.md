# 04. Backend (FastAPI)

Priority: **Core** = learn first, **Next** = after Core / when a project needs it, **Later** = just know it exists.

## A. How the web works

| Done | Concept                                                                        | Priority | What you should be able to do            |
| ---- | ------------------------------------------------------------------------------ | -------- | ---------------------------------------- |
| ☐    | Client-server model                                                            | Core     | Explain what happens when you open a URL |
| ☐    | HTTP request and response (headers, body, status)                              | Core     | Read a request in browser dev tools      |
| ☐    | HTTP methods (GET, POST, PUT, PATCH, DELETE)                                   | Core     | Pick the right one                       |
| ☐    | Status codes (2xx, 3xx, 4xx, 5xx, esp. 200, 201, 400, 401, 403, 404, 422, 500) | Core     | Return the right code                    |
| ☐    | URLs: path, query string, fragment                                             | Core     | Parse a URL                              |
| ☐    | JSON as the data format                                                        | Core     | Read and write JSON                      |
| ☐    | Cookies, sessions, headers                                                     | Next     | Know where each is used                  |
| ☐    | DNS, ports, HTTPS (basic idea)                                                 | Next     | Explain at a high level                  |
| ☐    | Using Postman / curl / HTTPie                                                  | Core     | Test APIs without a frontend             |

## B. REST API design

| Done | Concept                                        | Priority | What you should be able to do     |
| ---- | ---------------------------------------------- | -------- | --------------------------------- |
| ☐    | Resources and URL naming (`/users/{id}/posts`) | Core     | Design clean endpoints            |
| ☐    | CRUD mapped to HTTP methods                    | Core     | Build full CRUD                   |
| ☐    | Idempotency (GET, PUT, DELETE vs POST)         | Next     | Explain why it matters            |
| ☐    | Pagination, filtering, sorting                 | Next     | Add `?limit=&offset=` and filters |
| ☐    | API versioning (`/v1/`)                        | Next     | Know why                          |
| ☐    | Consistent error format                        | Core     | Return useful error messages      |
| ☐    | HATEOAS, GraphQL, gRPC (awareness)             | Later    | Know they exist                   |

## C. FastAPI core

| Done | Concept                                              | Priority | What you should be able to do   |
| ---- | ---------------------------------------------------- | -------- | ------------------------------- |
| ☐    | Install, `uvicorn`, first endpoint                   | Core     | Run a hello-world API           |
| ☐    | Path parameters and query parameters                 | Core     | Accept inputs in URLs           |
| ☐    | Request body with Pydantic models                    | Core     | Validate incoming JSON          |
| ☐    | Response models (`response_model`)                   | Core     | Control what you return         |
| ☐    | Status codes and `HTTPException`                     | Core     | Return errors properly          |
| ☐    | Auto docs (`/docs`, `/redoc`)                        | Core     | Use Swagger UI to test          |
| ☐    | Pydantic validation (types, constraints, validators) | Core     | Reject bad input                |
| ☐    | Headers, cookies, form data                          | Next     | Read them in endpoints          |
| ☐    | `APIRouter` (splitting routes across files)          | Core     | Organise a growing app          |
| ☐    | Dependency injection (`Depends`)                     | Next     | Reuse DB sessions and auth      |
| ☐    | `async def` vs `def` endpoints                       | Next     | Know which to use               |
| ☐    | Middleware                                           | Next     | Add logging or timing           |
| ☐    | CORS                                                 | Next     | Let a frontend call your API    |
| ☐    | Background tasks                                     | Next     | Send an email after responding  |
| ☐    | File uploads                                         | Next     | Accept an image or PDF          |
| ☐    | Lifespan events (startup/shutdown)                   | Next     | Set up resources                |
| ☐    | WebSockets                                           | Later    | Real-time features              |
| ☐    | Server-sent events, streaming responses              | Next     | Needed for streaming LLM output |

## D. Database integration

| Done | Concept                                  | Priority | What you should be able to do     |
| ---- | ---------------------------------------- | -------- | --------------------------------- |
| ☐    | Connect FastAPI to PostgreSQL            | Core     | Read and write real data          |
| ☐    | SQLAlchemy models and sessions           | Core     | Map tables to Python classes      |
| ☐    | Separate DB models from Pydantic schemas | Core     | Know why they differ              |
| ☐    | Session handling via dependency          | Core     | One session per request           |
| ☐    | Relationships and joins in the ORM       | Next     | Load related data                 |
| ☐    | Migrations with Alembic                  | Next     | Change schema safely              |
| ☐    | Transactions in the API layer            | Next     | Keep multi-step writes consistent |
| ☐    | Avoiding N+1 queries                     | Next     | Use eager loading                 |

## E. Authentication and authorization

| Done | Concept                                                    | Priority | What you should be able to do |
| ---- | ---------------------------------------------------------- | -------- | ----------------------------- |
| ☐    | Password hashing (bcrypt / argon2), never store plain text | Core     | Hash and verify               |
| ☐    | Authentication vs authorization                            | Core     | Explain the difference        |
| ☐    | JWT access tokens (structure, expiry, signing)             | Core     | Issue and verify tokens       |
| ☐    | Protecting routes (`Depends(get_current_user)`)            | Core     | Require login                 |
| ☐    | Refresh tokens                                             | Next     | Keep users logged in safely   |
| ☐    | Role-based access control (admin vs user)                  | Next     | Restrict endpoints            |
| ☐    | OAuth2 / social login                                      | Later    | Know the flow                 |
| ☐    | Session-based auth vs token-based                          | Next     | Know the trade-offs           |
| ☐    | Rate limiting on login                                     | Next     | Block brute force             |

## F. Project structure and config

| Done | Concept                                                  | Priority | What you should be able to do |
| ---- | -------------------------------------------------------- | -------- | ----------------------------- |
| ☐    | Environment variables and settings (`pydantic-settings`) | Core     | No secrets in code            |
| ☐    | `.env`, `.gitignore`                                     | Core     | Keep secrets out of Git       |
| ☐    | Folder layout (routers, models, schemas, services, core) | Core     | Structure beyond one file     |
| ☐    | Separation of concerns (routes vs business logic vs DB)  | Next     | Keep routes thin              |
| ☐    | Logging                                                  | Next     | Log requests and errors       |
| ☐    | Global exception handlers                                | Next     | One place for errors          |
| ☐    | Config per environment (dev/prod)                        | Next     | Switch settings easily        |

## G. Testing and quality

| Done | Concept                                                   | Priority | What you should be able to do |
| ---- | --------------------------------------------------------- | -------- | ----------------------------- |
| ☐    | Testing with `pytest` and `TestClient`                    | Next     | Test endpoints                |
| ☐    | Test database / fixtures                                  | Next     | Isolate tests                 |
| ☐    | Mocking external services                                 | Next     | Test without real API calls   |
| ☐    | Linting and formatting (`ruff`)                           | Next     | Keep code clean               |
| ☐    | Input sanitisation, common vulnerabilities (OWASP basics) | Next     | Avoid injection, XSS, etc.    |

## H. Performance and extras

| Done | Concept                                   | Priority | What you should be able to do    |
| ---- | ----------------------------------------- | -------- | -------------------------------- |
| ☐    | Caching with Redis                        | Next     | Cache a slow endpoint            |
| ☐    | Rate limiting                             | Next     | Protect your API                 |
| ☐    | Task queues (Celery / RQ / ARQ)           | Later    | Run heavy jobs in the background |
| ☐    | Pagination at scale (keyset)              | Later    | Know why offset breaks           |
| ☐    | Gunicorn / uvicorn workers                | Next     | Know how production runs         |
| ☐    | Profiling and slow-query analysis         | Later    | Find bottlenecks                 |
| ☐    | Email, payments, third-party integrations | Later    | Add when a project needs it      |
| ☐    | Other frameworks (Django, Flask)          | Later    | Know they exist                  |

## Projects

- [ ] **Project 1:** Notes / expense tracker API (CRUD, Postgres, JWT auth, validation, deployed)
- [ ] **Project 2:** Something real users use (college tool, club tool, small business tool)
- [ ] **Project 3:** The RAG service from `06_ai_llm_engineering.md`
