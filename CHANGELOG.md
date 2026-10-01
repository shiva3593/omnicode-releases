# Omnicode 0.1.0

Initial release for macOS and Linux on arm64 and x64. Linux requires glibc 2.38 or newer.

- Run `omnicode` from a project folder to open its persistent workspace and coding tab.
- Added workspaces and tabs survive reopening; the coding tab continues its previous session after restart.
- Edit settings and plugin presets in `~/.config/omnicode/`, and add your own plugins, commands and skills.
- Existing configuration edits persist across upgrades.

```sh
brew tap omnicode/tap https://github.com/shiva3593/homebrew-tap
brew install omnicode
cd your-project
omnicode
```

Connect your own provider account with `omnicode --direct auth login`. Homebrew installs the required dependencies; the release includes compiled executables, supporting runtime files and licenses.
