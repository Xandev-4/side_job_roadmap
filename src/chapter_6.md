# 05. DevTools and DevOps

Priority: **Core** = learn first, **Next** = after Core / when a project needs it, **Later** = just know it exists.

## A. Terminal and Linux

| Done | Concept                                                                  | Priority      | What you should be able to do     |
| ---- | ------------------------------------------------------------------------ | ------------- | --------------------------------- |
| ☐    | Navigating the filesystem (`cd`, `ls`, `pwd`, `mkdir`, `rm`, `cp`, `mv`) | Core          | Live in the terminal comfortably  |
| ☐    | Viewing files (`cat`, `less`, `head`, `tail`, `grep`)                    | Core          | Search logs                       |
| ☐    | Permissions (`chmod`, `chown`), users                                    | Next          | Fix "permission denied"           |
| ☐    | Environment variables, `PATH`                                            | Core          | Understand how commands are found |
| ☐    | Pipes and redirection (`                                                 | `, `>`, `>>`) | Next                              | Chain commands |
| ☐    | Processes (`ps`, `top`, `kill`)                                          | Next          | Find and stop a process           |
| ☐    | Package managers (`apt`)                                                 | Next          | Install software                  |
| ☐    | SSH (keys, connecting to a server)                                       | Next          | Log into a VM                     |
| ☐    | Shell scripting (bash basics)                                            | Next          | Automate small tasks              |
| ☐    | `curl`, `wget`                                                           | Next          | Call APIs from the terminal       |
| ☐    | `systemd`, cron                                                          | Later         | Run services and scheduled jobs   |
| ☐    | Networking tools (`netstat`, `ss`, `ping`, `dig`)                        | Later         | Debug connectivity                |

## B. Git and GitHub

| Done | Concept                                          | Priority | What you should be able to do  |
| ---- | ------------------------------------------------ | -------- | ------------------------------ |
| ☐    | `init`, `add`, `commit`, `status`, `log`, `diff` | Core     | Save work in clean commits     |
| ☐    | Good commit messages                             | Core     | Describe the _why_             |
| ☐    | `.gitignore`                                     | Core     | Never commit secrets or `venv` |
| ☐    | Branching (`branch`, `checkout/switch`, `merge`) | Core     | Work on features separately    |
| ☐    | Remotes (`clone`, `push`, `pull`, `fetch`)       | Core     | Sync with GitHub               |
| ☐    | Pull requests and code review                    | Core     | Open and review a PR           |
| ☐    | Resolving merge conflicts                        | Core     | Fix them without panic         |
| ☐    | `stash`, `reset`, `revert`, `restore`            | Next     | Undo mistakes safely           |
| ☐    | `rebase` (basics)                                | Next     | Keep history clean             |
| ☐    | Branching strategies (GitHub flow, trunk-based)  | Next     | Know how teams work            |
| ☐    | GitHub Issues, Projects, README, license         | Core     | Present a repo professionally  |
| ☐    | Git internals (objects, refs)                    | Later    | Know the idea                  |
| ☐    | Contributing to open source                      | Next     | Make one small PR              |

## C. Docker

| Done | Concept                                                   | Priority | What you should be able to do    |
| ---- | --------------------------------------------------------- | -------- | -------------------------------- |
| ☐    | What containers are, containers vs VMs                    | Next     | Explain in simple words          |
| ☐    | Images, containers, registries (Docker Hub)               | Next     | Pull and run an image            |
| ☐    | Core commands (`run`, `ps`, `logs`, `exec`, `stop`, `rm`) | Next     | Manage containers                |
| ☐    | Writing a `Dockerfile`                                    | Next     | Containerise your FastAPI app    |
| ☐    | Build context, `.dockerignore`, layer caching             | Next     | Make builds fast and small       |
| ☐    | Environment variables and secrets in containers           | Next     | Configure without rebuilding     |
| ☐    | Volumes and bind mounts                                   | Next     | Persist database data            |
| ☐    | Docker networks                                           | Next     | Containers talking to each other |
| ☐    | `docker compose` (app + Postgres + Redis)                 | Next     | One command to run everything    |
| ☐    | Multi-stage builds                                        | Later    | Smaller production images        |
| ☐    | Image security scanning                                   | Later    | Know it exists                   |

## D. Deployment

| Done | Concept                                             | Priority | What you should be able to do   |
| ---- | --------------------------------------------------- | -------- | ------------------------------- |
| ☐    | Dev vs staging vs production                        | Next     | Explain the differences         |
| ☐    | Deploy to a PaaS (Render, Railway, Fly.io)          | Next     | Get a public URL                |
| ☐    | Managed database (Neon, Supabase, Railway Postgres) | Next     | Connect your app to a hosted DB |
| ☐    | Environment variables in production                 | Next     | Set secrets safely              |
| ☐    | Custom domain and HTTPS                             | Later    | Point a domain at your app      |
| ☐    | Static frontend hosting (Vercel, Netlify)           | Later    | Deploy a simple UI              |
| ☐    | Health check endpoints                              | Next     | Let platforms monitor your app  |
| ☐    | Zero-downtime deploys, rollbacks                    | Later    | Know the idea                   |

## E. CI/CD

| Done | Concept                                           | Priority | What you should be able to do |
| ---- | ------------------------------------------------- | -------- | ----------------------------- |
| ☐    | What CI and CD mean                               | Next     | Explain the difference        |
| ☐    | GitHub Actions (workflows, jobs, steps, triggers) | Next     | Run tests on every push       |
| ☐    | Linting and tests in CI                           | Next     | Block bad code from merging   |
| ☐    | Building and pushing Docker images in CI          | Next     | Automate image builds         |
| ☐    | Auto-deploy on merge to main                      | Next     | Ship without manual steps     |
| ☐    | Secrets in CI                                     | Next     | Use GitHub Secrets            |
| ☐    | Caching, matrix builds                            | Later    | Speed up pipelines            |

## F. Cloud basics (pick AWS first)

| Done | Concept                                       | Priority | What you should be able to do       |
| ---- | --------------------------------------------- | -------- | ----------------------------------- |
| ☐    | Regions, availability zones                   | Next     | Explain why they exist              |
| ☐    | IAM (users, roles, policies, least privilege) | Next     | Never use root for daily work       |
| ☐    | EC2 (launch a VM, SSH in, run your app)       | Next     | Deploy manually once                |
| ☐    | S3 (object storage)                           | Next     | Store and serve files               |
| ☐    | RDS (managed Postgres)                        | Next     | Connect an app to it                |
| ☐    | VPC, subnets, security groups                 | Later    | Understand basic network layout     |
| ☐    | Load balancer, auto scaling                   | Later    | Know the idea                       |
| ☐    | Lambda / serverless                           | Later    | Know the idea                       |
| ☐    | Billing alerts and cost control               | Next     | Set one up **before** experimenting |
| ☐    | GCP / Azure equivalents                       | Later    | Know they exist                     |

## G. Web server and networking

| Done | Concept                          | Priority | What you should be able to do  |
| ---- | -------------------------------- | -------- | ------------------------------ |
| ☐    | Reverse proxy (Nginx basics)     | Later    | Put Nginx in front of your app |
| ☐    | TLS certificates (Let's Encrypt) | Later    | Get HTTPS                      |
| ☐    | DNS records (A, CNAME)           | Later    | Point a domain                 |
| ☐    | Load balancing basics            | Later    | Know the idea                  |

## H. Observability

| Done | Concept                                      | Priority | What you should be able to do     |
| ---- | -------------------------------------------- | -------- | --------------------------------- |
| ☐    | Application logging                          | Next     | Write useful logs                 |
| ☐    | Error tracking (Sentry)                      | Later    | Catch production errors           |
| ☐    | Metrics and dashboards (Prometheus, Grafana) | Later    | Know the idea                     |
| ☐    | Uptime monitoring                            | Later    | Get alerted when the site is down |

## I. Advanced infrastructure

| Done | Concept                                       | Priority | What you should be able to do |
| ---- | --------------------------------------------- | -------- | ----------------------------- |
| ☐    | Infrastructure as Code (Terraform)            | Later    | Know what it solves           |
| ☐    | Kubernetes (pods, deployments, services)      | Later    | Know what it solves           |
| ☐    | Helm, service mesh                            | Later    | Skip for now                  |
| ☐    | Ansible, configuration management             | Later    | Skip for now                  |
| ☐    | Secrets managers (Vault, AWS Secrets Manager) | Later    | Know they exist               |

## Projects

- [ ] Containerise Project 1 with Docker + compose
- [ ] Deploy it to Render / Railway with a managed DB
- [ ] Set up a GitHub Actions pipeline (lint, test, deploy)
- [ ] Launch an EC2 VM, run your app on it, then tear it down
