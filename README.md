# MIFARE Chameleon Tool (MCT) – iOS

iOS app to read, write and manage MIFARE Classic tags via **Chameleon Ultra** (Bluetooth). Styled after Mifare Classic Tool (MCT) with dump editor, tools and slot management.

![iOS](https://img.shields.io/badge/iOS-18.6+-blue.svg)

**Now available on the App Store.**

[![Download on the App Store](https://img.shields.io/badge/Download-App%20Store-black?logo=apple)](https://apps.apple.com/it/app/mifare-chameleon-tool/id6761231484)

## Hardware requirements

NFC operations (tag read/write) require a **Chameleon Ultra** connected via Bluetooth.

Without Chameleon Ultra you can still:
- edit dumps (.bin, .mct)
- compare dumps
- manage key files (.keys)
- use tools (Access Bits, Value Block, etc.)

## Features

| Section | Description |
|---------|-------------|
| **Read tag** | Full MIFARE 1K dump read via Chameleon Ultra with .keys file |
| **Write to tag** | Dump write to tag, magic tag Gen1A/Gen2 support, sector selection |
| **Edit dump** | Byte-by-byte editor, sector edit, swipe copy/paste blocks |
| **Key files** | .keys file management (create, import, export) |
| **Tools** | Access Bits, Value Block, Change UID magic, Chameleon Slots, Compare dumps |


### MIFARE tools

- **Access Bits**: Decode/encode trailer bytes (6,7,8), factory/read-only/value block presets
- **Value Block**: Decode/encode, Increment/Decrement/Transfer/Restore
- **Change UID magic**: Gen1A and Gen2 support, tag type detection
- **Chameleon slots**: 8-slot management, HF on/off, mfkey32 sniff, Shadow Gen4
- **Compare dumps**: A/B comparison with byte diff highlighting

## Localization

The app is available in:
- Italian
- English
- French
- German
- Spanish

## 📢 Community & Support

For updates, support, and discussions about the project, join the Telegram channel:
👉 https://t.me/MifareChameleonTool
Or search directly: **@MifareChameleonTool**

## Themes

- White, Black
- Liquid Glass, Newspaper style
- Custom color

## References

- [Privacy Policy](https://github.com/DGinefra/MifareChameleonTools/blob/main/Privacy.md)
- [Chameleon Ultra – RfidResearchGroup](https://github.com/RfidResearchGroup/ChameleonUltra)
- [MIFARE Classic – NXP](https://www.nxp.com/products/rfid-nfc/mifare-hf/mifare-classic)
