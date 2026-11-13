# 07. System Design (Complete)

Priority: **Core** = learn first, **Next** = after Core, **Later** = just know it exists.

**Best time to learn this:** after you've built and deployed at least one backend, so the concepts connect to things you've seen. Study with a notebook: for each concept, write "what problem does this solve?"

## A. Fundamentals

| Done | Concept                                               | Priority | What it is                                      |
| ---- | ----------------------------------------------------- | -------- | ----------------------------------------------- |
| ☐    | Client-server model, request flow end to end          | Core     | What happens from typing a URL to seeing a page |
| ☐    | Latency vs throughput                                 | Core     | Speed of one request vs requests per second     |
| ☐    | Availability and reliability                          | Core     | Uptime, "nines", failing gracefully             |
| ☐    | Functional vs non-functional requirements             | Next     | What it does vs how well it must do it          |
| ☐    | Back-of-envelope estimation (QPS, storage, bandwidth) | Next     | Rough capacity maths                            |
| ☐    | Scalability, maintainability, trade-offs              | Core     | Nothing is free; every choice costs something   |
| ☐    | SLA / SLO / SLI                                       | Later    | Formal reliability targets                      |

## B. Networking

| Done | Concept                                      | Priority | What it is                         |
| ---- | -------------------------------------------- | -------- | ---------------------------------- |
| ☐    | HTTP / HTTPS, DNS, IP, ports                 | Core     | The basics of how machines talk    |
| ☐    | TCP vs UDP                                   | Next     | Reliable vs fast                   |
| ☐    | REST vs GraphQL vs gRPC                      | Next     | API styles and when each fits      |
| ☐    | WebSockets, long polling, server-sent events | Next     | Real-time communication            |
| ☐    | Proxy vs reverse proxy                       | Next     | Who sits between client and server |
| ☐    | CDN                                          | Next     | Serve content from edge locations  |
| ☐    | TLS handshake and certificates in detail     | Later    | How HTTPS actually works           |

## C. Storage and databases

| Done | Concept                                               | Priority | What it is                                      |
| ---- | ----------------------------------------------------- | -------- | ----------------------------------------------- |
| ☐    | SQL vs NoSQL trade-offs                               | Core     | Structure and joins vs flexibility and scale    |
| ☐    | Indexing                                              | Core     | Faster reads, slower writes                     |
| ☐    | Replication (leader-follower, multi-leader)           | Next     | Copies of data for reads and safety             |
| ☐    | Sharding / partitioning (range, hash, directory)      | Next     | Splitting data across machines                  |
| ☐    | Consistent hashing                                    | Next     | Add/remove nodes without reshuffling everything |
| ☐    | NoSQL types (key-value, document, wide-column, graph) | Next     | Which type fits which problem                   |
| ☐    | Object / blob storage (S3)                            | Next     | Where files, images and videos live             |
| ☐    | Search engines (Elasticsearch basics)                 | Later    | Full-text search at scale                       |
| ☐    | Time-series and analytics databases                   | Later    | Metrics and logs                                |
| ☐    | Data warehouses, OLTP vs OLAP                         | Later    | Transactions vs analytics                       |
| ☐    | DB internals (B-trees, LSM trees, WAL)                | Later    | How databases store data                        |

## D. Scaling and traffic

| Done | Concept                                                    | Priority | What it is                        |
| ---- | ---------------------------------------------------------- | -------- | --------------------------------- |
| ☐    | Vertical vs horizontal scaling                             | Core     | Bigger machine vs more machines   |
| ☐    | Load balancers (L4 vs L7, algorithms)                      | Core     | Spread traffic across servers     |
| ☐    | Stateless vs stateful services                             | Next     | Why stateless scales easily       |
| ☐    | Rate limiting (token bucket, leaky bucket, sliding window) | Next     | Protect the system                |
| ☐    | Autoscaling                                                | Next     | Add capacity on demand            |
| ☐    | API gateway                                                | Next     | One entry point for many services |
| ☐    | Service discovery                                          | Later    | How services find each other      |
| ☐    | Sticky sessions                                            | Later    | Pinning a user to a server        |

## E. Caching

| Done | Concept                                                                 | Priority | What it is                       |
| ---- | ----------------------------------------------------------------------- | -------- | -------------------------------- |
| ☐    | Why and where to cache (browser, CDN, app, DB)                          | Core     | Avoid repeating expensive work   |
| ☐    | Cache strategies (cache-aside, read-through, write-through, write-back) | Next     | When data enters the cache       |
| ☐    | Eviction policies (LRU, LFU, TTL)                                       | Next     | What to remove when full         |
| ☐    | Cache invalidation                                                      | Next     | Keeping cache correct            |
| ☐    | Cache stampede / thundering herd                                        | Later    | Many requests hit the DB at once |
| ☐    | Redis vs Memcached                                                      | Next     | Common caches                    |

## F. Async processing and messaging

| Done | Concept                                                 | Priority | What it is                        |
| ---- | ------------------------------------------------------- | -------- | --------------------------------- |
| ☐    | Message queues (why and when)                           | Next     | Decouple producers and consumers  |
| ☐    | Pub/sub vs point-to-point                               | Next     | One-to-many vs one-to-one         |
| ☐    | Kafka vs RabbitMQ vs SQS                                | Next     | How they differ                   |
| ☐    | Background jobs and workers                             | Next     | Do slow work off the request path |
| ☐    | Idempotency, retries, dead-letter queues                | Next     | Handle failures safely            |
| ☐    | Delivery guarantees (at-most / at-least / exactly once) | Later    | What you can promise              |
| ☐    | Event-driven architecture, event sourcing, CQRS         | Later    | Advanced patterns                 |
| ☐    | Backpressure                                            | Later    | When consumers can't keep up      |
| ☐    | Stream processing (Flink, Spark Streaming)              | Later    | Real-time data pipelines          |

## G. Reliability and fault tolerance

| Done | Concept                                        | Priority | What it is                                   |
| ---- | ---------------------------------------------- | -------- | -------------------------------------------- |
| ☐    | Single point of failure, redundancy            | Next     | Remove anything that can take you down alone |
| ☐    | Health checks and failover                     | Next     | Detect and replace broken parts              |
| ☐    | Timeouts, retries, exponential backoff, jitter | Next     | Handle flaky dependencies                    |
| ☐    | Graceful degradation                           | Next     | Partial service beats no service             |
| ☐    | Circuit breaker, bulkhead                      | Later    | Stop failures from spreading                 |
| ☐    | Backups, disaster recovery (RPO / RTO)         | Later    | Recover from big failures                    |
| ☐    | Multi-region deployment                        | Later    | Survive a region outage                      |
| ☐    | Chaos engineering                              | Later    | Break things on purpose                      |

## H. Distributed systems theory

| Done | Concept                                       | Priority | What it is                                     |
| ---- | --------------------------------------------- | -------- | ---------------------------------------------- |
| ☐    | ACID vs BASE                                  | Next     | Strict vs relaxed guarantees                   |
| ☐    | CAP theorem                                   | Later    | Consistency, availability, partition tolerance |
| ☐    | PACELC                                        | Later    | CAP's more complete cousin                     |
| ☐    | Consistency models (strong, eventual, causal) | Later    | What readers see after writes                  |
| ☐    | Distributed transactions (2PC, saga)          | Later    | Transactions across services                   |
| ☐    | Consensus (Paxos, Raft), leader election      | Later    | How nodes agree                                |
| ☐    | Clocks and ordering (logical, vector clocks)  | Later    | Time in distributed systems                    |
| ☐    | Quorum reads/writes                           | Later    | Reading and writing with replicas              |
| ☐    | Gossip protocols, bloom filters, HyperLogLog  | Later    | Handy probabilistic tools                      |

## I. Architecture patterns

| Done | Concept                                             | Priority | What it is                                              |
| ---- | --------------------------------------------------- | -------- | ------------------------------------------------------- |
| ☐    | Monolith vs microservices                           | Next     | Trade-offs, and why many startups start with a monolith |
| ☐    | Layered / clean architecture                        | Next     | Structuring a codebase                                  |
| ☐    | Service-to-service communication (sync vs async)    | Later    | How services talk                                       |
| ☐    | Serverless                                          | Later    | Functions instead of servers                            |
| ☐    | Domain-driven design                                | Later    | Modeling the business                                   |
| ☐    | Strangler pattern, migrations between architectures | Later    | Moving off a legacy system                              |
| ☐    | Multi-tenancy                                       | Later    | Many customers on one system                            |

## J. API design

| Done | Concept                                      | Priority | What it is                           |
| ---- | -------------------------------------------- | -------- | ------------------------------------ |
| ☐    | RESTful design, versioning, pagination       | Core     | Clean, predictable APIs              |
| ☐    | Idempotent endpoints and idempotency keys    | Next     | Safe retries (e.g. payments)         |
| ☐    | Authentication flows (sessions, JWT, OAuth)  | Next     | Who's calling                        |
| ☐    | API security (input validation, rate limits) | Next     | Protect endpoints                    |
| ☐    | Backward compatibility                       | Later    | Changing APIs without breaking users |

## K. Security and observability

| Done | Concept                                   | Priority | What it is                          |
| ---- | ----------------------------------------- | -------- | ----------------------------------- |
| ☐    | Common attacks (SQL injection, XSS, CSRF) | Next     | And how to prevent them             |
| ☐    | Encryption at rest and in transit         | Later    | Protect data                        |
| ☐    | Secrets management                        | Later    | Keep keys out of code               |
| ☐    | Logging, metrics, tracing                 | Later    | Know what's happening in production |
| ☐    | Alerting and dashboards                   | Later    | Get paged before users complain     |

## L. Classic design problems (practice in this order)

For each: clarify requirements → estimate scale → draw the high-level design → go deep on one or two parts → discuss trade-offs.

| Done | Problem                 | Priority | Concepts it exercises                        |
| ---- | ----------------------- | -------- | -------------------------------------------- |
| ☐    | URL shortener           | Next     | Hashing, DB choice, caching, read-heavy load |
| ☐    | Rate limiter            | Next     | Token bucket, Redis, distributed counters    |
| ☐    | Pastebin / file storage | Next     | Object storage, expiry                       |
| ☐    | Key-value store         | Later    | Replication, partitioning, consistency       |
| ☐    | Chat application        | Later    | WebSockets, message delivery, storage        |
| ☐    | Notification system     | Later    | Queues, fan-out, retries                     |
| ☐    | News feed / Twitter     | Later    | Fan-out on write vs read, caching            |
| ☐    | Search autocomplete     | Later    | Tries, ranking, caching                      |
| ☐    | YouTube / Netflix       | Later    | CDN, video processing, storage               |
| ☐    | Uber / ride sharing     | Later    | Geospatial indexing, matching                |
| ☐    | Google Drive / Dropbox  | Later    | Sync, chunking, versioning                   |
| ☐    | Web crawler             | Later    | Queues, dedup, politeness                    |
| ☐    | Payment system          | Later    | Idempotency, consistency, reconciliation     |

## How to study this

- [ ] Read one concept, then write 3 lines in your own words: what problem it solves, how, and what it costs
- [ ] Draw every design by hand before looking at someone else's
- [ ] Apply each concept to your own projects ("where would a cache help here?")
- [ ] Do a URL shortener design end to end, then a rate limiter, before anything bigger
