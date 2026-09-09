# DNST

This repository contains the English DNST/SSHPlus installer script.

## Run on Ubuntu 20.04 x86_64

```bash
apt-get update -y && apt-get upgrade -y && wget -O DNST https://raw.githubusercontent.com/karyan779/DNST/main/DNST && chmod +x DNST && ./DNST
```

The script must run as `root` on an **Ubuntu 20.04 x86_64** VPS. It installs external modules, changes SSH/service settings, adds firewall rules, creates scheduled tasks, and downloads additional files. Review the source and take a VPS backup before running it.

## Compatibility and error-handling changes

The script now creates required working directories, uses reliable download checks, uses `python3-pip` and `pip3` on Ubuntu 20, prepares the SlowDNS binary from a working public source, generates and verifies `server.key` and `server.pub`, avoids errors when optional files are absent, and uses safe cleanup so the `/root/Plus` warning does not appear when the file was not downloaded under that name.

The script was not executed during preparation. It passed `bash -n` syntax validation.
