# Owen Anderson portfolio

Static portfolio at https://owanden.github.io/ using GitHub Pages from the main branch.

Preview from this directory:

```sh
python -m http.server 8765 --bind 127.0.0.1
```

Open http://127.0.0.1:8765/. No build step or package installation is required. Project cards link to public source repositories and local demo instructions. The Incident Triage demo uses predetermined fixture responses, and the Office Hours Queue walkthrough uses simulated notifications. Dispatch also links to recorded measurements.

## Queue browser preview

`demos/office-hours-queue/` contains the static browser preview built from OH-Queue. It reuses the queue interface with synthetic state held in one tab and no backend, credential entry, real phone input or provider calls. It resets on reload; simulated role controls do not establish API authentication or durable/shared state. The project card also retains the real full-stack local walkthrough.

`source.json` records the source repository/commit, build command and SHA256 of each copied asset. To update, build the recorded source's browser-preview target, review the resulting HTML/CSS/JavaScript, replace the preview directory, normalize built HTML to LF line endings and regenerate that provenance file. No environment files, source maps or private workspace materials belong in this static artifact.
