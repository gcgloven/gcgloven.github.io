# Observatory — Gong Chen

A connected personal wiki for research interests, reading notes, and related ideas.

**Website:** [gcgloven.github.io](https://gcgloven.github.io/)

This is the public publishing repository. It contains only a prebuilt website archive and deployment instructions. The editable source, local Keystatic editor, drafts, and private working files remain in the separate private authoring project.

## Publishing

GitHub Pages must use **Settings → Pages → Build and deployment → Source: GitHub Actions**. The workflow extracts `orbital-public-output.zip`, uploads only the generated website, and deploys it. No personal access token or private-repository credentials are required.

To update the site:

1. Edit and preview the private authoring project.
2. Run `npm ci`, `npm test`, then `SITE_URL=https://gcgloven.github.io BASE_PATH=/ npm run build` with Node.js 22.12.0 or newer.
3. Review `dist/`. Keep drafts, the editor, and raw source out of the public output.
4. Create `orbital-public-output.zip` from **the contents inside `dist/`**, including `.nojekyll`. `index.html` must be at the ZIP root, not inside a `dist` folder. Preserve nested folders and bundled license files, including the Geist font license.
5. Replace the archive in this repository and commit to `main`. The deployment workflow runs automatically; it can also be started manually in **Actions**.

Do not edit the generated website directly. Rebuild it from the private authoring project. Never upload the source-project ZIP or its Git history to this public repository.

Illustrative writing, fictional Worldlines, and AI-generated conceptual imagery retain their labels on the website.
