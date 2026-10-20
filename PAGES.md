# Publish this MVP with GitHub Pages

This folder is the complete static site. Its contents belong at the root of a GitHub Pages branch, such as `gh-pages`; configure GitHub Pages to deploy that branch from `/(root)`.

Included files:

- `index.html` — presentation and browser-side Living Archive.
- `cvp-genesis.json` — unsigned namespace/descriptor linking the parts of the MVP.
- `cvp-dictionary.json` — valid JSON packaging of the supplied dictionary source and selected vector definitions.
- `cvp-ministry-trust-source.json` — valid JSON packaging of the trust-source text; gateway/API credentials are redacted.
- `cvp-mvp.json` — machine-readable MVP manifest.
- `documents/` — three PDFs and their CID/digest/vector catalog.
- `assets/` — supplied presentation image.

The original source files are left unchanged. Gateway/API credentials are redacted from the public trust-source JSON copy.

The descriptor and catalog are unsigned. The local archive can sign browser-created records, but this demo is not a globally ordered registry and does not establish identity, trusted time, patents, ownership, legal enforceability, or jurisdiction. A CID verifies content against a reference when the content is available; it does not guarantee continued availability.
