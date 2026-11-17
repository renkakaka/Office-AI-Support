# Office AI Support

Windows desktop IT support companion — early v0.2.0 pilot.

This public repository is being initialized for the Office AI Support project. The project source bundle still needs to be added before the Windows release workflow can build an installer executable.

## Planned/current project capabilities

- Armenian-first Windows desktop support UI.
- Offline routing for common Windows support requests.
- Allow-listed local diagnostics and limited remediation.
- Action console showing diagnostic functions being run.
- Local incident reports.
- GitHub Releases update discovery with SHA-256 verification.

## Important limitations

This is an early office pilot, not an unrestricted autonomous administrator. It does not execute arbitrary AI-generated PowerShell. The current build uses a controlled set of local functions; some fixes open Windows settings or require user confirmation.

## Source and build

The Windows source bundle is available from the project owner as `Office_AI_Support_v0.2.0_Windows_MVP.zip`. After adding its source files to this repository, install Python 3.10+ on Windows, run `first_start.bat`, then `build_windows.bat`.

## Releases

The workflow in `.github/workflows/release.yml` is prepared to build the Windows executable and publish it with a SHA-256 checksum when a version tag such as `v0.2.1` is pushed. It will not succeed until the source files and dependencies are committed.

## Security and privacy

Do not commit office ticket exports, employee information, API keys, local `config.json`, or report files. This repository is public. No license has been added; public visibility alone does not grant broad reuse rights.
