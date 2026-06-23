# Security Policy

## Supported Versions

Guard Activity is currently in early public release.

| Version | Supported |
| ------- | --------- |
| v1.0.0  | Yes       |

Older or modified builds are not officially supported.

## Reporting a Vulnerability

If you find a security issue in Guard Activity, please report it responsibly.

Do not publicly post exploit details, bypass methods, or sensitive technical information before the issue has been reviewed.

Preferred reporting methods:

* Email: [dev.networkluki@gmail.com](mailto:dev.networkluki@gmail.com)
* Use GitHub private vulnerability reporting if it is enabled for this repository.
* Otherwise, contact the maintainer through the official GitHub repository.

Repository:

```text
https://github.com/networkluki/guard-activity
```

## What to Include

When reporting a vulnerability, include as much safe detail as possible:

* Guard Activity version
* Windows version
* Download source and release asset filename
* Steps to reproduce
* What you expected to happen
* What actually happened
* Relevant screenshots or logs, if they do not contain private data

Please remove personal information, usernames, tokens, file paths, and private log contents before sharing.

## Scope

Security reports may include:

* Local privilege escalation issues
* Unsafe file handling, including path traversal or unsafe permissions
* Sensitive data exposure in logs, reports, release assets, or diagnostics
* Unexpected network behavior
* Unsafe autostart behavior
* Log privacy issues, including collection of keystrokes, clipboard data, screenshots, audio, video, cookies, tokens, or private credentials
* Tampering or integrity problems with release assets, update paths, or local configuration
* Command injection, unsafe deserialization, or execution of untrusted input
* Denial-of-service issues that can corrupt or delete local activity data

## Out of Scope

The following are generally out of scope:

* Reports from modified unofficial builds
* Issues caused by running the app on a compromised system
* Social engineering
* Physical access attacks
* SmartScreen warnings caused only by the app being new or unsigned
* General antivirus detections without technical details
* Vulnerabilities in third-party software that are not directly triggered by Guard Activity

## Privacy and Data Handling

Guard Activity is designed to run locally on Windows.

Guard Activity does not intentionally record:

* Passwords
* Keystrokes
* Clipboard content
* Screenshots
* Microphone audio
* Camera video
* Browser cookies
* Browser tokens
* Private account credentials

Logs are stored locally on the user's own computer.

Do not send raw logs or reports with vulnerability submissions unless the maintainer specifically asks for them. If logs are needed, redact usernames, account names, file paths, window titles, process arguments, tokens, and other private data first.

## Responsible Use

Guard Activity is intended for use on computers you own or are authorized to monitor.

Do not use Guard Activity for unauthorized monitoring of other people.

## Security Notes

Guard Activity may trigger Windows SmartScreen or antivirus warnings because it is a new and unsigned application.

Users should only download Guard Activity from the official GitHub Releases page:

```text
https://github.com/networkluki/guard-activity/releases/latest
```

Users can verify the downloaded ZIP file with the published SHA256 hash. Do not install or run a file if the hash does not exactly match the value published by the maintainer for that specific release asset.

## Recommended Hardening

The current repository contains release and policy documentation only. Based on the documented behavior of a local Windows activity logger, future implementation and release work should follow these controls:

* Keep all logs local by default and require explicit user action before exporting or sharing them.
* Store logs and configuration in a per-user application data directory with permissions limited to that Windows user account.
* Treat process names, window titles, file paths, command lines, and log contents as sensitive data.
* Redact secrets and personal data from diagnostics before displaying or exporting them.
* Avoid collecting keystrokes, clipboard content, screenshots, audio, video, browser cookies, browser tokens, and private credentials.
* Validate and canonicalize paths before reading or writing files to prevent path traversal and accidental writes outside the intended log directory.
* Use atomic file writes for logs and reports to reduce corruption risk if the app exits unexpectedly.
* Avoid running with administrator privileges unless a clearly documented feature requires it.
* Do not execute shell commands built from untrusted input.
* Use HTTPS for any documented download, update, or support links.
* Publish SHA256 hashes for every release asset and keep each hash tied to its exact filename and version.
* Consider code signing release binaries so users can verify publisher identity in addition to file integrity.
* Document any future network behavior, autostart behavior, retention period, and log deletion controls in the README and release notes.

## Response Process

Security reports will be reviewed as soon as possible.

If the issue is confirmed, a fix may be released in a future version and documented in the release notes.
