# Discord MCP Server

[![smithery badge](https://smithery.ai/badge/@xcloudx123456/discord-mcp)](https://smithery.ai/server/@xcloudx123456/discord-mcp)

Model Context Protocol (MCP) server for Discord API integration.

## Prerequisites

Before running the server, you need to set up your environment variables:

1. Copy the `.env.example` file to `.env`:
   ```bash
   cp .env.example .env
   ```

2. Edit the `.env` file and fill in your actual values:
   - `DISCORD_TOKEN`: Your Discord bot token (required)
   - `DISCORD_GUILD_ID`: Your Discord server ID (optional but recommended)

## Running with Docker

To run the server using Docker:

1. Build and start the containers:
   ```bash
   docker-compose up --build
   ```

2. The server will be available at `http://localhost:8080`

## Running locally

To run the server locally:

1. Install dependencies:
   ```bash
   npm install
   ```

2. Build the project:
   ```bash
   npm run build
   ```

3. Start the server:
   ```bash
   npm start
   ```

   Or for development with auto-reload:
   ```bash
   npm run dev
   ```

## Environment Variables

For HTTP transport, you can also set:
- `MCP_HTTP_PORT` or `PORT`: Port for HTTP server (default: 8080)

Other optional variables:
- `ENABLE_LOGGING`: Enable/disable logging (default: true)
- `LOG_LEVEL`: Logging level (default: INFO)
- `MAX_RETRIES`: Maximum number of retries for Discord API calls (default: 3)
- `RETRY_DELAY`: Delay between retries in milliseconds (default: 1000)
- `TIMEOUT`: Timeout for Discord API calls in milliseconds (default: 30000)
- `RATE_LIMIT_PROTECTION`: Enable/disable rate limit protection (default: true)
- `ALLOWED_ACTIONS`: Comma-separated list of allowed actions (optional)
- `DENIED_ACTIONS`: Comma-separated list of denied actions (optional)


## Installation

### Installing via Smithery

To install Discord MCP Server automatically via [Smithery](https://smithery.ai/server/@xcloudx123456/discord-mcp):

```bash
npx -y @smithery/cli install @xcloudx123456/discord-mcp
```
