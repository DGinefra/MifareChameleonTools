## MIFARE Chameleon Tool (MCT) – iOS

iOS app for Chameleon Ultra (Bluetooth) to read, write and manage MIFARE Classic tags. Inspired by Mifare Classic Tool (MCT), featuring dump editing, key management, slot management and advanced NFC tools.

![iOS](https://img.shields.io/badge/iOS-18.6+-blue.svg)
![Swift](https://img.shields.io/badge/Swift-5.0-orange.svg)

Now available on the App Store.# MIFARE Chameleon Tool (MCT)

**iOS** companion for **Chameleon Ultra** (Bluetooth): read/write and manage **MIFARE Classic** tags, with a workflow inspired by **Mifare Classic Tool (MCT)**—dumps, keys, tools, and slot helpers. A **Mac** target also lives in this repo (`MifareChameleonTool_Mac`).

![iOS](https://img.shields.io/badge/iOS-18.6+-blue.svg)
![Swift](https://img.shields.io/badge/Swift-5.0-orange.svg)

[![Download on the App Store](https://img.shields.io/badge/Download-App%20Store-black?logo=apple)](https://apps.apple.com/app/mifare-chameleon-tool/id6761231484)

## Hardware

- **NFC on tag** (read/write, sniff-related flows): requires a **Chameleon Ultra** connected over **Bluetooth**.
- **Offline / no device:** you can still edit dumps (`.bin`, `.mct`), compare dumps, manage key files (`.keys`), and use several tools (Access Bits, Value Block, etc.).

## Highlights

| Area | What you get |
|------|----------------|
| **Read / write tag** | MIFARE Classic 1K flows via Chameleon; `.keys` support; magic Gen1A / Gen2 where applicable |
| **Edit dump** | Byte editor, sector edit, block copy/paste |
| **Key files** | Create, import, export `.keys` (and compatible text formats) |
| **Tag Detect** | Quick tag / PRNG-style readout from the device (when supported by firmware) |
| **MF1 key recovery** | Automated classic recovery pipeline aligned with Chameleon-style tooling (dictionary, darkside / nested paths; **hardnested** where applicable) |
| **mfkey32v2 / mfkey64** | Dedicated nonce log and recovery workflows, including mfkey32v2-compatible records and mfkey64 support |
| **Advanced attacks** | Static Encrypted Nonces, darkside, nested/static nested, and hardnested workflows |
| **LF tag emulation** | External LF scan and slot UID programming for EM410X, HID Prox, Viking, ioProx, and PAC/Stanley |
| **Firmware update** | Check device firmware and update **from the app**: **Normal / Dev** channel, **App / Full** packages, install from **ZIP** when needed |
| **Tools** | Access Bits, Value Block, UID magic (Gen1A/Gen2), Chameleon slots, dump compare, and more |

> **Legal / ethical use only.** Use on tags and systems you own or are explicitly authorized to test. Cryptographic tooling is provided for interoperability and security research with compatible hardware.

## App Features & Quick Guide

Features that interact with physical tags require a **Chameleon Ultra** connected over Bluetooth. In offline mode, you can still edit dumps, compare files, manage keys, and use tools that work on local data.

- **Connect Chameleon Ultra:** turn on the device, open the app, tap **Connect Chameleon Ultra**, and select it. You can also enter offline mode and connect later.
- **Read a MIFARE Classic tag:** open **Read tag**, select a `.keys` file, place the tag on Chameleon, and start reading. The app tries available keys, builds the dump, and lets you save or edit it.
- **Write a MIFARE Classic tag:** open **Write tag**, select keys, load a `.bin` or `.mct` dump, choose sectors, and keep the tag steady on Chameleon. For magic tags, you can enable UID writing and choose Gen1A or Gen2.
- **Edit dumps:** open **Edit dump**, import a `.bin` or `.mct` file, select sector/block, edit bytes in hex, copy/paste blocks, and save again.
- **Manage key files:** open **Key files** to create, import, edit, export, or share `.keys`, `.txt`, and `.dic` files. Each line contains one 6-byte MIFARE key in hex format.
- **Tag Detect:** open **Tools > Tag Detect**, place the tag on Chameleon, and start scanning. The screen shows UID, ATQA, SAK, type, and PRNG hints when supported by firmware.
- **Automatic MF1 key recovery:** from **Tag Detect** or **Tools**, start key recovery. The app uses dictionary, darkside, nested, static nested, or hardnested depending on the tag, then saves recovered keys as `.keys`.
- **Ultra GUI-style advanced attacks/acquisition:** in **Tools**, run darkside, static encrypted nested, and sector key checks. Keep the tag on the antenna during the full process.
- **mfkey32:** open **Tools > mfkey32**, prepare a Classic 1K slot, enable mfkey32 sniff, trigger authentication with an external reader, then run recovery. Captured nonces are validated to reduce false keys.
- **mfkey64:** open **Tools > mfkey64**, enter/import required nonce data, and run key calculation when you have a valid authentication pair.
- **Static Encrypted Nonces:** launch the dedicated attack from **Tag Detect** or **Tools**, set the known key if needed, acquire nonces, and let the solver filter/verify candidate keys.
- **Chameleon slots:** open **Tools > Chameleon slots** to manage all 8 slots: active slot, load/read dump, HF/LF enable, nicknames, and slot reinitialize.
- **External LF scan:** in slot configuration, enable LF, choose tag type (EM410X, HID Prox, Viking, ioProx, or PAC/Stanley), run external LF scan, and save UID to the selected slot.
- **Compare dumps:** open **Tools > Compare dumps**, load dump A and dump B, review byte-by-byte differences, and export/reopen edited files.
- **Access Bits:** open **Tools > Access Bits** or tap access condition bytes from the dump editor. Enter trailer bytes 6, 7, and 8, decode permissions, and apply presets.
- **Value Block:** from dump editor or MIFARE tools, inspect/build value blocks. Decode/encode works offline; increment/decrement/transfer/restore require connected Chameleon.
- **Change magic UID:** open **Tools > Change UID (magic)**, detect tag type, enter new hex UID, and write to Gen1A or Gen2 magic tags. The app reads back to verify.
- **BIN / HEX / DEC converter:** open **Tools > Converter**, choose conversion direction, set endianness when needed, and copy results.
- **Firmware and hardware checks:** open **Tools > Firmware version** to read device info, choose Normal or Dev channel, and update via DFU `.zip` package when needed.
- **Settings, language, and theme:** open **Info > Settings** to change language, theme, color, privacy, and run global actions such as clearing and turning off all slots.

## Localization

UI strings: **English**, **Italian**, **French**, **German**, **Spanish**.

## Themes

Light / dark bases, **Liquid Glass**, **Newspaper**, and custom accent color.

## Open source & licenses

- This repository mixes **app source** and **third-party** components.
- The **UltraRecovery** / hardnested-related C code is under **GPL-3.0** (see `MifareChameleonTool/MifareChameleonTool/UltraRecovery/LICENSE.GPL-3-UltraRecovery.txt`). If you redistribute binaries, respect the GPL obligations for those parts.

## Community & support

- **Website:** [mifarechameleontool.com](https://mifarechameleontool.com)
- **Repository:** [DGinefra/MifareChameleonTools](https://github.com/DGinefra/MifareChameleonTools)
- **Issues:** [GitHub Issues](https://github.com/DGinefra/MifareChameleonTools/issues) for bugs and feature requests.
- **Telegram:** [t.me/MifareChameleonTool](https://t.me/MifareChameleonTool)
- **Privacy:** [Privacy policy (markdown)](https://github.com/DGinefra/MifareChameleonTools/blob/main/PRIVACY.md)

## References

- [Chameleon Ultra – RfidResearchGroup](https://github.com/RfidResearchGroup/ChameleonUltra)

## Building (developers)

1. Open `MifareChameleonTool/MifareChameleonTool.xcodeproj` in **Xcode** (recent stable release recommended).
2. Select the **MifareChameleonTool** iOS target, a simulator or device, and **Run**.
3. A **Chameleon Ultra** is required for on-tag NFC; other screens work without hardware.

---

*README aligned with app features around **v1.1** (LF slot support, mfkey32/64, static encrypted nonces, firmware update UX + nested / hardnested integration).*


[![Download on the App Store](https://img.shields.io/badge/Download-App%20Store-black?logo=apple)](https://apps.apple.com/app/mifare-chameleon-tool/id6761231484)

## Hardware

- **NFC on tag** (read/write, sniff-related flows): requires a **Chameleon Ultra** connected over **Bluetooth**.
- **Offline / no device:** you can still edit dumps (`.bin`, `.mct`), compare dumps, manage key files (`.keys`), and use several tools (Access Bits, Value Block, etc.).

## Highlights

| Area | What you get |
|------|----------------|
| **Read / write tag** | MIFARE Classic 1K flows via Chameleon; `.keys` support; magic Gen1A / Gen2 where applicable |
| **Edit dump** | Byte editor, sector edit, block copy/paste |
| **Key files** | Create, import, export `.keys`|
| **Tag Detect** | Quick tag / PRNG-style readout from the device|
| **MF1 key recovery** | Automated classic recovery pipeline aligned with Chameleon-style tooling (dictionary, darkside / nested paths; **hardnested** where applicable) |
| **Firmware** | Update the device Normal and Dev firmware, install from **ZIP** when needed |
| **Tools** | Access Bits, Value Block, UID magic (Gen1A/Gen2), Chameleon slots, dump compare, and more |

> **Legal / ethical use only.** Use on tags and systems you own or are explicitly authorized to test. Cryptographic tooling is provided for interoperability and security research with compatible hardware.

## Localization

**English**, 
**Italian**, 
**French**, 
**German**, 
**Spanish**.

## Themes

Light / dark bases, Liquid Glass, Newspaper, and custom accent color.


## Community & support

- **Issues:** [GitHub Issues](https://github.com/DGinefra/MifareChameleonTools/issues) for bugs and feature requests.
- **Telegram:** [t.me/MifareChameleonTool](https://t.me/MifareChameleonTool)
- **Privacy:** [Privacy policy](https://github.com/DGinefra/MifareChameleonTools/blob/main/Privacy.md)

## References

- [Chameleon Ultra – RfidResearchGroup](https://github.com/RfidResearchGroup/ChameleonUltra)
- [MIFARE Classic – NXP](https://www.nxp.com/docs/en/data-sheet/MF1S50YYX_V1.pdf)


---
