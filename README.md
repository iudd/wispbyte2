# Wispbyte Template

A full-stack template for deploying applications to the Wispbyte platform.

## Project Structure

```
wispbyte-template/
├── server/          # Backend - Hono + Bun + Socket.IO + Telegram Bot
├── web/             # Frontend - React 19 + Vite + Tailwind CSS
├── package.json     # Bun workspaces config
└── tsconfig.base.json
```

## Features

- **Server**: Hono HTTP framework, Socket.IO, SSE, optional Telegram Bot
- **Web**: React 19, Vite, Tailwind CSS, PWA support
- **TypeScript**: Full type safety across all packages
- **Bun**: Fast runtime and package manager

## Quick Start

### Prerequisites

- [Bun](https://bun.sh/) installed

### Development

```bash
# Install dependencies
bun install

# Start development servers (server + web)
bun run dev
```

### Build

```bash
# Build all packages
bun run build
```

### Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `WEBAPP_PORT` | `3006` | Server listening port |
| `CLI_API_TOKEN` | (auto-generated) | Access token for API |
| `TELEGRAM_BOT_TOKEN` | - | Telegram bot token (optional) |
| `WEBAPP_URL` | - | Public URL for the app |
| `ALLOWED_CHAT_IDS` | - | Comma-separated Telegram chat IDs |

## Development Guide

### Adding New Features

1. **Server API**: Add routes in `server/src/web/`
2. **Frontend Pages**: Add components in `web/src/routes/`
3. **Shared Types**: Define in respective `types/` directories

### Project Conventions

- TypeScript strict mode
- 4-space indentation
- Path alias `@/*` maps to `./src/*` per package

## Deployment

This template is designed for Wispbyte platform deployment. Use the provided Dockerfile in `server/` for containerization.

```bash
docker build -t my-app -f server/Dockerfile .
docker run -p 3006:3006 my-app
```

## License

MIT
