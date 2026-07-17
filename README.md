# wireshark-prodj-dissectors
Wireshark Dissectors for PRO DJ LINK protocol

Based on the awesome [dysentery](https://github.com/Deep-Symmetry/dysentery) project and community.


## Install

Copy all `.lua` files to:

- (Windows)      `%APPDATA%\Wireshark\plugins\`
- (Linux)        `$HOME/.wireshark/plugins`
- (Mac)          `$HOME/.config/wireshark/plugins` (you may need to create the `plugins` folder).
                  If the `wireshark` directory doesn't exist in `.config`, try `$HOME/.wireshark/plugins` instead —
                  both paths may work depending on your Wireshark version.


## Screenshots

![](announce.png)

![](cdj3000-touch-audio.png)


## Protocols

| File | Layer | Display filter |
|------|-------|----------------|
| `pro-dj-link-announce.lua` | UDP announce (:50000) | `pdj_announce` |
| `pro-dj-link-status.lua` | UDP status (:50002) | `pdj_status` |
| `pro-dj-link-beat.lua` | UDP beat (:50001) | `pdj_beat` |
| `pro-dj-link-audio.lua` | UDP audio | `pdj_audio` |
| `pro-dj-link-dbserver.lua` | TCP dbserver (library / menu API) | `pdj_dbserver` |

The DB Server dissector covers the TCP metadata protocol (Deep Symmetry **dbserver**, magic `0x872349AE`). It is **not** the on-disk USB DeviceSQL/PDB export format.

## Contributions

Contributions are welcome!

