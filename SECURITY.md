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
* Steps to reproduce
* What you expected to happen
* What actually happened
* Relevant screenshots or logs, if they do not contain private data

Please remove personal information, usernames, tokens, file paths, and private log contents before sharing.

## Scope

Security reports may include:

* Local privilege escalation issues
* Unsafe file handling
* Sensitive data exposure
* Unexpected network behavior
* Unsafe autostart behavior
* Log privacy issues
* Tampering or integrity problems

## Out of Scope

The following are generally out of scope:

* Reports from modified unofficial builds
* Issues caused by running the app on a compromised system
* Social engineering
* Physical access attacks
* SmartScreen warnings caused only by the app being new or unsigned
* General antivirus detections without technical details

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

## Responsible Use

Guard Activity is intended for use on computers you own or are authorized to monitor.

Do not use Guard Activity for unauthorized monitoring of other people.

## Security Notes

Guard Activity may trigger Windows SmartScreen or antivirus warnings because it is a new and unsigned application.

Users should only download Guard Activity from the official GitHub Releases page:

```text
https://github.com/networkluki/guard-activity/releases/latest
```

Users can verify the downloaded ZIP file with the published SHA256 hash.

## Response Process

Security reports will be reviewed as soon as possible.

If the issue is confirmed, a fix may be released in a future version and documented in the release notes.
