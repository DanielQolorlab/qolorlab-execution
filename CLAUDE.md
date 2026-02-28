# Qolorlab Execution Roadmap (single-file web app)

## What this repo is
A single-page app (index.html) that displays and edits the Qolorlab executive roadmap.
It supports optional Supabase persistence + auth.

## Key files
- index.html: the entire app (HTML/CSS/JS)
- config.local.js (git-ignored): local overrides for Supabase URL/key and BYPASS_AUTH

## Dev
Run locally:
- python3 -m http.server 8000
Open:
- http://localhost:8000

## Important behaviors
- BYPASS_AUTH=true skips the login gate, but Supabase remote sync requires auth (RLS) unless policies are changed.
- worldtimeapi fetch is disabled; app uses local fallback to compute ISO week.

## Change rules
- Keep it working as a single file (no build system).
- Prefer minimal diffs.
- Avoid introducing external dependencies.
- Keep auth / persistence logic safe and explicit.

## Typical tasks
- UI tweaks
- Small JS refactors
- Supabase integration improvements
