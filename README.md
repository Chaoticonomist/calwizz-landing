# CalWizz Landing

CalWizz Landing is the static marketing and policy site for CalWizz.

The repo is mapped in Workspace as `calwizz_landing` and on GitHub as `Chaoticonomist/calwizz-landing`.

## Product

The landing site explains CalWizz calendar analytics and meeting insights for busy professionals.

It includes:

- marketing homepage
- privacy policy
- terms page
- comparison/alternative pages
- marketing drafts
- OAuth publishing guidance

## Architecture

This is a static HTML/CSS site.

Important files:

```text
index.html
privacy.html
terms.html
clockwise-alternative.html
CalWizz-logo.png
docs/
marketing/
```

## Development

For local inspection, serve the repo root:

```sh
python3 -m http.server 8000
```

Then open:

```text
http://127.0.0.1:8000/
```

## Agent Startup

This repository participates in the local Brain + Workspace + Operating-System + Software Factory ecosystem.

Before meaningful work, run:

```sh
/Users/adamroberts/Projects/Operating-System/conductor/agent-context.sh
```

For proposed ideas or tasks, run intake first:

```sh
/Users/adamroberts/Projects/Operating-System/conductor/idea-intake.sh --task "Describe the proposed work"
```

Before meaningful work, read:

1. [AGENTS.md](AGENTS.md)
2. [docs/assistant-startup.md](docs/assistant-startup.md)
3. `/Users/adamroberts/Projects/Workspace/docs/architecture-handbook.md`
4. `/Users/adamroberts/Projects/Operating-System/AGENTS.md`
5. The Brain project note at `Projects/calwizz-landing.md`

## Related Docs

- [docs/assistant-startup.md](docs/assistant-startup.md)
- [docs/google-oauth-publishing-guide.md](docs/google-oauth-publishing-guide.md)
- [docs/calwizz-privacy-policy-update.md](docs/calwizz-privacy-policy-update.md)

## Notes

The local branch may lag remote. Check status and branch state before editing or pushing.
