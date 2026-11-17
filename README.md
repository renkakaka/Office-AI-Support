# Office AI Support

Windows desktop IT support companion (v0.2.0).

The current project bundle is available in [Office_AI_Support_v0.2.0_Windows_MVP.zip](./Office_AI_Support_v0.2.0_Windows_MVP.zip).

## What this version does

- Armenian-first desktop support UI.
- Offline routing for common Windows support requests.
- Allow-listed local diagnostics and limited remediation.
- Action console showing the diagnostic functions being run.
- Local incident reports.
- GitHub Releases updater support with SHA-256 verification.

## Important limitations

This is an early office pilot, not an unrestricted autonomous administrator. It does not execute arbitrary AI-generated PowerShell. The current build uses a controlled set of local functions; some fixes open Windows settings or require user confirmation.

## Build

Extract the ZIP on Windows 10/11, install Python 3.10+, run `first_start.bat`, then `build_windows.bat`.

## Releases

The workflow in `.github/workflows/release.yml` builds the Windows executable and publishes it with a SHA-256 checksum when a version tag such as `v0.2.0` is pushed.

## Security and privacy

Do not commit office ticket exports, employee information, API keys, local `config.json`, or report files. The repository is public. No license has been added; public visibility alone does not grant broad reuse rights.
