# Guard Activity

Guard Activity is a local Windows activity logger with a system tray icon, Away mode, and local activity reports.

It is designed to help you see if your own computer was used while you were away.

## Features

- System tray icon
- Away / At computer mode
- Local activity logs
- Local daily report
- Process activity metadata
- Foreground app metadata
- Idle and active-after-idle detection
- File activity metadata for common user folders

## Privacy

Guard Activity does not record:

- Passwords
- Keystrokes
- Clipboard content
- Screenshots
- Microphone audio
- Camera video
- Browser cookies
- Browser tokens
- Private account credentials

Logs are stored locally on your own Windows computer.

## Download

Latest release:

https://github.com/networkluki/guard-activity/releases/latest

## SHA256

Release asset: `guardLog-v1.0.0-win-x64.zip`

```text
ADAB4FBD1E51AC6CE398DCAAA3FFC14DFD23AEDB55E9E9C1E168ABEFC2EA89E3
```


## Verify a Download

Only download Guard Activity from the official GitHub Releases page. Before running a downloaded ZIP file, compare its SHA256 hash with the hash published for that exact release asset.

On Windows PowerShell:

```powershell
Get-FileHash .\guardLog-v1.0.0-win-x64.zip -Algorithm SHA256
```

You can also verify the file in your browser by going to https://theinfo.nu/tools/files/, uploading `guardLog-v1.0.0-win-x64.zip`, and pasting this SHA256 value:

```text
ADAB4FBD1E51AC6CE398DCAAA3FFC14DFD23AEDB55E9E9C1E168ABEFC2EA89E3
```

Do not run the file if the hash differs from the published value.

## Security and Responsible Use

Guard Activity is intended for local use on computers you own or are authorized to monitor. Do not use it for unauthorized monitoring of other people.

See [SECURITY.md](SECURITY.md) for vulnerability reporting, privacy expectations, and recommended hardening guidance.
