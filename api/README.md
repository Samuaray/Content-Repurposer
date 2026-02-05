# API Service

FastAPI-based REST service for the Content Repurposer.

## Responsibilities

- Expose REST endpoints for submitting videos/podcasts for repurposing
- Manage job lifecycle (create, status, cancel, retrieve results)
- Authenticate and authorize API consumers
- Dispatch processing tasks to Celery workers
- Serve generated content back to clients
