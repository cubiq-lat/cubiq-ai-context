# AGENTS.md - Cubiq Base Guidelines
<!-- This is the base template. Copy into each project's AGENTS.md and customize. -->

## Company Context

Cubiq is a product-led software factory based in Uruguay, building digital products and a Backend-as-a-Service platform for LATAM startups. They are an AI-driven company, managed by humans: they create, operate, and scale digital businesses in LATAM.

- Institutional site: https://www.cubiq.lat
- API: https://api.cubiq.lat
- API docs: https://api.cubiq.lat/docs — JSON format: https://api.cubiq.lat/docs-json

## Session Start

At the start of each session or before beginning a new implementation, run `git pull` to fetch the latest changes.

## Git Commits & Pushes

**Never commit** without explicit permission. When asked to commit:

1. **Bump version BEFORE creating each commit** — If a `package.json` exists, bump the patch version by 1 (e.g. `0.7.80` → `0.7.81`) before creating the commit. This applies to ALL commits — code changes, documentation, refactoring, etc. Never create a commit without first bumping the version. If committing code changes separately from the version bump, ensure both commits are pushed together in a single push operation.
2. **Commit format** — Use commit messages starting with the `"AGENT:"` prefix. Confirm what will be committed before committing.

**Never push automatically** — always ask first.

## General Behavior

- Be concise in responses
- Never install new packages without confirmation first
- Never make assumptions — ask for clarification when requirements are unclear
- Ask before any destructive command (database truncations, force pushes, `down -v`, etc.)
- Never kill processes by port number without first identifying what is running on that port — use `lsof -i :PORT` or `netstat -tlnp | grep PORT` first