# @stackweld/registry

[![Version](https://img.shields.io/badge/version-0.3.0-blue.svg)](https://github.com/mundowise/Stackweld/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

The technology registry for Stackweld. Contains 83 YAML technology definitions with JSON Schema validation, covering compatibility rules, dependencies, ports, and scaffold instructions.

This package is an internal dependency — you do not use it directly. Install `@stackweld/cli` instead.

## What it contains

83 technology definitions across 9 categories:

| Category | Count | Examples |
|----------|-------|---------|
| Runtime | 7 | Node.js, Python, Go, Rust, Bun, Deno, PHP |
| Frontend | 12 | Next.js, React, Vue, Nuxt, Svelte, SvelteKit, Astro, Angular |
| Backend | 12 | Express, FastAPI, Django, Gin, Hono, NestJS, Laravel |
| Database | 11 | PostgreSQL, MySQL, MongoDB, Redis, SQLite, Supabase |
| ORM | 6 | Prisma, Drizzle, SQLAlchemy, TypeORM, Django ORM, Mongoose |
| Auth | 4 | NextAuth, Clerk, Lucia, Supabase Auth |
| Styling | 6 | Tailwind CSS, shadcn/ui, Chakra UI, Material UI |
| Service | 10 | Nginx, Traefik, MinIO, Grafana, Prometheus, pgAdmin |
| DevOps | 15 | Docker, TypeScript, Vitest, Jest, Playwright, GitHub Actions |

Each definition specifies:
- `id`, `name`, `category`, `description`
- `dockerImage` and `port` (for services)
- `incompatibleWith` — technologies that cannot be combined
- `requires` — technologies that must be included if this one is selected
- `scaffoldCmd` — the official CLI command used to scaffold this technology

## Repository

[github.com/mundowise/Stackweld](https://github.com/mundowise/Stackweld)

## License

MIT
