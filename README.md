# Office AI Support

Windows desktop IT support companion — v0.3.0 office pilot.

## What this version adds

- Armenian-first compact desktop assistant.
- Glowing desktop Orb that is intended to be visible only while the Windows desktop is foreground.
- Orb and chat hide when another application (including a maximized or full-screen browser) is foreground.
- Chat can be opened from the Orb; diagnostic work continues while the UI is hidden.
- Offline routing for known support requests.
- Allow-listed local diagnostics and limited remediation.
- Action panel showing the support functions invoked and their results.
- Local incident reports.
- Public GitHub Releases update discovery and SHA-256 verification.

## Important limitations

This is an early office pilot, not an unrestricted autonomous administrator. It does not execute arbitrary AI-generated PowerShell. The current build uses a controlled set of local functions; some fixes open Windows settings or require user confirmation. Desktop-only visibility must be tested on Windows 10/11 because shell behavior differs across Windows builds and virtual desktops.

## Source bundle

The complete source archive is stored in the `bundle/` directory as eight sequential binary parts:

`office_ai_support_source.tar.gz.part00` through `part07`.

The GitHub Actions workflow reassembles the parts, extracts the source, runs tests, builds the Windows executable and publishes a GitHub Release with an EXE and SHA-256 checksum.

## Build locally on Windows

1. Clone this repository.
2. Reassemble the source archive by concatenating the eight parts in lexical order.
3. Extract the resulting `office_ai_support_source.tar.gz`.
4. In the extracted project folder, run `first_start.bat` to install dependencies and start the app.
5. Run `build_windows.bat` to build a Windows executable.

The automatic GitHub build is the preferred way to obtain a release EXE.

## Updating

The app checks the latest public GitHub Release for `renkakaka/Office-AI-Support`. Release assets include `OfficeAISupport.exe` and `OfficeAISupport.exe.sha256`. The updater verifies the checksum before installation.

## Security and privacy

Do not commit office ticket exports, employee information, API keys, local `config.json`, or report files. This repository is public. No license has been added; public visibility alone does not grant broad reuse rights. Test releases on a non-production Windows device before deploying to office computers.
