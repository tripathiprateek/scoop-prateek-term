# Prateek-Term Scoop bucket

Terminal emulator and SSH/serial connection manager for Windows.
<https://github.com/tripathiprateek/prateek-term>

## Install

```powershell
scoop bucket add prateek-term https://github.com/tripathiprateek/scoop-prateek-term
scoop install prateek-term          # stable
scoop install prateek-term-rc       # release candidate
```

Upgrade with `scoop update prateek-term` (or `prateek-term-rc`).

## Why Scoop rather than the installer from the releases page

Prateek-Term is not code-signed. The NSIS installer therefore triggers a
"Windows protected your PC" SmartScreen warning. Scoop extracts a zip instead,
so no downloaded executable is launched and SmartScreen never appears.

Every release also publishes a `SHA256SUMS` file; the hashes in these manifests
come from it and Scoop verifies them on install.

## Both architectures

x64 and arm64 are built natively and selected automatically.

## Uninstall

```powershell
scoop uninstall prateek-term
```

Settings live in `%APPDATA%\Prateek-Term` and are deliberately kept. To remove
them too:

```powershell
Remove-Item -Recurse $env:APPDATA\Prateek-Term
```

---

Manifest versions and hashes are updated automatically by CI on each release.
