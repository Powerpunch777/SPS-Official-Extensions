# SPS Official Extensions

SPS is Redon's local-first Desktop workspace, where plugins add the workflow a project needs. This repository distributes the signed index and immutable release records for SPS-published extensions; it is the package channel, not the Desktop application or Core runtime.

## Registry contents

The signed `registry.json` identifies the Registry, publisher key, and available plugin releases. SPS Desktop verifies the Registry signature, release-record signatures, and artifact size and SHA-256 before staging a package.

The current index lists `local.room-chat` version `0.3.83`. A Desktop development candidate may include a different bundled extension version; use the candidate's support matrix and the release record for the exact package and Host tuple you intend to use.

Registry data describes packages and their integrity. It does not install, enable, or execute a plugin. The SPS Host reviews compatibility and performs explicit lifecycle actions for the target Workspace.

## Publishing

Only the SPS release process may add a signed extension release. Do not hand-edit `registry.json`, replace an artifact, or alter an immutable release record. Never publish Registry or Publisher private keys, credentials, workspace data, invitations, or diagnostic logs.

Plugin developers can create and inspect packages with the public [SPS Plugin SDK](https://github.com/Powerpunch777/sps-plugin-sdk). For the SPS product and its beta status, see [redongames.com/sps](https://redongames.com/sps/).
