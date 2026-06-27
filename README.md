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

## Agent Entry Points

Before meaningful work, read:

1. [AGENTS.md](AGENTS.md)
2. `/Users/adamroberts/Projects/Workspace/docs/architecture-handbook.md`
3. `/Users/adamroberts/Projects/Operating-System/AGENTS.md`
4. The Brain project note at `Projects/calwizz-landing.md`

## Related Docs

- [docs/google-oauth-publishing-guide.md](docs/google-oauth-publishing-guide.md)
- [docs/calwizz-privacy-policy-update.md](docs/calwizz-privacy-policy-update.md)

## Notes

The local branch may lag remote. Check status and branch state before editing or pushing.

