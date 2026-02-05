# Workers Service

Celery workers for async content processing and LangChain orchestration.

## Responsibilities

- Run async media processing tasks (transcription, audio extraction)
- Orchestrate LangChain pipelines for content generation
- Transform long-form content into platform-specific formats
- Handle retries, error recovery, and task state reporting
- Communicate results back to the API service via the shared database
