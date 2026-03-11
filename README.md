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

Install
Run:
AtlasOpsPOS-Setup-0.1.0.exe
The installer adds Start Menu/Desktop shortcuts for AtlasOpsPOS.
Verify Integrity (Recommended)
Get-FileHash .\AtlasOpsPOS-Setup-0.1.0.exe -Algorithm SHA256
Expected SHA256:
85745AF9032159B39B4A80FC3F48B7533162F65EC22978CA7FC91CE627396D34
Notes
•This installer includes the runtime needed to launch the program.
•Subscription and access checks are enforced inside the program.
•For internal team machines, trust setup is required once per user profile.
