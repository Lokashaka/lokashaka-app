# Lokashaka

AI companions that live on your desktop. They react to your day and chat with an AI that runs entirely on your own computer.

This repository only hosts the installers. Learn more and manage your account at [lokashaka.id](https://lokashaka.id).

## Download

Get the latest version from [Releases](https://github.com/Lokashaka/lokashaka-app/releases/latest).

| System | File |
| --- | --- |
| Windows 10/11 (64-bit) | `LokashakaSetup-<version>.exe` |
| Ubuntu 22.04+, Debian 12+ (and Mint, Pop!_OS, Zorin, ...) | apt repository (recommended) or `lokashaka_<version>_amd64.deb` |
| Any 64-bit Linux with glibc 2.34+ (Arch, Manjaro, EndeavourOS, Fedora 35+, ...) | `Lokashaka-<version>-x86_64.AppImage` |
| Linux without FUSE | `Lokashaka-<version>-linux-x86_64.tar.gz` |

Every character can be tried free for 3 days per computer. The AI brain (about 1.1 GB per language) is needed for chat: the Windows installer can download it for you, or use the Download button inside the app.

## Install on Linux

### Ubuntu / Debian (recommended: apt repository)

One command adds the signed Lokashaka repository and installs the app:

```sh
curl -fsSL https://apt.lokashaka.id/install.sh | sudo sh
```

Updates then arrive with your normal system updates (`sudo apt update && sudo apt upgrade`). The repository is signed with the key `2CCE 3A38 97DD AAC6 E885 1C91 C06E A57C F098 B5B4`; manual setup steps are at [apt.lokashaka.id](https://apt.lokashaka.id). Uninstall with `sudo apt remove lokashaka`.

### Ubuntu / Debian (single .deb file)

Without the repository you can install the package directly, but you will not get automatic updates:

```sh
wget https://github.com/Lokashaka/lokashaka-app/releases/latest/download/lokashaka_1.0.6_amd64.deb
sudo apt install ./lokashaka_1.0.6_amd64.deb
```

Use `apt` (not `dpkg -i`) so the required system libraries are installed too. Lokashaka then appears in your app menu, or run `lokashaka` in a terminal. Uninstall with `sudo apt remove lokashaka`.

### Arch, Fedora and other distros (AppImage)

```sh
wget https://github.com/Lokashaka/lokashaka-app/releases/latest/download/Lokashaka-1.0.6-x86_64.AppImage
chmod +x Lokashaka-1.0.6-x86_64.AppImage
./Lokashaka-1.0.6-x86_64.AppImage
```

If it says FUSE is missing, install it (`sudo pacman -S fuse2` on Arch, `sudo apt install libfuse2t64` on Ubuntu 24.04+) or use the tar.gz below.

### Without FUSE (tar.gz)

```sh
tar xzf Lokashaka-1.0.6-linux-x86_64.tar.gz
./Lokashaka/lokashaka
```

### Notes for Linux

- Characters need to move their own windows, which Wayland does not allow, so Lokashaka always runs through XWayland. This works out of the box on GNOME and KDE.
- Your data is stored in `~/.local/share/Lokashaka`.

## Windows SmartScreen

The installer is not code-signed yet, so Windows may show "Windows protected your PC". Choose **More info**, then **Run anyway**.

## Verify your download

Compare the file's SHA-256 with `SHA256SUMS.txt` from the same release:

```
certutil -hashfile LokashakaSetup-1.0.4.exe SHA256    # Windows
sha256sum -c SHA256SUMS.txt --ignore-missing          # Linux
```

## Support

[halo@lokashaka.id](mailto:halo@lokashaka.id) · [Terms of Service](https://lokashaka.id/terms) · [Privacy Policy](https://lokashaka.id/privacy)
