## MIFARE Chameleon Tool (MCT) – iOS

iOS app for Chameleon Ultra (Bluetooth) to read, write and manage MIFARE Classic tags. Inspired by Mifare Classic Tool (MCT), featuring dump editing, key management, slot management and advanced NFC tools.

![iOS](https://img.shields.io/badge/iOS-18.6+-blue.svg)
![Swift](https://img.shields.io/badge/Swift-5.0-orange.svg)

Now available on the App Store.

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
| **Firmware** | Update the device **from the app**: **Normal / Dev** channel, **App / Full** packages, install from **ZIP** when needed |
| **Tools** | Access Bits, Value Block, UID magic (Gen1A/Gen2), Chameleon slots, dump compare, and more |

> **Legal / ethical use only.** Use on tags and systems you own or are explicitly authorized to test. Cryptographic tooling is provided for interoperability and security research with compatible hardware.

## Localization

UI strings: **English**, **Italian**, **French**, **German**, **Spanish**.

## Themes

Light / dark bases, **Liquid Glass**, **Newspaper**, and custom accent color.


## Community & support

- **Repository:** [DGinefra/MifareChameleonTools](https://github.com/DGinefra/MifareChameleonTools)
- **Issues:** [GitHub Issues](https://github.com/DGinefra/MifareChameleonTools/issues) for bugs and feature requests.
- **Telegram:** [t.me/MifareChameleonTool](https://t.me/MifareChameleonTool)
- **Privacy:** [Privacy policy (markdown)](https://github.com/DGinefra/MifareChameleonTools/blob/main/PRIVACY.md)

## References

- [Chameleon Ultra – RfidResearchGroup](https://github.com/RfidResearchGroup/ChameleonUltra)
- [MIFARE Classic – NXP](https://www.nxp.com/products/rfid-nfc/mifare-hf/mifare-classic)


---
