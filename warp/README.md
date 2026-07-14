# Claude+ for Warp

A Claude inspired theme for the [Warp](https://www.warp.dev) terminal. Ships **Claude+ Dark** and **Claude+ Light**.

## Install

Copy both files into Warp's theme directory:

```sh
mkdir -p ~/.warp/themes
cp claude_plus_*.yaml ~/.warp/themes/
```

Then open Warp's command palette (`cmd-p`) → **Open Theme Picker** (or Settings → Appearance → Themes) and pick **Claude+ Dark** or **Claude+ Light**. No restart needed; Warp rescans the folder when the picker opens.

On Linux the directory is the same: `~/.warp/themes/`.

## Files

```
claude_plus_dark.yaml
claude_plus_light.yaml
```

## The schema

Warp themes are flat — no syntax highlighting surface, just the terminal itself:

- `accent` — selection, cursor, and UI highlights
- `background` / `foreground` — the terminal pane
- `details` — `darker` or `lighter`, tells Warp which way to render its own chrome
- `terminal_colors.normal` / `.bright` — the 16 ANSI colors

The ANSI colors are the same values the Zed and VS Code ports use for their integrated terminals, so a terminal in any of the three looks identical.

## Publishing

Warp's built-in theme list comes from [warpdotdev/themes](https://github.com/warpdotdev/themes). To submit, open a PR adding these YAML files under the appropriate `themes/` subdirectory along with a preview `.png`, per that repo's contributing guide.
