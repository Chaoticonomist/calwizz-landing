# CalWizz Landing Agent Instructions

Read this file before meaningful work in this repository.

## Required Startup

Run the shared Operating-System startup packet from this repository:

```sh
/Users/adamroberts/Projects/Operating-System/conductor/agent-context.sh
```

If a human or AI partner proposes an idea or task, route it through intake before planning or building:

```sh
/Users/adamroberts/Projects/Operating-System/conductor/idea-intake.sh --task "Describe the idea"
```

Before planning or implementing:

1. Read this file.
2. Read `/Users/adamroberts/Projects/Operating-System/AGENTS.md`.
3. Read `/Users/adamroberts/Projects/Workspace/AGENTS.md`.
4. Read `/Users/adamroberts/Projects/Workspace/docs/architecture-handbook.md`.
5. Read `/Users/adamroberts/Projects/Workspace/workspace.yml`.
6. Read `README.md`.
7. Search Brain for relevant CalWizz context using the Brain path from Workspace.
8. Summarize relevant Brain context, or state explicitly that none exists.
9. Inspect repository status and surface unrelated dirty work.
10. Continue through the stepwise workflow.

Primary Brain note:

```text
Projects/calwizz-landing.md
```

## Default Workflow

Project work starts at `context`:

```sh
/Users/adamroberts/Projects/Operating-System/conductor/workflow-step.sh show context
```

Standard stage order:

```text
context
scope
plan
approve
build
verify
review
fix
commit
push
brain
handoff
```

## Approval Rule

A proposed idea is intake, not approval to build.

Get explicit approval before implementation when the work affects behavior, architecture, data, permissions, dependencies, deployment, workflow policy, or user-visible output.

Only group stages or skip gates when the user explicitly names the repo/layer and the stage range or skipped gate.

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
- Workspace owns local paths, repo aliases, GitHub slugs, and Brain project-note mappings.
- Operating-System owns workflow policy and conductor behavior.
- Software Factory owns reusable templates and shared assets.
- Durable decisions and project context belong in Brain.
- Do not store source code in Brain.

## Verification

Choose focused verification based on the change:

- HTML/content changes: inspect affected pages in a browser or local static server.
- Privacy/OAuth changes: compare against Google OAuth publishing requirements.
- SEO/social changes: inspect meta tags and canonical URLs.
- Marketing copy changes: check visible page hierarchy and calls to action.

If browser verification or deployment context is unavailable, state that explicitly.

Do not skip verification silently. Do not claim success when critical checks were not run.
