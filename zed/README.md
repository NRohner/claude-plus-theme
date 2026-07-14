# Claude+ for Zed

A Claude inspired theme for the [Zed](https://zed.dev) editor. Ships **Claude+ Dark** and **Claude+ Light**.

![Claude+ Dark Theme Preview](../screenshots/claude-plus-dark.png)

## Install

**From the extension registry**

1. Open the command palette (`cmd-shift-p`) and run `zed: extensions`.
2. Search for **Claude+** and install it.
3. Run `theme selector: toggle` and pick **Claude+ Dark** or **Claude+ Light**.

**Manually (single theme file)**

Copy `themes/claude-plus.json` into `~/.config/zed/themes/`. Zed picks it up without a restart.

**As a dev extension**

Run `zed: install dev extension` from the command palette and select this `zed/` directory.

## Files

```
extension.toml            extension manifest
themes/claude-plus.json   both variants, Zed theme schema v0.2.0
```

## Publishing

Zed extensions live in the [zed-industries/extensions](https://github.com/zed-industries/extensions) repo, which expects `extension.toml` at the root of the submodule. Since this repo keeps the Zed theme in a subdirectory, the entry in `extensions.toml` needs a `path`:

```toml
[claude-plus]
submodule = "extensions/claude-plus"
version = "1.0.0"
path = "zed"
```

Bump `version` in both `extension.toml` and that entry when you publish an update.
