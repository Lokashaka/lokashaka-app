# Lokashaka

AI companions that live on your desktop. They react to your day and chat with an AI that runs entirely on your own computer.

This repository only hosts the installers. Learn more and manage your account at [lokashaka.id](https://lokashaka.id).

## Download

Get the latest version from [Releases](https://github.com/Lokashaka/lokashaka-app/releases/latest).

| System | File |
| --- | --- |
| Windows 10/11 (64-bit) | `LokashakaSetup-<version>.exe` |
| Linux (64-bit, Ubuntu 22.04+, Debian 12+, Fedora 35+) | `Lokashaka-<version>-x86_64.AppImage` |
| Linux without FUSE | `Lokashaka-<version>-linux-x86_64.tar.gz` |

Every character can be tried free for 3 days per computer. The AI brain (about 1.1 GB per language) is needed for chat: the Windows installer can download it for you, or use the Download button inside the app.

## Windows SmartScreen

The installer is not code-signed yet, so Windows may show "Windows protected your PC". Choose **More info**, then **Run anyway**.

## Verify your download

Compare the file's SHA-256 with `SHA256SUMS.txt` from the same release:

```
certutil -hashfile LokashakaSetup-1.0.0.exe SHA256    # Windows
sha256sum -c SHA256SUMS.txt --ignore-missing          # Linux
```

## Support

[halo@lokashaka.id](mailto:halo@lokashaka.id) · [Terms of Service](https://lokashaka.id/terms) · [Privacy Policy](https://lokashaka.id/privacy)
