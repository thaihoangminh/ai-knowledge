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
| **frontend-skill** | Frontend design guidelines for premium UIs with restrained composition and tasteful motion |
| **seo-audit** | Technical SEO audit — Core Web Vitals, meta tags, indexing, crawl errors, ranking issues |
| **web-design-guidelines** | UI review against Web Interface Guidelines — accessibility, design, and UX compliance |
| **web-perf** | Web performance analysis using Chrome DevTools — FCP, LCP, TBT, CLS, Speed Index |

### Developer Tooling

| Skill | Description |
|-------|-------------|
| **create-readme** | Generate well-structured README files for projects |
| **find-skills** | Discover and install new agent skills from the registry |
| **get-api-docs** | Fetch up-to-date documentation for third-party libraries and APIs |
| **gh-fix-ci** | Debug and fix failing GitHub PR checks running in GitHub Actions |
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

### Option 1 — Clone & Symlink (Recommended)

This approach keeps your local skills directory in sync with the repository via a symlink, so `git pull` always gives you the latest skills.

```bash
# 1. Clone the repository
cd ~/Projects
git clone https://github.com/thaihoangminh/ai-knowledge.git

# 2. Copy any existing skills into the repo first
cp -r ~/.agents/skills/* ~/Projects/ai-knowledge/skills/

# 3. Back up the original skills directory
mv ~/.agents/skills ~/.agents/skills_backup

# 4. Create a symlink: ~/.agents/skills → repo
ln -s ~/Projects/ai-knowledge/skills ~/.agents/skills

# 5. Verify the symlink
ls -la ~/.agents/skills
# skills -> /Users/<your_username>/Projects/ai-knowledge/skills
```

> [!TIP]
> After the symlink is in place, running `git pull` inside `~/Projects/ai-knowledge` is all you need to update your skills.

### Option 2 — npx skills CLI

Use the [`npx skills`](https://github.com/vercel-labs/skills) CLI to search, install, and remove skills without touching the file system manually:

```bash
# Search for skills
npx skills search <query>

# Install a skill
npx skills add <skill-name>

# List installed skills
npx skills list

# Remove a skill
npx skills remove <skill-name>
```

> [!NOTE]
> See the full CLI reference at [github.com/vercel-labs/skills](https://github.com/vercel-labs/skills).
