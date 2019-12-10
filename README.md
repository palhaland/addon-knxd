# Community Hass.io Add-ons: KNXD

[![GitHub Release][releases-shield]][releases]
![Project Stage][project-stage-shield]
[![License][license-shield]](LICENSE.md)

![Supports aarch64 Architecture][aarch64-shield]
![Supports amd64 Architecture][amd64-shield]
![Supports armhf Architecture][armhf-shield]
![Supports armv7 Architecture][armv7-shield]
![Supports i386 Architecture][i386-shield]

![Project Maintenance][maintenance-shield]
[![GitHub Activity][commits-shield]][commits]

[![Buy me a coffee][buymeacoffee-shield]][buymeacoffee]

This add-on sets up a knxd daemon that could also act as a tunnel or
TCP/IP gateway in addition to connect xknx component to it.

## About

This add-on sets up a knxd daemon on the hass-io installation, enabling
it to act as a TCP/IP gateway for the KNX system.

## WARNING


## Features

## Installation

The installation of this add-on is pretty straightforward and not different in
comparison to installing any other Hass.io add-on.

1. [Add my Hass.io add-ons repository][repository] to your Hass.io instance.
1. Install the "knxd" add-on.
1. Configure the addon
1. Start the "knxd" add-on.
1. Check the logs of the "knxd" add-on to see if everything
    went well.

**NOTE**: Do not add this repository to Hass.io, please use:
`https://github.com/palhaland/hassio-addon-repo`.

## Configuration

**Note**: _Remember to restart the add-on when the configuration is changed._

knxd add-on configuration:

```json
{
  “address”: “0.0.1”,
  “client_address”: “0.0.1:10”,
  “interface”: “tpuart”,
  “device”: “/dev/ttyAMA0”,
  “custom_config”: “”
}
```

**Note**: _This is just an example, don't copy and paste it! Create your own!_

### Option group `knxd`

---

The following options are for the option group: `knxd`.

#### Option `address`: `0.0.1`

This option allows you to change the address the knxd daemon will use on the KNX
bus network.

#### Option `client_address`: `0.0.2:10`

This option allows you to change what addresses the clients that connect through
the daemon can use. In this case it is from 1:10

#### Option `interface` `tpuart`

Depending on what type of device you have connected to the Home-Assistant device,
you need to select the correct one here. Can can be one of:
* tpuart
* usb

#### Option `device`: `/dev/ttyAMA0`

The default device to communicate with.

#### Option `custom_config`: ``

This is for additional configuration options to start the knxd server with.


## Known issues and limitations


## Changelog & Releases

This repository keeps a change log using [GitHub's releases][releases]
functionality. The format of the log is based on
[Keep a Changelog][keepchangelog].

Releases are based on [Semantic Versioning][semver], and use the format
of ``MAJOR.MINOR.PATCH``. In a nutshell, the version will be incremented
based on the following:

- ``MAJOR``: Incompatible or major changes.
- ``MINOR``: Backwards-compatible new features and enhancements.
- ``PATCH``: Backwards-compatible bugfixes and package updates.

## Support

Got questions?

You have several options to get them answered:

- The [Home Assistant Discord chat server][discord-ha] for general Home
  Assistant discussions and questions.
- The Home Assistant [Community Forum][forum].
- Join the [Reddit subreddit][reddit] in [/r/homeassistant][reddit]

You could also [open an issue here][issue] GitHub.

## Contributing

This is an active open-source project. We are always open to people who want to
use the code or contribute to it.

We have set up a separate document containing our
[contribution guidelines](CONTRIBUTING.md).

Thank you for being involved! :heart_eyes:

## Authors & contributors

For a full list of all authors and contributors,
check [the contributor's page][contributors].

## We have got some Hass.io add-ons for you

Want some more functionality to your Hass.io Home Assistant instance?

We have created multiple add-ons for Hass.io. For a full list, check out
our [GitHub Repository][repository].

## License

MIT License

Copyright (c) 2019 Pål Håland

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[alpine-packages]: https://pkgs.alpinelinux.org/packages
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[buymeacoffee-shield]: https://www.buymeacoffee.com/assets/img/guidelines/download-assets-sm-2.svg
[buymeacoffee]: https://www.buymeacoffee.com/palhaland
[commits-shield]: https://img.shields.io/github/commit-activity/y/palhaland/addon-knxd.svg
[commits]: https://github.com/palhaland/addon-knxd/commits/master
[contributors]: https://github.com/palhaland/addon-knxd/graphs/contributors
[discord-ha]: https://discord.gg/c5DvZ4e
[discord-shield]: https://img.shields.io/discord/478094546522079232.svg
[forum-shield]: https://img.shields.io/badge/community-forum-brightgreen.svg
[palhaland]: https://github.com/palhaland
[home-assistant]: https://home-assistant.io
[i386-shield]: https://img.shields.io/badge/i386-yes-green.svg
[issue]: https://github.com/palhaland/addon-knxd/issues
[keepchangelog]: http://keepachangelog.com/en/1.0.0/
[license-shield]: https://img.shields.io/github/license/palhaland/addon-knxd.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2019.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-production%20ready-brightgreen.svg
[reddit]: https://reddit.com/r/homeassistant
[releases-shield]: https://img.shields.io/github/release/palhaland/addon-knxd.svg
[releases]: https://github.com/palhaland/addon-knxd/releases
[repository]: https://github.com/palhaland/hassio-addon-repo
[semver]: http://semver.org/spec/v2.0.0.htm
