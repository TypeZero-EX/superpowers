# Sample landing page

A single-file, dependency-free landing page for Superpowers. It exists as a
sample/reference — it is not wired into the plugin, the hooks, or the test
suite, and nothing in the repository loads it.

- `index.html` — the whole page: markup, styles, and ~40 lines of JS for the
  copy buttons and the harness tabs. No build step, no framework, no bundler.
  Open it directly in a browser.

## Notes

- All copy is drawn from `README.md` in the repository root: the workflow
  steps, the skills library, the install commands, and the version in the
  header (`6.4.1`, from `.claude-plugin/plugin.json`).
- The session excerpt in the hero is illustrative, and labelled as such on the
  page. The prompt it shows — "Let's make a react todo list" — is the
  acceptance test for a real harness integration described in `AGENTS.md`.
- Fonts come from Google Fonts (Bricolage Grotesque, Public Sans, IBM Plex
  Mono) with system fallbacks, so the page still reads correctly offline.
- Light and dark themes are defined as CSS custom properties and follow
  `prefers-color-scheme`.
