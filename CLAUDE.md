# CLAUDE.md

Guidance for Claude Code (claude.ai/code) when working in this repository.

## What this repository is

`martinellibrs93/martinellibrs93` is a **GitHub profile repository** — the special
repo whose name matches its owner's username. GitHub renders `README.md` from this
repo's default branch at the top of https://github.com/martinellibrs93.

Repository description: *"Config files for my GitHub profile."*
Default branch: `main`. Topics: `config`, `github-config`.

## Current state: empty

**As of 2026-08-13 this repository contains no commits, no branches, and no files** —
locally or on the remote. There is no application code, no build system, no test
suite, no dependency manifest, and no CI configuration.

Do not describe this repo as having an architecture, a stack, or a development
workflow. It has none yet. If a future session finds files here, this document is
stale and should be rewritten against what actually exists.

## Working here

Because the repo is empty, most conventional guidance does not apply:

- **Build / test / lint:** none. There is nothing to run. Do not invent commands or
  suggest `npm test`-style workflows unless a manifest is actually added first.
- **Language / framework:** undetermined. Any choice is a greenfield decision that
  belongs to the user, not an inference from existing code.
- **Directory layout:** flat and empty. A profile repo normally needs only
  `README.md` at the root; add directories only when something genuinely requires them.

### If asked to build the profile README

The profile README is the repo's primary purpose. Relevant mechanics:

- The file must be named `README.md` and live at the **root of the default branch**
  (`main`). A README in a subdirectory or on a non-default branch will not render on
  the profile.
- GitHub renders it with GitHub Flavored Markdown. Inline HTML is permitted but
  sanitized — no `<script>`, no `<style>`, no event handlers, no forms.
- Images and badges must be publicly reachable URLs. Relative paths resolve against
  this repo, so committed assets (e.g. `assets/banner.png`) work.
- Emoji shortcodes, task lists, and tables render. Mermaid diagrams render inside
  fenced code blocks tagged `mermaid`.
- Content here is **public** regardless of what other repos are private. Do not
  commit anything that reveals private repository names, internal hostnames, tokens,
  or personal contact details the user has not explicitly asked to publish.

### If asked to add automation

Profile repos commonly use GitHub Actions to refresh README content on a schedule
(activity feeds, stats, now-playing widgets). If that is requested:

- Workflows go in `.github/workflows/`.
- A workflow that commits back to the repo needs `permissions: contents: write`.
- Pin third-party actions to a commit SHA rather than a floating tag.
- Never place secrets in the README or workflow files; use repository secrets and
  reference them via `${{ secrets.NAME }}`.

## Git conventions

- The default branch is `main`, but it does **not exist yet** — the first push
  creates it. Confirm with the user before pushing directly to `main`; otherwise
  work on a feature branch and let them open a PR.
- Push with `git push -u origin <branch-name>`.
- Do not create pull requests unless explicitly asked.

## Related repositories

The account also owns `martinellibrs93/nest-reef-` (private, JavaScript, created
2026-08-13). It is **not** in scope for this session and must not be read from or
written to without being added explicitly. If a request seems to describe an actual
codebase with real structure and workflows, it likely targets that repo rather than
this one — ask before assuming.

## Maintaining this file

This document describes an empty repository. The moment real content lands, replace
these sections with the actual structure, commands, and conventions — verified by
reading the files, not inferred.
