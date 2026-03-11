# AtlasOps POS (Windows)

AtlasOps POS is the desktop point-of-sale client for AtlasOps operations.

## Download

Get the latest release assets from GitHub Releases:

- `AtlasOpsPOS-Setup-0.1.0.exe`
- `AtlasOpsPOS-Setup-0.1.0.exe.sha256`
- `atlasops-codesign.cer`
- `trust-atlasops-codesign-cert.ps1`

## First-Time Trust Setup (Private Distribution)

Because this build is signed with an internal/private code-signing certificate, run this once before installing:

```powershell
powershell -ExecutionPolicy Bypass -File .\trust-atlasops-codesign-cert.ps1
