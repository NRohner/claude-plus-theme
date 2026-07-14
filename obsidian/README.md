# Claude+ for Obsidian

A Claude inspired theme for [Obsidian](https://obsidian.md). One file, both **Dark** and **Light** modes — Obsidian switches between them with the app's own appearance setting.

![Claude+ Dark Theme Preview](../screenshots/claude-plus-dark.png)

## Install

**From Community themes**

Settings → Appearance → Themes → **Manage** → search for **Claude+** → Use.

**Manually**

Copy `manifest.json` and `theme.css` into your vault at:

```
<vault>/.obsidian/themes/Claude+/
```

Then Settings → Appearance → Themes → select **Claude+**.

## Files

```
manifest.json   theme manifest (name, version, minAppVersion)
theme.css       both modes
```

## How it works

The theme sets Obsidian's own CSS variables rather than restyling components, so it stays compatible across Obsidian updates and plays well with plugins:

- `--color-base-00` … `--color-base-100` — the background-to-text ramp
- `--color-red` / `--color-green` / `--color-blue` / … — semantic colors
- `--accent-h` / `--accent-s` / `--accent-l` — the clay accent, as HSL parts
- `--code-*` — syntax token colors in code blocks and Source mode

`.theme-dark` and `.theme-light` each define a full set; the shared `body` block maps headings, links, quotes and graph nodes onto those colors.

## Publishing

Obsidian's community-theme installer pulls `manifest.json` and `theme.css` from the repo's **latest GitHub release**, so keeping them in this subfolder is fine — just attach both files as release assets. Bump `version` in `manifest.json`, tag the release with the same version (no `v` prefix), then submit a PR to [obsidianmd/obsidian-releases](https://github.com/obsidianmd/obsidian-releases) adding an entry to `community-css-themes.json`.
