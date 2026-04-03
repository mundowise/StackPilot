# @stackweld/templates

[![Version](https://img.shields.io/badge/version-0.4.0-blue.svg)](https://github.com/mundowise/Stackweld/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Built-in stack templates for Stackweld. 20 curated, ready-to-use project templates that you can scaffold with a single command.

This package is an internal dependency — you do not use it directly. Install `@stackweld/cli` instead.

## Available templates

| Template | Description |
|----------|-------------|
| `t3-stack` | T3 Stack (Next.js + tRPC + Prisma + Tailwind) |
| `django-rest` | Django REST API with PostgreSQL |
| `fastapi-react` | FastAPI backend + React frontend |
| `go-microservice` | Go microservice with Gin |
| `astro-landing` | Astro landing page |
| `sveltekit-fullstack` | SvelteKit full-stack app |
| `nuxt3-app` | Nuxt 3 application |
| `express-api` | Express REST API |
| `hono-microservice` | Hono microservice |
| `django-react` | Django + React full-stack |
| `mern-stack` | MERN stack (MongoDB + Express + React + Node) |
| `saas-starter` | SaaS starter with auth, billing, and admin |
| `nestjs-api` | NestJS API with TypeORM and PostgreSQL |
| `remix-fullstack` | Remix full-stack application |
| `solidstart-app` | SolidStart application |
| `laravel-app` | Laravel application with MySQL |
| `python-ai-lab` | Python AI/ML workspace with Jupyter |
| `tauri-desktop` | Tauri 2 desktop application |
| `monorepo-starter` | Turborepo monorepo with shared packages |
| `htmx-django` | HTMX + Django (zero JS framework) |

## Usage

```bash
# List all templates
stackweld template list

# Scaffold from a template
stackweld create t3-stack --path /home/user/projects

# Save your own stack as a template
stackweld template save my-stack-id

# Use a custom saved template
stackweld template use-custom my-template
```

## Repository

[github.com/mundowise/Stackweld](https://github.com/mundowise/Stackweld)

## License

MIT
