# Cloudflare Gemini CLI Extension

This extension provides a suite of tools for interacting with Cloudflare services directly from the Gemini CLI. It includes 15 specialized MCP servers covering everything from documentation to resource management and observability.

## Authentication

All Cloudflare MCP servers in this extension use **Cloudflare OAuth 2.0** for authentication.

When you first use a tool from this extension, you will be prompted to authenticate. A browser window will open, allowing you to log in to your Cloudflare account and authorize the Gemini CLI to access the necessary resources. Once authorized, the CLI will securely store the access tokens for future use.

## Available Servers and Tools

The extension includes the following remote MCP servers:

- **Documentation (`cloudflare-docs`)**: Access the latest Cloudflare reference information.
- **Workers Bindings (`cloudflare-workers-bindings`)**: Manage KV, R2, D1, and other Workers primitives.
- **Observability (`cloudflare-observability`)**: Debug and gain insight into logs and analytics.
- **Radar (`cloudflare-radar`)**: Global Internet traffic insights and trends.
- **Browser Rendering (`cloudflare-browser-rendering`)**: Fetch web pages and take screenshots.
- **AI Gateway (`cloudflare-ai-gateway`)**: Manage AI logs and usage.
- **Workers Builds (`cloudflare-workers-builds`)**: Manage your Workers deployment pipeline.
- **DNS Analytics (`cloudflare-dns-analytics`)**: Optimize and debug DNS performance.
- **GraphQL (`cloudflare-graphql`)**: Query Cloudflare's GraphQL API for detailed analytics.
- **Audit Logs (`cloudflare-auditlogs`)**: Query and report on account activity.
- **Logpush (`cloudflare-logpush`)**: Monitor the health of Logpush jobs.
- **AutoRAG (`cloudflare-autorag`)**: Search documents on your AutoRAGs.
- **Sandbox Containers (`cloudflare-sandbox-containers`)**: Spin up sandboxed environments.
- **DEX Analysis (`cloudflare-dex-analysis`)**: Monitor Digital Experience metrics.
- **Cloudflare One CASB (`cloudflare-one-casb`)**: Identify security misconfigurations in SaaS apps.

## Usage Tips

- Use the `@` symbol to reference files in your project when using tools that can read context.
- Start with `cloudflare-docs` if you're unsure about how a Cloudflare feature works or how to write Workers code.
- Tools will automatically request confirmation before performing destructive actions (like deleting a KV namespace) unless you have marked the server as trusted.
