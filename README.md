MIFARE Chameleon Tool (MCT) – iOS

iOS app to read, write and manage MIFARE Classic tags via Chameleon Ultra (Bluetooth). Styled after Mifare Classic Tool (MCT) with dump editor, tools and slot management.

iOS

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
| **Firmware** | Update the device **from the app**: **Normal / Dev** channel, **App / Full** packages, install from **ZIP** when needed |
| **Tools** | Access Bits, Value Block, UID magic (Gen1A/Gen2), Chameleon slots, dump compare, and more |

> **Legal / ethical use only.** Use on tags and systems you own or are explicitly authorized to test. Cryptographic tooling is provided for interoperability and security research with compatible hardware.

## Localization

UI strings: **English**, **Italian**, **French**, **German**, **Spanish**.

## Themes

Light / dark bases, **Liquid Glass**, **Newspaper**, and custom accent color.

## Open source & licenses

- This repository mixes **app source** and **third-party** components.
- The **UltraRecovery** / hardnested-related C code is under **GPL-3.0** (see `MifareChameleonTool/MifareChameleonTool/UltraRecovery/LICENSE.GPL-3-UltraRecovery.txt`). If you redistribute binaries, respect the GPL obligations for those parts.

## Community & support

- **Repository:** [DGinefra/MifareChameleonTools](https://github.com/DGinefra/MifareChameleonTools)
- **Issues:** [GitHub Issues](https://github.com/DGinefra/MifareChameleonTools/issues) for bugs and feature requests.
- **Telegram:** [t.me/MifareChameleonTool](https://t.me/MifareChameleonTool)
- **Privacy:** [Privacy policy (markdown)](https://github.com/DGinefra/MifareChameleonTools/blob/main/PRIVACY.md)

## References

- [Chameleon Ultra – RfidResearchGroup](https://github.com/RfidResearchGroup/ChameleonUltra)
- [MIFARE Classic – NXP](https://www.nxp.com/products/rfid-nfc/mifare-hf/mifare-classic)

## Building (developers)

1. Open `MifareChameleonTool/MifareChameleonTool.xcodeproj` in **Xcode** (recent stable release recommended).
2. Select the **MifareChameleonTool** iOS target, a simulator or device, and **Run**.
3. A **Chameleon Ultra** is required for on-tag NFC; other screens work without hardware.

---

*README aligned with app features around **v1.0.9** (firmware update UX + nested / hardnested integration).*


Download on the App Store

Hardware requirements

NFC operations (tag read/write) require a Chameleon Ultra connected via Bluetooth.

Without Chameleon Ultra you can still:

edit dumps (.bin, .mct)
compare dumps
manage key files (.keys)
use tools (Access Bits, Value Block, etc.)
Features

Section	Description
Read tag	Full MIFARE 1K dump read via Chameleon Ultra with .keys file
Write to tag	Dump write to tag, magic tag Gen1A/Gen2 support, sector selection
Edit dump	Byte-by-byte editor, sector edit, swipe copy/paste blocks
Key files	.keys file management (create, import, export)
Tools	Access Bits, Value Block, Change UID magic, Chameleon Slots, Compare dumps
MIFARE tools

Access Bits: Decode/encode trailer bytes (6,7,8), factory/read-only/value block presets
Value Block: Decode/encode, Increment/Decrement/Transfer/Restore
Change UID magic: Gen1A and Gen2 support, tag type detection
Chameleon slots: 8-slot management, HF on/off, mfkey32 sniff, Shadow Gen4
Compare dumps: A/B comparison with byte diff highlighting
Localization

The app is available in:

Italian
English
French
German
Spanish
📢 Community & Support

For updates, support, and discussions about the project, join the Telegram channel: 👉 https://t.me/MifareChameleonTool Or search directly: @MifareChameleonTool

Themes

White, Black
Liquid Glass, Newspaper style
Custom color
References

Privacy Policy
Chameleon Ultra – RfidResearchGroup
MIFARE Classic – NXP
