# opencode config

Personal [opencode](https://opencode.ai) configuration: agents, commands, skills, plugins, and TUI settings.

## Install

Clone into opencode's config directory:

```bash
git clone <repo-url> ~/.config/opencode
cd ~/.config/opencode
npm install
```

`npm install` is required — the local plugin imports `@opencode-ai/plugin`.

Restart opencode, then verify the plugin and config loaded:

```bash
opencode --version
```

## Already have a config?

Back up the existing directory first, then clone:

```bash
mv ~/.config/opencode ~/.config/opencode.bak
git clone <repo-url> ~/.config/opencode
cd ~/.config/opencode
npm install
```

Merge `opencode.json` / `opencode.jsonc` and `cli.json` manually if you want to keep local settings.

## What's inside

| Path | Purpose |
| --- | --- |
| `opencode.json` | Registers the local caveman plugin |
| `opencode.jsonc` | Compaction settings |
| `cli.json` | TUI theme (`rosepine`), diff wrapping, sidebar, animations |
| `AGENTS.md` | Global instructions (caveman mode) |
| `agents/` | Custom subagents |
| `commands/` | Custom slash commands |
| `skills/` | Skills (caveman, design, document tooling) |
| `plugins/caveman/` | Caveman output plugin |

## Update

```bash
cd ~/.config/opencode
git pull
npm install
```

## Uninstall

```bash
rm -rf ~/.config/opencode
```
