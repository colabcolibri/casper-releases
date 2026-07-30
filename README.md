# Casper — public desktop releases

This repository hosts **distribution artifacts only** for the **Casper** desktop app (Windows and macOS). Source code lives in a private project repository; here we publish installers, the auto-update manifest (`latest.json`), and signed updater bundles when applicable.

**Portuguese:** [README.pt.md](README.pt.md)

## Download (recommended)

Use the **official** site links — they always point at the latest release, without browsing GitHub:

| Platform | Link |
| -------- | ------------------------------------------------ |
| Windows | https://casper.sergioluciano.com/download/windows |
| macOS | https://casper.sergioluciano.com/download/mac |

Website: https://casper.sergioluciano.com  
Browser demo: https://demo.casper.sergioluciano.com

## Releases in this repository

On the **[Releases](https://github.com/colabcolibri/casper-releases/releases)** tab, each `desktop-v*` tag (semver with prefix) includes:

- **Windows:** `Casper_*-setup.exe` (NSIS installer)
- **Windows (updater):** `latest.json`, `*.nsis.zip`, and matching `*.sig` when the updater is enabled
- **macOS:** `.dmg` on the same release when a Mac build is uploaded

### How builds land here

| Platform | Pipeline |
| -------- | -------- |
| Windows | GitHub Actions on the private code repo — push tag `desktop-v*` |
| macOS | Local signed build on a Mac → `pnpm publish:desktop:mac --upload` |

## Trial and license

- **7-day trial:** start from the app — enter your email on first launch (desktop sends the request to the license server).
- **Paid license:** after purchase on the website, you receive a **license code by email**. Enter it in the app activation screen.
- **Browser demo** at `demo.casper.sergioluciano.com` is read-only and does not require a desktop license.

## Support

For purchase or download questions, use the channels listed on the official website. This repository **does not** handle product issues — it only hosts release binaries.
