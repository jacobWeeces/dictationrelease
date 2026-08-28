# Laurelle — Release Channel

Public distribution point for the Laurelle dictation app.

This repository contains **no source code**. It holds only:

- signed build artifacts attached to each [Release](../../releases)
- `latest.json`, the update manifest the app polls on launch
- `SHA256SUMS.txt` for each release

Source lives in a private repository. This repo exists so the app's
auto-updater can fetch new versions over plain HTTPS without storing a
GitHub credential on an end user's machine.

## For users

Download the newest installer from the [Releases page](../../releases/latest).
The app updates itself after that — you should not need to come back here.

## Verifying a download

Every release lists a SHA-256 for each artifact in `SHA256SUMS.txt`.

```powershell
# Windows PowerShell
Get-FileHash .\Laurelle-Setup-x.y.z.exe -Algorithm SHA256
```

```bash
# macOS / Linux
shasum -a 256 Laurelle-x.y.z-macos.dmg
```

The value must match the corresponding line in `SHA256SUMS.txt`.
