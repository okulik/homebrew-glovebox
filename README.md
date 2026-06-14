# homebrew-glovebox

  A [Homebrew](https://brew.sh) tap for [**glovebox**](https://github.com/okulik/glovebox) -
  a Docker-based isolation harness for running AI coding agents on macOS.

  This repo holds only the formula (`Formula/glovebox.rb`). The source code,
  documentation, and issue tracker live in the main project repo:
  **https://github.com/okulik/glovebox**

  ## Install

  ```bash
  brew tap okulik/glovebox
  brew trust --formula okulik/glovebox/glovebox    # brew 5.x; see below
  brew install glovebox
  ```

  `brew tap okulik/glovebox` resolves to this repo automatically - Homebrew
  inserts the `homebrew-` prefix to find `okulik/homebrew-glovebox`. The
  `brew trust` step is Homebrew 5.x's opt-in for third-party taps; without it
  `brew install` runs but doesn't link the `gbx` binary onto your PATH.

  The CLI is `gbx`:

  ```bash
  gbx --help
  man gbx
  ```

  glovebox requires Docker or OrbStack to be running. See the
  [main README](https://github.com/okulik/glovebox#readme) for prerequisites
  and a quickstart.

  ## Track development (optional)

  To install the latest `main` instead of the tagged release:

  ```bash
  brew install --HEAD glovebox
  ```

  ## Upgrade

  ```bash
  brew update
  brew upgrade glovebox
  ```

  For a `--HEAD` install, force a refresh (the version string doesn't change,
  so a plain `brew upgrade` reports "already installed"):

  ```bash
  brew upgrade --fetch-HEAD glovebox
  # or, equivalently:
  brew reinstall --HEAD glovebox
  ```

  ## Uninstall

  ```bash
  brew uninstall glovebox
  brew untap okulik/glovebox
  ```

  ## Licence

  glovebox is licensed under [AGPL-3.0-or-later](https://github.com/okulik/glovebox/blob/main/LICENSE).
  © 2026 Orest Kulik.
