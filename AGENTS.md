# AGENTS.md

Codex guidance for this repo.

## What this repo is

Docker-only action client and Windows hotkey wrapper for sending JSON intent packets.

## Quick commands

- Setup: `Copy-Item .env.example .env`
- Run (stdin): `Get-Content .\docs\examples\example_intent.json | docker compose run --rm -T action-client run --stdin`
- Run (file): `docker compose run --rm action-client run --file docs/examples/example_intent.json`
- Tests: `docker compose run --rm test smoke`

## Safe to edit

- `docs/`
- `windows/`
- `client/src/` (if present)
- `README.md`

## Avoid or be careful

- `client/dist/` (generated)
- `docker-compose.yml` unless the change is required for new behavior

## Contracts

- JSON schemas live in `..\notion_assistant_contracts\schemas\v1\`.
- Examples live in `..\notion_assistant_contracts\examples\`.
