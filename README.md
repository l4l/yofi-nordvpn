# rofi-nordvpn
<p align="center">
  <img src="https://i.imgur.com/Y5kDbVf.png">
</p>

<p align="center">
  <a href="./LICENSE.md"><img src="https://img.shields.io/badge/license-MIT-blue.svg"></a>
</p>

Dynamic menu interface for `nordvpn`.

# Dependencies:

 * `yofi`
 * `nordvpn`

# Installation:

Just git clone this repo and place the `yofi-nordvpn` file somewhere on your `PATH` and make sure it is executable `chmod +x yofi-nordvpn`.

# Configuration:

There isn't much to configure. If you are not a `yofi` user don't fret you simply need to adjust the `menu` function to use your chosen dynamic menu program.

# Status bars:

For easy embeding into your chosen status bar, consider using the `-s` flag which outputs the current vpn status.

```sh
$ yofi-nordvpn -s
Paris
```

For polybar here is my module (using the [Siji](https://github.com/stark/siji) font):

```ini
[module/vpn]
type = custom/script
label =  %output%
exec = yofi-nordvpn -s
interval = 10
click-left = yofi-nordvpn &
```
