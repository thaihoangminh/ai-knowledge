# AI Knowledge

*A curated collection of AI agent skills for modern web development workflows.*

## Overview

**AI Knowledge** is a repository of reusable agent skills designed to supercharge AI-assisted development. Each skill provides domain-specific expertise — from Cloudflare Workers deployment to PostgreSQL optimization — enabling AI coding assistants to deliver high-quality, best-practice code out of the box.

> [!TIP]
> Skills are standalone and composable. Install only the ones relevant to your stack.

## Skills

### Cloudflare & Edge

| Skill | Description |
|-------|-------------|
| **building-ai-agent-on-cloudflare** | Build AI agents using the Agents SDK with real-time WebSockets and tool integration |
| **building-mcp-server-on-cloudflare** | Build remote MCP servers on Cloudflare Workers with OAuth and production deployment |
| **cloudflare** | Comprehensive platform skill covering Workers, Pages, KV, D1, R2, AI, networking, and security |
| **durable-objects** | Stateful coordination patterns — chat rooms, multiplayer, booking, RPC, SQLite, WebSockets |
| **sandbox-sdk** | Sandboxed code execution for AI interpreters, CI/CD, and untrusted code environments |
| **workers-best-practices** | Production best practices for Cloudflare Workers — streaming, state, secrets, observability |
| **wrangler** | CLI guidance for deploying and managing Workers, KV, R2, D1, Vectorize, and more |

### Next.js & React

| Skill | Description |
|-------|-------------|
| **next-best-practices** | File conventions, RSC boundaries, data patterns, async APIs, metadata, error handling |
| **next-cache-components** | Next.js 16 cache components — PPR, `use cache`, `cacheLife`, `cacheTag`, `updateTag` |
| **next-upgrade** | Upgrade Next.js to the latest version following official migration guides and codemods |
| **vercel-react-best-practices** | React & Next.js performance optimization guidelines from Vercel Engineering |

### Database & Backend

| Skill | Description |
|-------|-------------|
| **postgresql-code-review** | Code review for PostgreSQL — anti-patterns, schema design, RLS, function optimization |
| **postgresql-optimization** | Advanced PostgreSQL features — JSONB, arrays, custom types, full-text search, window functions |
| **supabase-postgres-best-practices** | Postgres performance optimization and best practices from Supabase |

### Web Quality & Performance

| Skill | Description |
|-------|-------------|
| **seo-audit** | Technical SEO audit — Core Web Vitals, meta tags, indexing, crawl errors, ranking issues |
| **web-design-guidelines** | UI review against Web Interface Guidelines — accessibility, design, and UX compliance |
| **web-perf** | Web performance analysis using Chrome DevTools — FCP, LCP, TBT, CLS, Speed Index |

### Developer Tooling

| Skill | Description |
|-------|-------------|
| **create-readme** | Generate well-structured README files for projects |
| **find-skills** | Discover and install new agent skills from the registry |
| **get-api-docs** | Fetch up-to-date documentation for third-party libraries and APIs |
| **git-commit** | Conventional commit workflow — auto-detect type/scope from diff, generate semantic messages |
| **migrate-oxlint** | Migration guide from ESLint to Oxlint |
| **test-driven-development** | TDD workflow — write tests before implementation for features and bugfixes |
| **turborepo** | Turborepo monorepo guidance — task pipelines, caching, remote cache, CI optimization |

### Other

| Skill | Description |
|-------|-------------|
| **gws-drive** | Google Drive — manage files, folders, and shared drives |
| **system-design** | Design systems, services, and architectures — API design, data modeling, service boundaries |

## Skill Structure

Each skill follows a consistent directory layout:

```
skills/<skill-name>/
├── SKILL.md          # Main instructions (required)
├── scripts/          # Helper scripts and utilities
├── examples/         # Reference implementations
└── resources/        # Templates, assets, and additional files
```

The `SKILL.md` file contains YAML frontmatter (`name`, `description`) followed by detailed markdown instructions that AI agents follow when the skill is activated.

## Installation

Clone the repository and point your AI coding assistant's skill directory to the `skills/` folder:

```bash
git clone git@github.com:thaihoangminh/ai-knowledge.git
```

Then configure your agent to load skills from `ai-knowledge/skills/`.

## Adding a New Skill

1. Create a new directory under `skills/` with a descriptive name
2. Add a `SKILL.md` file with YAML frontmatter and detailed instructions
3. Optionally include `scripts/`, `examples/`, or `resources/` directories
4. Keep instructions specific, actionable, and biased towards official documentation

> [!IMPORTANT]
> Each skill should be self-contained and focused on a single domain or technology.
