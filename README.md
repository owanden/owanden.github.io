# Owen Anderson portfolio

Public static output for https://owanden.github.io/ on GitHub Pages.

The design and content are maintained in the separate PortfolioWebsite source project. Its dependency-free generator builds the project index, detail pages, stylesheet, favicon and 404 page. Build and check there, then use its guarded `scripts/publish-pages.mjs` helper with this clean checkout as the target. Review and commit the generated diff here; avoid editing the same content in both repositories.

`generated-pages.json` records the source commit and SHA256 of the generated files. It excludes independently retained assets. The public output contains no generator source, private project code, imported conversations or planning documents.

Selected work: Dispatch, RustLB, Office Hours Queue and Incident Triage Agent. Each detail page explains an implementation decision, a failure boundary and the available verification. RustLB source remains private. Project descriptions distinguish local demonstrations and fixed fixtures from deployed services or model-quality results.

## Queue browser preview

`demos/office-hours-queue/` retains the separate OH-Queue browser preview. It uses synthetic in-tab state, simulated roles and no backend/provider calls. `source.json` pins its source commit, build command and asset hashes. Update it from the source browser-preview target after checking the built output; do not copy environment files, source maps or private workspace material.

## Incident browser preview

`demos/incident-triage/` contains the separate Incident Triage browser build. Its fixed fixture, shared request handler and memory adapter execute within the tab. No backend/model calls or persistent browser storage; reload resets sessions. Use synthetic details only. `source.json` records source/build provenance and exact generated hashes. Rebuild from the pinned project source; publish only the three static files and provenance.

## Preview

Serve this directory with a local static HTTP server, then inspect the home page, `/projects/rustlb/` and the existing queue preview. The generated portfolio pages require no browser JavaScript or package installation.
