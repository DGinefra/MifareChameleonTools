<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>MIFARE Chameleon Tool (MCT) – README preview</title>
  <style>
    :root { color-scheme: light dark; }
    body {
      font-family: system-ui, -apple-system, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      line-height: 1.5;
      max-width: 52rem;
      margin: 2rem auto;
      padding: 0 1.25rem;
    }
    h1 { font-size: 1.75rem; margin-top: 0; }
    h2 { font-size: 1.2rem; margin-top: 1.75rem; border-bottom: 1px solid color-mix(in srgb, CanvasText 18%, transparent); padding-bottom: 0.25rem; }
    p { margin: 0.75rem 0; }
    ul, ol { margin: 0.5rem 0 0.75rem; padding-left: 1.35rem; }
    li { margin: 0.25rem 0; }
    code { font-size: 0.92em; padding: 0.1em 0.35em; border-radius: 4px; background: color-mix(in srgb, CanvasText 8%, transparent); }
    blockquote {
      margin: 1rem 0;
      padding: 0.5rem 1rem;
      border-left: 4px solid color-mix(in srgb, CanvasText 35%, transparent);
      background: color-mix(in srgb, CanvasText 6%, transparent);
    }
    table { width: 100%; border-collapse: collapse; margin: 0.75rem 0; font-size: 0.95rem; }
    th, td { border: 1px solid color-mix(in srgb, CanvasText 20%, transparent); padding: 0.45rem 0.6rem; text-align: left; vertical-align: top; }
    th { background: color-mix(in srgb, CanvasText 8%, transparent); }
    .badges { display: flex; flex-wrap: wrap; gap: 0.5rem; align-items: center; margin: 0.75rem 0; }
    .badges img { height: 20px; }
    hr { margin: 1.5rem 0; border: none; border-top: 1px solid color-mix(in srgb, CanvasText 15%, transparent); }
    .muted { font-size: 0.9rem; opacity: 0.85; }
    .note { font-size: 0.85rem; margin-top: 2rem; }
  </style>
</head>
<body>

  <h1>MIFARE Chameleon Tool (MCT)</h1>

  <p><strong>iOS</strong> companion for <strong>Chameleon Ultra</strong> (Bluetooth): read/write and manage <strong>MIFARE Classic</strong> tags, with a workflow inspired by <strong>Mifare Classic Tool (MCT)</strong>—dumps, keys, tools, and slot helpers. A <strong>Mac</strong> target also lives in this repo (<code>MifareChameleonTool_Mac</code>).</p>

  <div class="badges">
    <img src="https://img.shields.io/badge/iOS-18.6+-blue.svg" alt="iOS 18.6+">
    <img src="https://img.shields.io/badge/Swift-5.0-orange.svg" alt="Swift 5.0">
  </div>

  <p><strong>App Store:</strong> <em>[add your public App Store link here when the listing is live]</em></p>

  <h2>Hardware</h2>
  <ul>
    <li><strong>NFC on tag</strong> (read/write, sniff-related flows): requires a <strong>Chameleon Ultra</strong> connected over <strong>Bluetooth</strong>.</li>
    <li><strong>Offline / no device:</strong> you can still edit dumps (<code>.bin</code>, <code>.mct</code>), compare dumps, manage key files (<code>.keys</code>), and use several tools (Access Bits, Value Block, etc.).</li>
  </ul>

  <h2>Highlights</h2>
  <table>
    <thead>
      <tr><th>Area</th><th>What you get</th></tr>
    </thead>
    <tbody>
      <tr><td><strong>Read / write tag</strong></td><td>MIFARE Classic 1K flows via Chameleon; <code>.keys</code> support; magic Gen1A / Gen2 where applicable</td></tr>
      <tr><td><strong>Edit dump</strong></td><td>Byte editor, sector edit, block copy/paste</td></tr>
      <tr><td><strong>Key files</strong></td><td>Create, import, export <code>.keys</code> (and compatible text formats)</td></tr>
      <tr><td><strong>Tag Detect</strong></td><td>Quick tag / PRNG-style readout from the device (when supported by firmware)</td></tr>
      <tr><td><strong>MF1 key recovery</strong></td><td>Automated classic recovery pipeline aligned with Chameleon-style tooling (dictionary, darkside / nested paths; <strong>hardnested</strong> where applicable)</td></tr>
      <tr><td><strong>Firmware</strong></td><td>Update the device <strong>from the app</strong>: <strong>Normal / Dev</strong> channel, <strong>App / Full</strong> packages, install from <strong>ZIP</strong> when needed</td></tr>
      <tr><td><strong>Tools</strong></td><td>Access Bits, Value Block, UID magic (Gen1A/Gen2), Chameleon slots, dump compare, and more</td></tr>
    </tbody>
  </table>

  <blockquote>
    <strong>Legal / ethical use only.</strong> Use on tags and systems you own or are explicitly authorized to test. Cryptographic tooling is provided for interoperability and security research with compatible hardware.
  </blockquote>

  <h2>Localization</h2>
  <p>UI strings: <strong>English</strong>, <strong>Italian</strong>, <strong>French</strong>, <strong>German</strong>, <strong>Spanish</strong>.</p>

  <h2>Themes</h2>
  <p>Light / dark bases, <strong>Liquid Glass</strong>, <strong>Newspaper</strong>, and custom accent color.</p>

  <h2>Open source &amp; licenses</h2>
  <ul>
    <li>This repository mixes <strong>app source</strong> and <strong>third-party</strong> components.</li>
    <li>The <strong>UltraRecovery</strong> / hardnested-related C code is under <strong>GPL-3.0</strong> (see <code>MifareChameleonTool/MifareChameleonTool/UltraRecovery/LICENSE.GPL-3-UltraRecovery.txt</code>). If you redistribute binaries, respect the GPL obligations for those parts.</li>
  </ul>

  <h2>Community &amp; support</h2>
  <ul>
    <li><strong>Issues:</strong> <a href="https://github.com/DGinefra/MifareChameleonTools/issues">GitHub Issues</a> for bugs and feature requests.</li>
    <li><strong>Privacy:</strong> <a href="https://github.com/DGinefra/MifareChameleonTools/blob/main/PRIVACY.md">in-app privacy policy (markdown)</a></li>
  </ul>

  <h2>References</h2>
  <ul>
    <li><a href="https://github.com/RfidResearchGroup/ChameleonUltra">Chameleon Ultra – RfidResearchGroup</a></li>
    <li><a href="https://www.nxp.com/products/rfid-nfc/mifare-hf/mifare-classic:MC_53483">MIFARE Classic – NXP</a></li>
  </ul>

  <h2>Building (developers)</h2>
  <ol>
    <li>Open <code>MifareChameleonTool/MifareChameleonTool.xcodeproj</code> in <strong>Xcode</strong> (recent stable release recommended).</li>
    <li>Select the <strong>MifareChameleonTool</strong> iOS target, a simulator or device, and <strong>Run</strong>.</li>
    <li>A <strong>Chameleon Ultra</strong> is required for on-tag NFC; other screens work without hardware.</li>
  </ol>

  <hr>
  <p class="note muted"><em>README preview aligned with <code>README.md</code> (≈ v1.0.9). Open this file in a browser for a local render; GitHub uses <code>README.md</code> on the repo home.</em></p>

</body>
</html>
    <li><strong>Offline / no device:</strong> you can still edit dumps (<code>.bin</code>, <code>.mct</code>), compare dumps, manage key files (<code>.keys</code>), and use several tools (Access Bits, Value Block, etc.).</li>
  </ul>

  <h2>Highlights</h2>
  <table>
    <thead>
      <tr><th>Area</th><th>What you get</th></tr>
    </thead>
    <tbody>
      <tr><td><strong>Read / write tag</strong></td><td>MIFARE Classic 1K flows via Chameleon; <code>.keys</code> support; magic Gen1A / Gen2 where applicable</td></tr>
      <tr><td><strong>Edit dump</strong></td><td>Byte editor, sector edit, block copy/paste</td></tr>
      <tr><td><strong>Key files</strong></td><td>Create, import, export <code>.keys</code> (and compatible text formats)</td></tr>
      <tr><td><strong>Tag Detect</strong></td><td>Quick tag / PRNG-style readout from the device (when supported by firmware)</td></tr>
      <tr><td><strong>MF1 key recovery</strong></td><td>Automated classic recovery pipeline aligned with Chameleon-style tooling (dictionary, darkside / nested paths; <strong>hardnested</strong> where applicable)</td></tr>
      <tr><td><strong>Firmware</strong></td><td>Update the device <strong>from the app</strong>: <strong>Normal / Dev</strong> channel, <strong>App / Full</strong> packages, install from <strong>ZIP</strong> when needed</td></tr>
      <tr><td><strong>Tools</strong></td><td>Access Bits, Value Block, UID magic (Gen1A/Gen2), Chameleon slots, dump compare, and more</td></tr>
    </tbody>
  </table>

  <blockquote>
    <strong>Legal / ethical use only.</strong> Use on tags and systems you own or are explicitly authorized to test. Cryptographic tooling is provided for interoperability and security research with compatible hardware.
  </blockquote>

  <h2>Localization</h2>
  <p>UI strings: <strong>English</strong>, <strong>Italian</strong>, <strong>French</strong>, <strong>German</strong>, <strong>Spanish</strong>.</p>

  <h2>Themes</h2>
  <p>Light / dark bases, <strong>Liquid Glass</strong>, <strong>Newspaper</strong>, and custom accent color.</p>

  <h2>Open source &amp; licenses</h2>
  <ul>
    <li>This repository mixes <strong>app source</strong> and <strong>third-party</strong> components.</li>
    <li>The <strong>UltraRecovery</strong> / hardnested-related C code is under <strong>GPL-3.0</strong> (see <code>MifareChameleonTool/MifareChameleonTool/UltraRecovery/LICENSE.GPL-3-UltraRecovery.txt</code>). If you redistribute binaries, respect the GPL obligations for those parts.</li>
  </ul>

  <h2>Community &amp; support</h2>
  <ul>
    <li><strong>Issues:</strong> <a href="https://github.com/DGinefra/MifareChameleonTools/issues">GitHub Issues</a> for bugs and feature requests.</li>
    <li><strong>Privacy:</strong> <a href="https://github.com/DGinefra/MifareChameleonTools/blob/main/PRIVACY.md">in-app privacy policy (markdown)</a></li>
  </ul>

  <h2>References</h2>
  <ul>
    <li><a href="https://github.com/RfidResearchGroup/ChameleonUltra">Chameleon Ultra – RfidResearchGroup</a></li>
    <li><a href="https://www.nxp.com/products/rfid-nfc/mifare-hf/mifare-classic:MC_53483">MIFARE Classic – NXP</a></li>
  </ul>

  <h2>Building (developers)</h2>
  <ol>
    <li>Open <code>MifareChameleonTool/MifareChameleonTool.xcodeproj</code> in <strong>Xcode</strong> (recent stable release recommended).</li>
    <li>Select the <strong>MifareChameleonTool</strong> iOS target, a simulator or device, and <strong>Run</strong>.</li>
    <li>A <strong>Chameleon Ultra</strong> is required for on-tag NFC; other screens work without hardware.</li>
  </ol>

  <hr>
  <p class="note muted"><em>README preview aligned with <code>README.md</code> (≈ v1.0.9). Open this file in a browser for a local render; GitHub uses <code>README.md</code> on the repo home.</em></p>

</body>
</html>
