# Commons Vector Protocol — GitHub Pages MVP

This folder is a self-contained static-site bundle for **Det Levende Arkivet**. It combines the working browser archive, the vector presentation, a valid machine-readable MVP manifest, selected dictionary definitions, a sanitized JSON envelope for the supplied trust-source text, and the supplied PDF documents.

## Publish with GitHub Pages

1. Put the **contents** of this folder at the root of a branch named `gh-pages` (including `index.html` and `assets/`).
2. Push the `gh-pages` branch to GitHub.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `gh-pages`, and select **/(root)**.
5. Save and wait for the Pages deployment to finish.

The site is static and needs no build step or server-side credentials. HTTPS Pages is a secure context for supported Web Crypto operations.

## Files

- `index.html` — the presentation and functioning browser-side archive.
- `assets/commons-vector-presentation.png` — supplied presentation artwork.
- `cvp-mvp.json` — valid JSON manifest for the MVP and its vector coordinates.
- `cvp-genesis.json` — unsigned descriptor linking the namespace, dictionary, vectors, trust-source reference, and archive.
- `cvp-dictionary.json` — sanitized JSON envelope of the source dictionary plus selected vector/provenance definitions.
- `cvp-ministry-trust-source.json` — trust-source text in a valid JSON envelope with access credentials redacted. The original source remains unchanged.
- `cvp-mvp-source.md` — supplied MVP presentation text, preserved as source.
- `documents/` — the two attached PDFs, the project deliverables PDF, and their CVP document catalog.

The document catalog follows the dictionary's tri-vector vocabulary (content CID, spatial vector, and rule vector) and composite-key formula. The catalog makes SHA-512 CIDs from the supplied PDF bytes. Its entries are unsigned references, not signed archive instruments, legal conclusions, or proof that the PDFs have been pinned to IPFS. A CID can verify that retrieved bytes match a reference; it does not by itself establish authorship, patent rights, ownership, or legal status.

The HTML app stores records in browser storage and keeps its non-extractable Ed25519 key in IndexedDB. A different browser profile or cleared site data will not have that local key. Export archives for portability and retain the original browser profile if you need to continue signing with the same identity.

The app does not upload to Pinata. Its optional local Kubo upload sends payload bytes only to the loopback API that the user configures after clicking the upload button. The app does not place gateway credentials or API secrets in the site code.
