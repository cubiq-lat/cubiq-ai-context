# AGENTS.md - Cubiq Base Guidelines

<!-- This is the base template. Copy into each project's AGENTS.md and customize. -->

## Company Context

Cubiq is a product-led software factory based in Uruguay, building digital products and a Backend-as-a-Service platform for LATAM startups. They are an AI-driven company, managed by humans: they create, operate, and scale digital businesses in LATAM.

- Institutional site: https://www.cubiq.lat
- API: https://api.cubiq.lat
- API docs: https://api.cubiq.lat/docs — JSON format: https://api.cubiq.lat/docs-json

## Agent Guidelines

1. **git pull first** - At the start of each session or before beginning a new implementation, run `git pull` to fetch the latest changes.
2. **Bump version BEFORE creating each commit** - If a `package.json` exists, bump the patch version by 1 (e.g. `0.7.80` → `0.7.81`) BEFORE creating the commit. This applies to ALL commits — code changes, documentation, refactoring, etc. NEVER create a commit without first bumping the version. If committing code changes separately from the version bump, ensure both commits are pushed together in a single push operation.
3. **Commit format** - Use commit messages starting with `"AGENT:"` prefix. Confirm what will be committed before committing.
4. **Never push automatically** - Always ask before pushing.
5. **Don't expose secrets** - Never commit `.env` files, credentials, API keys, or any secrets to the repository.
6. **Don't run Docker commands locally** - Running `docker compose up` or `docker compose build` locally will deploy to production (api.cubiq.lat). Only run Docker commands when explicitly instructed. Most of the time this should be done on the development server (100.69.199.77 via Tailscale). Running locally is a temporary fallback only when the development server is offline.
7. **Ask before destructive commands** - Confirm with the user before running commands like `docker compose down -v`, database truncations, or force pushes.
8. **Don't kill processes blindly** - Never kill processes by port number without first checking what is running on that port. The server runs multiple applications. Always use `lsof -i :PORT` or `netstat -tlnp | grep PORT` to identify the process first.
9. **Don't make assumptions** - Ask for clarification when requirements are unclear rather than guessing.
10. **Never install packages without confirmation** - Always ask before installing new dependencies.
11. **Verify with tests** - Run relevant tests when possible to verify solutions work correctly.
12. **Be concise** - Keep responses short and to the point.

**Never push automatically** — always ask first.

## General Behavior

- Be concise in responses
- Never install new packages without confirmation first
- Never make assumptions — ask for clarification when requirements are unclear
- Ask before any destructive command (database truncations, force pushes, `down -v`, etc.)
- Never kill processes by port number without first identifying what is running on that port — use `lsof -i :PORT` or `netstat -tlnp | grep PORT` first
