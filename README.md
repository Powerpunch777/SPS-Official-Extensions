# SPS Official Extensions

For the SPS product overview, downloads, and feedback routes, visit
[Powerpunch777/SPS](https://github.com/Powerpunch777/SPS).

This is the static, signed distribution channel for SPS-built extensions. SPS
Desktop presents connected Catalog sources in Settings > Plugins. This is not a
community marketplace and it does not accept third-party uploads.

The repository contains only immutable Registry metadata and `.spsplugin`
artifacts that are already distributed to SPS Desktop installations. It does
not contain SPS Core, SPS Desktop, Owner Host, user projects, Room or Task
data, API keys, Registry private keys, or Publisher private keys.

## Verification

SPS Desktop pins the official Registry root public key and verifies:

1. `registry.json` root signature
2. each immutable release record signature
3. artifact SHA-256 and size before staging

The Registry catalog never grants installation or execution permission by
itself. It only provides package metadata that SPS can inspect before a plugin
lifecycle change.

For a local integrity check with the public SDK:

```powershell
git clone https://github.com/Powerpunch777/SPS-Official-Extensions.git
cd SPS-Official-Extensions
node ..\sps-plugin-sdk\cli\sps-plugin.mjs inspect .
```

## Source boundary

A plugin artifact must be available to the computer that installs it, so its
runtime files can be inspected by the recipient. This does not publish SPS
Core or Host runtime source code and does not grant rights to use SPS names,
logos, official badges, or Registry operations.

## Publishing

Only the SPS release pipeline may add a signed release. Do not add, replace, or
edit a package, release record, or `registry.json` manually. Never commit
private signing keys, credentials, logs, or customer data.
