# AgentFlow AI

AgentFlow AI is a proposed multi-tenant business automation platform that combines managed business records, conversational AI, approved tool execution, human-in-the-loop controls, document-grounded retrieval, and auditable integrations.

Phase 1 defines the product and architecture only. No application code, database migration, deployment, or production integration has been implemented.

## Proposed architecture

- React, TypeScript, Vite, Tailwind CSS, TanStack Query, and React Router for the web application.
- FastAPI, Pydantic, SQLAlchemy, and Alembic for the API.
- LangGraph behind a provider-neutral LLM adapter for agent orchestration.
- PostgreSQL with pgvector for transactional and vector data.
- Celery with Redis for background work, rate limits, and ephemeral coordination.
- S3-compatible object storage for uploaded source files.
- Secure cookie sessions, Argon2id passwords, privileged-account TOTP, and OIDC-ready identity boundaries.
- Registered typed tools, immutable approval payloads, transactional outbox delivery, and tenant-scoped authorization.
- Docker Compose for local development and AWS as the proposed production target.

See [System Architecture](docs/architecture/SYSTEM_ARCHITECTURE.md), [Security Architecture](docs/architecture/SECURITY_ARCHITECTURE.md), and [Phase Status](docs/phases/PHASE_STATUS.md).

## Development workflow

The project is delivered in 12 owner-approved phases. Each phase must inspect the current state, publish a plan, implement only its approved scope, run applicable validation, update documentation, issue a validation report, and stop. Phase 2 must not begin until the owner explicitly approves it.

## Phase 1 document index

- Product scope: `docs/requirements/PRODUCT_REQUIREMENTS.md`
- Functional requirements: `docs/requirements/FUNCTIONAL_REQUIREMENTS.md`
- Nonfunctional requirements: `docs/requirements/NON_FUNCTIONAL_REQUIREMENTS.md`
- Traceability: `docs/requirements/TRACEABILITY_MATRIX.md`
- System, database, and security designs: `docs/architecture/`
- API contracts: `docs/api/API_CONTRACTS.md`
- Agent and RAG designs: `docs/ai/`
- Test strategy: `docs/testing/TEST_STRATEGY.md`
- Proposed deployment: `docs/deployment/DEPLOYMENT_GUIDE.md`
- Phase plan and status: `docs/phases/`
- Architecture decisions: `docs/decisions/`

## Current status

Phase 1 documentation is complete and design-only. All targets labeled **proposed** or **assumption** require implementation-time measurement or owner validation. External services have not been connected or verified.
