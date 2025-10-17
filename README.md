# Kali-Installer Build-Scripts

_`simple-cdd` configuration for Kali ISO images._

These are the same [build-scripts](https://gitlab.com/kalilinux/build-scripts) that the [Kali team](https://www.kali.org/) uses to generate the official Kali Linux base images, found here: [kali.org/get-kali/](https://www.kali.org/get-kali/).

_Build your Kali Linux image today!_

- - -

These images offer customization during setup. For being able to live boot into Kali, from such a USB/CD/DVD/sdCard, see [kali-live](https://gitlab.com/kalilinux/build-scripts/kali-live).

- [kali-installer](https://gitlab.com/kalilinux/build-scripts/kali-installer) uses [Simple-CDD](https://wiki.debian.org/Simple-CDD) _(which is a wrapper for [debian-cd](https://wiki.debian.org/debian-cd))_
- [kali-live](https://gitlab.com/kalilinux/build-scripts/kali-live) uses [live-build](https://live-team.pages.debian.net/live-manual/html/live-manual/index.en.html)

- - -

# Help

## How to build:

```console
./build.sh --verbose --variant karla
```

### What each files (probably) does

**`simple-cdd/profiles/kali-karla.packages`** - Lists packages that are automatically installed when the karla variant is selected during installation.

**`simple-cdd/profiles/kali.preseed`** - Contains debconf answers for automated installation choices. 

**`simple-cdd/profiles/kali-karla.postinst`** - Runs after installation completes. Basic Linux config (e.g. create user).

### Installation

```console
$ ./build.sh --help
Usage: ./build.sh [<option>...]

  --distribution <arg>
  --arch <arg>
  --verbose
  --debug
  --variant <arg>
  --version <arg>
  --subdir <arg>
  --get-image-path
  --no-clean
  --clean
  --help
$
```

