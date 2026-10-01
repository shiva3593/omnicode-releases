# Omnicode

Omnicode opens a persistent workspace for the folder you run it from, with a coding tab and separate tabs for Git, a terminal, and tests. Run it again from that folder to return to the same workspace. Detach with `Ctrl+B`, then `Q`.

## Install

Enable the Omnicode tap, then install:

```sh
brew tap omnicode/tap https://github.com/shiva3593/homebrew-tap
brew install omnicode
```

Supports macOS (Apple Silicon and Intel) and Linux (arm64 and x64, glibc 2.38 or newer). Homebrew installs the required dependencies. Update with `brew upgrade omnicode`.

## Use

```sh
cd your-project
omnicode
```

Sign in to a model provider with your own account:

```sh
omnicode --direct auth login
```

Run `omnicode --herdr --help` for workspace commands; for example, `omnicode --herdr workspace list` lists this folder's workspaces. Added workspaces and tabs survive reopening. The coding tab continues your previous session after a restart.

`--direct` passes commands through to the underlying CLI. For example, `omnicode --direct run "explain this project"` runs a prompt directly. See `omnicode --help` for launcher options; `omnicode --version` prints the installed version.

## Configuration

On first run, Omnicode creates editable defaults under `~/.config/omnicode/`. Run `omnicode --config` to seed the defaults and print that directory. Edit `opencode.jsonc` for models, agents, and defaults; use `tui.json` for the terminal interface and `plugins/preset-*.mjs` for bundled plugin presets. You can add your own plugins there as well. Your changes persist across upgrades.
