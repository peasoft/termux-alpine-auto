# `termux-alpine-auto`
> Modified by peasoft

[![Release](https://img.shields.io/github/v/release/illvart/termux-alpine?color=orange)][1]
[![License: GPL-3.0](https://img.shields.io/badge/License-GPLv3-blue.svg)][2]
[![CI Status](https://github.com/illvart/termux-alpine/workflows/CI/badge.svg)](https://github.com/illvart/termux-alpine/actions)

> Bash script for installing **Alpine Linux** in [Termux].

<p align="center">
  <img src="https://github.com/illvart/termux-alpine/blob/main/ss.png?raw=true" alt="Alpine Linux Termux"/>
  <br>
  <em>Check out the other screenshots on my <a href="https://www.instagram.com/notudope">Instagram</a>.</em>
</p>

## Table of Contents

<details>
<summary>Details</summary>

- [Installation](#installation)
  - [Launch Alpine Linux](#launch-alpine-linux)
  - [Reinstall](#reinstall)
  - [Uninstall](#uninstall)
- [Options](#options)
- [Credits](#credits)
- [Contributing](#contributing)
- [License](#license)

</details>

## Installation

Open [Termux] app, copy and paste the following command in Termux.

```sh
bash -c "$(curl -fsSL https://raw.githubusercontent.com/peasoft/termux-alpine-auto/main/setup-termux-alpine)"
```

For users in China, please run:

```sh
bash -c "$(curl -fsSL https://fastly.jsdelivr.net/gh/peasoft/termux-alpine-auto@main/setup-termux-alpine)"
```

### Installation with options

Installation [options](#options).

```sh
curl -fsSL https://raw.githubusercontent.com/peasoft/termux-alpine-auto/main/setup-termux-alpine > setup-termux-alpine
chmod +x setup-termux-alpine
./setup-termux-alpine --setup-user
```

Please follow the output of the command above!

#### Launch Alpine Linux

Just typing a command like below in Termux and enter.

```sh
termux-alpine
```

You can also running any commands inside Alpine Linux:

```sh
termux-alpine echo "Hello World"
```

### Reinstall

To reinstall just typing a command like [installation](#installation) above, type *y* for yes, and enter.

Or pass the command with [options](#options) example:

```sh
./setup-termux-alpine -S -F
```

### Uninstall

Please note! Before uninstalling, recommended to backup the current installation.

```sh
./setup-termux-alpine --uninstall
```

Or manually (isn't safe):

```sh
rm -rf ${PREFIX}/bin/termux-alpine \
    ${HOME}/.alpine
```

## Options

```sh
Usage: ./setup-termux-alpine [options]

Options:
--install-nodejs	install nodejs-current, npm, and yarn
--install-python3	install python3 py3-pip, and py3-wheel
-S, --setup-user	setup a non-root user
-F, --fake-kernel	use a fake kernel
-u, --uninstall		full wipe the rootfs installation
-v, --version		show this program version
-h, --help		show this help information
```

If you're using `--setup-user`, to login a non-root user after installation use `login your_username` and enter the password.


## Credits

Credit to [Hax4us](https://github.com/Hax4us) and [termux](https://github.com/termux) for source.

## Contributing

If you would like to help out with some code, check the [details][2].

## License

This project is licensed under the **GPL-3.0 License**. See the [LICENSE][3] file for details.


[1]: https://github.com/illvart/termux-alpine/releases
[2]: https://github.com/illvart/termux-alpine/blob/main/docs/CONTRIBUTING.md
[3]: https://github.com/illvart/termux-alpine/blob/main/LICENSE
[Termux]: https://termux.com

