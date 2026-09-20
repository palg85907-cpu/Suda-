# Suda 2.0

Offline nearby communication app using Google Nearby Connections.

### Added in 2.0
- Multi-hop relay (up to 5 hops) using message IDs + relay TTL.
- Photo/video/document/file transfer with Nearby FILE payloads.
- Hindi / English switch using Android AppCompat locales.
- Auto-connect: starts advertising + discovery automatically after permissions; asks Android to turn Bluetooth on when needed.
- Suda logo from the supplied logo image.
- Phone-friendly GitHub Actions APK build.

### Important
- Both phones need Suda installed for Suda chat/relay/file-transfer protocol.
- Android does not allow an app to silently enable Bluetooth; Suda uses the system Bluetooth-enable confirmation.
- Multi-hop is implemented at the Suda application layer; Google Nearby's P2P_CLUSTER alone is not a mesh router.


## Suda 2.1 Dynamic Multi-Hop Relay
- No app-level fixed hop-count limit.
- Relay uses a 10-minute message TTL to prevent endless circulation.
- Duplicate message IDs prevent relay loops.
- The number of simultaneous connections remains subject to Android/Nearby Connections and phone hardware limits.
