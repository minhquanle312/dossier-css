# dossier.css

A "case-file dossier" design system stylesheet for long-form HTML documents —
technical specs, architecture docs, decision records, review write-ups.
Fraunces serif display + Source Sans 3 body + IBM Plex Mono for data/labels,
sage-paper palette, stamp badges, ledger tables, case-file decision cards.
Both light and dark themes wired via CSS custom properties.

Originated from a Noodle Factory internal spec artifact (SW-7666 essay
activity). Paired with the `artifact-design` Claude Code skill.

## Usage

Load it from jsDelivr's GitHub CDN, pinned to a tag:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,600;9..144,700;9..144,900&family=Source+Sans+3:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/minhquanle312/dossier-css@v1.0.0/dossier.css">
```

Or `@latest` instead of a version tag to always track the newest release
(not recommended for production — pin a tag).

## Components

See the stylesheet's section comments for the full component list: masthead
+ index-strip navigation, cover/pillars hero, stamp badges (`accent` / `ok`
/ `warn` / `danger` / `ai` / `ink`), ledger tables, schema/code cards,
note-box callouts, diagram-frame (repo-map / state-chain / pipeline), case
cards for decisions and risk, sketch blocks for screen mockups, verification
walk lists, and chapter-flip footer nav for multi-page splits.

Not for use inside a Claude Artifact published via claude.ai — that sandbox's
CSP only allows external stylesheets from `fonts.googleapis.com`; inline this
file's contents into the artifact's own `<style>` tag instead.
