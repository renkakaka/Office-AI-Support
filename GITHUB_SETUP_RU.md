# GitHub Releases setup

Repository: https://github.com/renkakaka/Office-AI-Support

The repository is public. The Windows client can check public GitHub Releases anonymously; never embed a personal access token in the app.

## Release process
1. Commit the source files and workflow to the default branch.
2. Push a version tag, e.g. `v0.2.1`.
3. GitHub Actions builds `OfficeAISupport.exe` on a Windows runner.
4. The workflow publishes the EXE and SHA-256 checksum as release assets.

## Client configuration
Run `configure_github_updates.bat` on Windows and enter `renkakaka/Office-AI-Support`. The updater checks the latest public release and validates the downloaded file's SHA-256 before installing it.

## Security
Do not commit office ticket exports, employee information, API keys, local config files, or reports. Test releases on a non-production Windows device first.
