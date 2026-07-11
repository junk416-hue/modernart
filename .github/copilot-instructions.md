# Modernart Copilot Instructions

## Project Shape
- This is a single-page static game.
- The main entry point is `index.html`.
- All shipped assets currently live at the repository root.
- There is no build step in the repo today.

## Editing Rules
- Prefer small, targeted edits over broad refactors.
- Keep the game working as a standalone static file unless the user asks to introduce tooling.
- Preserve the current canvas-based architecture and existing asset filenames unless there is a clear reason to change them.
- Avoid adding dependencies for changes that can be made in plain HTML, CSS, or vanilla JavaScript.

## Distribution Notes
- For itch.io, package the repo as a flat zip with `index.html` at the archive root.
- `modernart.zip` is the itch.io distribution file in this repo.
- Include only the files needed to run the game in the browser.
- Do not include local caches, editor settings, or generated Firebase artifacts in the distributable.

## Validation
- For UI or game behavior changes, verify by loading `index.html` in a browser or serving the folder statically.
- If packaging changes are made, confirm the zip still opens with `index.html` at the top level.

## Common Repo Details
- `firebase.json` is for hosting deployment, not the itch.io package.
- `modernart.zip` should be regenerated whenever the distributable changes.