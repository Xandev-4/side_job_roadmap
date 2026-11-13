# Learning Order (read this first)

No timeline in here on purpose. You move to the next step when the **"Done when"** line is true, not when a date arrives.

**Goal:** a job at a product-based startup.
**Stack:** Python everywhere (DSA, backend, AI), FastAPI + PostgreSQL, Docker, deployed projects.

Priority labels used in every file:

- **Core**: needed to be useful. Do these first.
- **Next**: learn once Core feels okay, or when a project forces it.
- **Later**: know it exists. Don't touch it yet.

---

## The 5 rules

1. **Max 2-3 active topics at a time.** Never all seven.
2. **Finish a topic's Core rows before its Next rows**, unless a project forces one early. Then learn only that row.
3. **Learn by building.** After each stage you build something, and the Done-when line is about what you can do.
4. **Don't plan, pick the next row and go.** If you catch yourself reorganising this file, close it and open a code editor.
5. **Never skip the daily minimum.** On a bad day it's 1 DSA problem or 10 minutes of code. A tiny day keeps the habit alive.

---

## The order

| Step                          | Active topics                                | Do these rows                                                                                   | Build this                                                                                                            | Done when                                                                                                                     |
| ----------------------------- | -------------------------------------------- | ----------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **1. Foundations**            | Python + Git/Terminal                        | `01_python` Core, `05_devtools_devops` Git + Linux basics                                       | 3-4 small scripts (CLI to-do app saving to JSON, text file analyser, simple quiz) pushed to GitHub                    | You can write a function, a loop and a class from scratch without looking things up every line, and use Git without fear      |
| **2. Problem solving starts** | + DSA (runs in parallel from here on)        | `02_dsa` Foundations + Core patterns                                                            | Nothing to build, solve problems                                                                                      | You can solve easy array/string/hashmap problems without hints most of the time                                               |
| **3. Data**                   | Python + DSA + SQL                           | `03_sql_postgresql` Core, then PostgreSQL Core rows                                             | A small database for a made-up app (users, posts, comments) with 10+ queries including joins and group by             | You can design 3-4 related tables and answer questions about the data with SQL                                                |
| **4. Backend**                | Backend + DSA (+ Python Next as needed)      | `04_backend_fastapi` Core, `01_python` Next rows (OOP, typing, async, Pydantic) as they come up | **Project 1:** REST API (e.g. notes or expense tracker) with PostgreSQL, user signup/login with JWT, CRUD, validation | Your API runs locally, is documented via `/docs`, and you can explain every line in it                                        |
| **5. Ship it**                | Backend + DevOps + DSA                       | `05_devtools_devops` Docker, compose, deployment                                                | Deploy Project 1 live with a public URL, with a README                                                                | Anyone can open your link. `docker compose up` runs it on a fresh machine                                                     |
| **6. Real project**           | Backend + SQL Next + DSA                     | `04_backend_fastapi` Next, `03_sql_postgresql` Next                                             | **Project 2:** something with real users (even 10 friends): a tool for your college, a club, a small business         | You have users, you've fixed real bugs they found, and you've handled auth, pagination and errors                             |
| **7. AI layer**               | AI + Backend                                 | `06_ai_llm_engineering` Core, then Next (embeddings, vector search, RAG)                        | **Project 3:** a RAG app (chat over PDFs/docs) exposed as a FastAPI service, deployed                                 | You can explain how chunking, embeddings, retrieval and generation fit together, and your app answers from your own documents |
| **8. Automate and harden**    | DevOps + System Design (basics)              | `05_devtools_devops` CI/CD, basic cloud; `07_system_design` Core + Next                         | GitHub Actions pipeline for a project, one deploy on a cloud VM                                                       | A push runs your tests and deploys. You can draw and explain how your own project would scale                                 |
| **9. Interview mode**         | DSA Next + System Design practice + projects | `02_dsa` Next, `07_system_design` classic problems                                              | Mock interviews, your resume, a clean GitHub profile                                                                  | You can talk through your projects confidently and solve medium problems with some thinking time                              |
| **10. Later rows**            | Anything                                     | All **Later** rows                                                                              | Whatever interests you                                                                                                | You're comfortable with everything above                                                                                      |

### How the steps overlap

- **DSA** starts at step 2 and continues all the way. It's the daily habit.
- **Python Next rows** are picked up inside steps 4-6, not as a separate stage.
- **Job hunting doesn't wait for step 9.** Start cold-messaging founders and engineers and applying for internships once you have Project 1 deployed. Applications teach you what to study.

---

## Your daily rhythm (block-based, not clock-based)

| Block           | What                                                          | Notes                                                                                                |
| --------------- | ------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| **Build block** | Your current stage's main thing (project or backend learning) | The core of the day                                                                                  |
| **DSA block**   | 1-2 problems                                                  | Even a failed attempt counts if you then read the solution and re-solve it from scratch the next day |
| **Learn block** | Theory for the current stage (a doc page, a video)            | Always followed by trying it in code                                                                 |
| **Flex block**  | Finish things, review, or rest                                | Don't skip rest                                                                                      |

**Block rules:** one topic per block, 10-15 minute break between blocks, phone in another room, and at the end of every session write the _very next step_ so tomorrow's start is easy.

---

## When things go wrong

| Situation                                                       | What to do                                                                                              |
| --------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| Stuck on a bug for 45+ minutes                                  | Write down what you tried, ask AI to **explain**, not to fix. Then fix it yourself                      |
| A day or week missed                                            | Do the next block. Never "catch up"                                                                     |
| Feel the urge to start a new language or framework (Rust, etc.) | Add it to a "Later" list at the bottom of this file. Check it after step 8                              |
| Everything feels too much                                       | Open the step table, find your current step, do the first unchecked row in the topic file. Nothing else |
| Tutorial hell (watching but not building)                       | Rule: for every 20 minutes of watching, 40 minutes of typing your own code                              |
| AI writing all your code                                        | Use AI to explain, review and quiz you. Write the first draft yourself                                  |

---

## Resources (free, solid)

| Topic            | Where                                                            |
| ---------------- | ---------------------------------------------------------------- |
| Python           | The official Python tutorial, CS50P                              |
| DSA              | NeetCode roadmap (use the topic order, not the full 150 at once) |
| SQL / PostgreSQL | The official PostgreSQL tutorial, SQLBolt, pgexercises.com       |
| FastAPI          | The official FastAPI tutorial (very good)                        |
| Docker           | Docker's "Get Started" docs                                      |
| AI/LLM           | The docs of your LLM provider (Anthropic, OpenAI)                |
| System design    | The "System Design Primer" repo on GitHub                        |

---

## Parking lot (things you're curious about but not doing now)

- [ ] Rust
- [ ] ...
