# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A single static HTML page: the "Términos y condiciones" (terms and conditions) for a
promotional sweepstakes run by Industria Lojana de Especerías ILE C.A. ("Ají Criollo ILE").
The page is legal/marketing copy in Spanish, not an interactive application.

The repo currently contains only two files:

- `index.html` — the full terms-and-conditions content (title, intro paragraphs, a numbered
  `<ol>` of clauses, closing signature block).
- `style.css` — minimal styling (background gradient, heading colors/fonts, ordered-list
  marker and indent styling).

There is no build tooling, package manager config, test suite, or `src/` directory in this
repo despite its parent folder name (`threejs/TERMINOS`) — no Three.js code is present.

## Known inconsistencies to be aware of

- `index.html` contains `<script type="module" src="/src/main.ts"></script>` and a
  `<style src="style.css" type="text/css"></style>` tag (this second one is non-standard HTML
  and has no effect — the actual stylesheet is loaded correctly via the `<link rel="stylesheet">`
  in `<head>`). Neither `/src/main.ts` nor any `src/` directory exists. If asked to "fix" or
  build out the project, check with the user whether they intend to scaffold a real
  Vite/TypeScript project here or whether these are leftover/dead references that should be
  removed — don't assume either way.

## Working with this repo

- There is no build/lint/test command — it's a plain HTML/CSS file pair. Open `index.html`
  directly in a browser (or serve the directory with any static file server) to preview.
- When editing the legal text in `index.html`, preserve exact wording, dates, monetary/prize
  counts, and legal references — this is binding promotional legal copy for a real company
  (ILE C.A.) and precision matters. Don't paraphrase or "improve" the Spanish legal language
  unless explicitly asked to.
- Keep content in Spanish (the page's `lang="es"`) unless told otherwise.
