# Python Backend Deployment Scaffold

A small application-side companion to my Cloud & DevOps portfolio. Its purpose is to provide a simple workload that can be containerised, tested, deployed, logged, and operated in the AWS and Azure labs.

## Current scope

This repository is intentionally a **scaffold**, not a finished production API. It currently contains a minimal Python smoke test and legacy imported material. I do not present it as a feature-complete backend until the implementation and its CI evidence exist.

That boundary is deliberate: accurate documentation is more useful to a recruiter than a broad “production-ready” claim without corresponding code.

## Target shape

The next implementation phase will establish one clear application root:

```text
app/                 # API and configuration
tests/               # automated tests
Dockerfile           # reproducible container build
.github/workflows/   # lint, test, build and image checks
docs/                # runbook, architecture and deployment notes
.env.example         # non-secret configuration contract
```

## What the completed companion should demonstrate

- health and readiness endpoints for deployment checks
- structured logs that can be correlated in CloudWatch or Azure Monitor
- environment-driven configuration with no secrets committed to Git
- a small, tested REST API
- a reproducible Docker image
- GitHub Actions checks before deployment
- deployment notes that connect the application to ECS/Fargate or Azure Container Apps

## Engineering standard

The repository will be featured in the portfolio only after it includes:

1. Source code and dependency definitions.
2. Automated tests running in CI.
3. A Docker build that can be reproduced locally.
4. A deployment example with non-secret configuration.
5. Operational notes covering logs, health checks, rollback, and cleanup.

## Repository hygiene

The nested `cloud-consultant-2026/` material is retained as legacy imported content. New work should use the root-level structure above so that the current application boundary is unambiguous.

## Related portfolio

For the implemented cloud architecture case studies and interview-ready explanations, see [cloud-engineering-portfolio](https://github.com/titoiunit/cloud-engineering-portfolio).