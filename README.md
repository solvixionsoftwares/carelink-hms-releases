# CareLink HMS desktop releases

This repository distributes Windows desktop installers and update manifests only. Application source code is maintained privately.

Download the installer EXE from the [latest release](https://github.com/solvixionsoftwares/carelink-hms-releases/releases/latest). Each release includes its SHA-256 checksum and updater manifest.

## In-app updates

Version 1.0.12 and later use this public update feed by default. For an existing 1.0.10 or 1.0.11 installation, create `C:/ProgramData/CareLinkHMS/update.json` containing:

```json
{
  "manifestUrl": "https://github.com/solvixionsoftwares/carelink-hms-releases/releases/latest/download/carelink-hms-update.json",
  "checkOnStartup": true
}
```

Restart CareLink HMS, then select **Updates & Version > Check for updates**. Save your work before choosing **Install now**. Windows administrator approval is required to replace the installed application files.

Installers exclude runtime uploads, environment configuration, and legacy operational database dumps. Existing database and ProgramData files are preserved by in-place updates.
