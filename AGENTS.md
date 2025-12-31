# AGENTS.md

Short guide for AI agents in this repo.

## Repo layout
- `server/` - Hono HTTP server + Socket.IO + SSE + Telegram Bot
- `web/` - React 19 frontend with Vite + Tailwind

## Reference docs
- `README.md` (project overview)
- `server/README.md` (server setup and architecture)
- `web/README.md` (web app behavior and dev workflow)

## Shared rules
- TypeScript strict; no untyped code.
- Bun workspaces; run `bun` commands from repo root.
- Path alias `@/*` maps to `./src/*` per package.
- Prefer 4-space indentation.

## Common commands (repo root)

- `bun install` - Install all dependencies
- `bun run dev` - Start dev servers (server + web)
- `bun run build` - Build all packages
- `bun typecheck` - Type check all packages

## Key source dirs
- `server/src/web/` - HTTP routes
- `server/src/telegram/` - Telegram bot
- `server/src/sse/` - Server-sent events
- `web/src/components/` - React components
- `web/src/routes/` - Page routes
- `web/src/hooks/` - React hooks
