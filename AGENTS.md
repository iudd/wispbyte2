# AGENTS.md

Short guide for AI agents in this repo.

## Repo layout

- `server/` - Hono HTTP server + Socket.IO + SSE + Telegram bot
- `web/` - React PWA / Telegram Mini App

## Reference docs

- `README.md` (project overview)
- `server/README.md` (server setup)
- `web/README.md` (web app workflow)

## Shared rules

- TypeScript strict; no untyped code.
- Bun workspaces; run `bun` commands from repo root.
- Path alias `@/*` maps to `./src/*` per package.
- Prefer 4-space indentation.

## Common commands (repo root)

- `bun install` - Install dependencies
- `bun run dev` - Start development servers
- `bun run build` - Build for production
- `bun typecheck` - Type checking

## Key source dirs

- `server/src/web/` - HTTP routes
- `server/src/socket/` - Socket.IO handlers
- `server/src/telegram/` - Telegram bot
- `server/src/sse/` - Server-Sent Events
- `web/src/components/` - React components
- `web/src/hooks/` - React hooks
- `web/src/lib/` - Utilities
