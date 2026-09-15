# dossier.css

A technical-reference design system stylesheet for long-form HTML documents —
specs, architecture docs, decision records, review write-ups. IBM Plex Mono
headings/labels + IBM Plex Sans body, sage-green paper, teal accent, generic
categorical badge hues, dark code blocks, mermaid-friendly diagram wrapper,
sticky sidebar table of contents. Both light and dark themes wired via CSS
custom properties.

Originated from a Noodle Factory internal artifact ("Quiz Schema Reference"),
generalized for reuse. Paired with the `artifact-design` Claude Code skill.

## Versions

- **v2.0.0** (current) — sidebar-nav technical reference style: IBM Plex Mono
  + IBM Plex Sans, sage/teal palette, mermaid diagram wrapper.
- **v1.0.0** — case-file dossier style: Fraunces serif + Source Sans 3 +
  IBM Plex Mono, sage-paper palette, stamp badges, ledger tables. Still
  available pinned to that tag if you have documents already built on it.

## Usage

Load it from jsDelivr's GitHub CDN, pinned to a tag:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500;600;700&family=IBM+Plex+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/minhquanle312/dossier-css@v2.0.0/dossier.css">
```

Or `@latest` instead of a version tag to always track the newest release
(not recommended for production — pin a tag).

## Components

See the stylesheet's section comments for the full component list: `.wrap`
sidebar-grid layout with sticky `nav.toc`, `header.masthead` hero (eyebrow +
title + deck + meta-strip), numbered `section` blocks with `.s-head`/`.s-num`,
`.callout` (plus `.callout.risk`), `.grid.cols-2`/`.cols-3` + `.card`,
`.badge` (`b-ok` / `b-gap` / `b-cat1` / `b-cat2` / `b-cat3` — rename the
categorical ones per subject), `.table-scroll` + sticky-header tables,
`pre.code` / `.code-block` for code, `.diagram-wrap` for Mermaid diagrams,
`.cite` for inline file:line references.

Mermaid diagrams (`<pre class="mermaid">...</pre>` inside `.diagram-wrap`)
render natively with no extra script when published as a Claude Artifact on
claude.ai. Outside claude.ai, load Mermaid yourself first — a pinned UMD
build from cdnjs, e.g.
`https://cdnjs.cloudflare.com/ajax/libs/mermaid/11.x.x/mermaid.min.js` —
then call `mermaid.initialize({ startOnLoad: true })`.

Not for use inside a Claude Artifact published via claude.ai — that sandbox's
CSP only allows external stylesheets from `fonts.googleapis.com`; inline this
file's contents into the artifact's own `<style>` tag instead.
