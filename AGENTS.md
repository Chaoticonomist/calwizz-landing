# CalWizz Landing Agent Instructions

Read this file before meaningful work in this repository.

## Required Context

Before planning or implementing:

1. Read `/Users/adamroberts/Projects/Workspace/AGENTS.md`.
2. Read `/Users/adamroberts/Projects/Workspace/docs/architecture-handbook.md`.
3. Read `/Users/adamroberts/Projects/Operating-System/AGENTS.md`.
4. Read `README.md`.
5. Search Brain for relevant CalWizz context.

Primary Brain note:

```text
Projects/calwizz-landing.md
```

## Current Repo State

This repository may have active landing-page changes in progress. Before editing, inspect `git status` and avoid touching unrelated modified files.

At the time this onboarding file was added, active changes existed in:

- `index.html`
- `privacy.html`
- `clockwise-alternative.html`

The local branch was also behind `origin/main`. Do not pull, rebase, or merge unless the user explicitly asks.

## Project Boundaries

- This repo contains static marketing and policy pages.
- Chrome extension work belongs in `/Users/adamroberts/Projects/calwizz/calwizz-extension`.
- App/backend work belongs in `/Users/adamroberts/Projects/calwizz/time-insights-app`.
- Durable decisions and project context belong in Brain.
- Do not store source code in Brain.

## Verification

Choose focused verification based on the change:

- HTML/content changes: inspect affected pages in a browser or local static server.
- Privacy/OAuth changes: compare against Google OAuth publishing requirements.
- SEO/social changes: inspect meta tags and canonical URLs.
- Marketing copy changes: check visible page hierarchy and calls to action.

If browser verification or deployment context is unavailable, state that explicitly.

