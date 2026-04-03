# @stackweld/core

[![Version](https://img.shields.io/badge/version-0.3.1-blue.svg)](https://github.com/mundowise/Stackweld/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

The core engine for Stackweld. Handles stack persistence, compatibility rules, scaffolding orchestration, Docker lifecycle, and all analysis modules.

This package is an internal dependency — you do not use it directly. Install `@stackweld/cli` instead.

## What it contains

```
src/
  db/          SQLite persistence layer (better-sqlite3)
  docker/      Docker Compose generation and runtime manager
  engine/      All analysis and intelligence modules:
               compatibility, env-sync, detect, compose-preview,
               health, migration, diff, share, infra, lint,
               benchmark, cost, learn, plugin
  scaffold/    Scaffold orchestrator + tech installer
  types/       Shared TypeScript types
  index.ts     Public API surface
```

### Key exports

```typescript
import {
  StackEngine,         // Create, save, load, delete stacks (SQLite)
  RulesEngine,         // Validate technology combinations, resolve dependencies
  ScaffoldOrchestrator,// Run official CLI tools (create-next-app, django-admin...)
  TechInstaller,       // Install per-technology extras (Prisma, NextAuth, Vitest...)
  DockerManager,       // docker compose up/down/status/logs
  scoreCompatibility,  // Score two technologies (0-100)
  checkProjectHealth,  // Audit an existing project directory
  planMigration,       // Step-by-step migration plan between technologies
  estimateCost,        // Monthly hosting cost estimate across providers
  detectStack,         // Detect stack from existing project files
  generateInfra,       // Generate Dockerfile + nginx / CloudFormation / Terraform
} from '@stackweld/core';
```

## Requirements

- Node.js >= 22.0.0
- Docker + Docker Compose (for runtime operations)

## Repository

[github.com/mundowise/Stackweld](https://github.com/mundowise/Stackweld)

## License

MIT
