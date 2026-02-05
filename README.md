# Content Repurposer

AI-powered content repurposing pipeline that takes long-form video and podcast content and automatically generates platform-optimized outputs (blog posts, social media threads, newsletters, short-form clips, and more) using LangChain.

## Tech Stack

- **FastAPI** - REST API for job management and content delivery
- **LangChain** - LLM orchestration for content generation and transformation
- **Celery** - Distributed task queue for async media processing
- **PostgreSQL** - Primary data store for jobs, content, and metadata
- **Redis** - Message broker for Celery and caching layer
- **Docker** - Containerized deployment for all services

## Architecture Overview

The system is organized into three core services:

```
┌──────────────┐     ┌──────────────────┐     ┌──────────────┐
│   api/       │────▶│   workers/       │────▶│   shared/    │
│  FastAPI     │     │  Celery +        │     │  Models,     │
│  REST API    │     │  LangChain       │     │  Config,     │
│              │     │  Orchestration   │     │  Utilities   │
└──────────────┘     └──────────────────┘     └──────────────┘
```

- **api/** - FastAPI service exposing REST endpoints for submitting content, tracking jobs, and retrieving generated outputs.
- **workers/** - Celery workers that handle transcription, LangChain-based content generation, and media processing pipelines.
- **shared/** - Common utilities, database models, configuration, and schemas shared across services.

## Project Structure

```
content-repurposer/
├── api/                # FastAPI REST service
├── workers/            # Celery workers & LangChain pipelines
├── shared/             # Common models, config, utilities
├── tests/              # Test suite
├── scripts/            # Setup and utility scripts
├── docs/               # Documentation and architecture diagrams
├── requirements.txt    # Python dependencies
└── README.md
```

## Setup Instructions

<!-- TODO: Add setup instructions -->

_Setup instructions will be added once dependencies and Docker configuration are in place._
