# Relay73 for iOS

The iPhone application for **Relay73**, a modular amateur-radio messaging and data platform.

> **Status:** Repository scaffold. Existing iOS application work is maintained in the Relay73 development workspace and has not yet been migrated into this repository.

## Scope

- Compose and manage messages, including Winlink email workflows.
- Configure callsign, station selection, and connection settings.
- Operate a supported modem through an iPhone-compatible radio interface.
- Show connection, audio, PTT, message, and diagnostic status.
- Make modem support modular rather than coupling the interface to one transport.

## Current development direction

The existing prototype uses .NET MAUI, an embedded Pat backend for Winlink workflows, upstream Modem73 for RF transport, and Digirig Lite audio/PTT integration. The iOS bundle identifier is `org.w4car.relay73`.

These are descriptions of ongoing development, not promises of currently available features in this empty repository.

## Integration boundaries

- The app owns the user experience, configuration, and platform-specific hardware handling.
- Pat handles Winlink-related application protocols.
- Upstream modem implementations own their own RF protocol behavior.
- Platform glue stays in Relay73-owned adapters so upstream modem updates remain manageable.

For shared modem integration work, see [relay73-modem-adapters](https://github.com/Relay73/relay73-modem-adapters). For the Windows RMS side, see [relay73-gateway](https://github.com/Relay73/relay73-gateway).

## Initial milestones

1. Migrate the current iOS project while preserving its build history and signing settings.
2. Document build, install, radio, and attended test procedures.
3. Validate message transfer with compatible gateway software.
4. Expand supported modem options through stable integration interfaces.

## Build instructions

Build commands and prerequisites will be documented when the existing project is migrated. No downloadable iOS build is currently published from this repository.

## Project hub

[Relay73 project overview](https://github.com/Relay73/Relay73)

License and contribution instructions are pending. Follow local radio regulations and use an authorized station for on-air operation.
