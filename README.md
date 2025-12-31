# Wispbyte Template

A full-stack application template for deploying to Wispbyte platform.

## Features

- **Server**: Hono + Socket.IO + SSE + Telegram Bot
- **Web**: React 19 + Vite + Tailwind CSS + PWA
- **Runtime**: Bun workspaces

## Quick Start

```bash
# Install dependencies
bun install

# Development
bun run dev

# Build
bun run build
```

## Project Structure

```
wispbyte-template/
├── package.json           # Workspace config
├── tsconfig.base.json     # Shared TypeScript config
├── server/                # Backend server
│   ├── src/
│   │   ├── index.ts       # Entry point
│   │   ├── configuration.ts
│   │   ├── telegram/      # Telegram bot
│   │   ├── web/           # HTTP routes
│   │   ├── socket/        # Socket.IO
│   │   ├── sse/           # Server-Sent Events
│   │   └── utils/
│   └── package.json
└── web/                   # Frontend app
    ├── src/
    │   ├── main.tsx       # Entry point
    │   ├── App.tsx        # Root component
    │   ├── components/    # UI components
    │   ├── hooks/         # React hooks
    │   └── lib/           # Utilities
    ├── index.html
    └── package.json
```

## Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `WEBAPP_PORT` | `3006` | Server listening port |
| `CLI_API_TOKEN` | (auto-generated) | Access token for API |
| `TELEGRAM_BOT_TOKEN` | - | Telegram bot token (optional) |
| `WEBAPP_URL` | - | Public URL for Telegram Mini App |
| `ALLOWED_CHAT_IDS` | - | Comma-separated Telegram chat IDs |

## Development

### Server

```bash
cd server && bun run dev
```

### Web

```bash
cd web && bun run dev
```

## Build & Deploy

```bash
# Build all
bun run build

# Or build separately
bun run build:server
bun run build:web
```

## License

MIT
