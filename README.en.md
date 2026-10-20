# qnid

<p align="center"><img src="assets/qnid-icon.png" width="160" alt="qnid"></p>

[Русский](README.md) | **English**

**qnid is the new name of DirectDrop (working title).** It is the same app, with a new icon and continued device compatibility.

**Send files between your phone and computer — simply and directly.**

qnid lets you send photos, videos, documents, and other files between
devices over a local network or the internet. Files travel directly between
devices, without being uploaded to an intermediate server or requiring a qnid account.

**All files transferred over the internet are protected by end-to-end WebRTC/DTLS encryption.**
Data is encrypted on the sending device and decrypted on the receiving device.
Encryption is enabled automatically for internet transfers.

**[Download qnid for Windows](https://github.com/Kamradi/qnid/releases/latest)**

## Coming soon to iOS and Android

**qnid apps for iOS and Android** are in development. All three versions —
**iOS, Android, and Windows — will be fully compatible with one another**.
You will be able to send files from iPhone to Android, from your phone to your
computer, and back, using qnid on each device.

| Platform | Availability |
| --- | --- |
| Windows x64 | [Available to download](https://github.com/Kamradi/qnid/releases/latest) |
| iOS | Coming soon |
| Android | Coming soon |

The mobile apps will be released later. Download links will be added here when they are available.

## What you can do with qnid

- Move photos and videos from your phone to your computer in their original quality.
- Send documents and other files from your computer to your phone.
- Share files between nearby devices or over the internet.

## Windows features

- Local network device discovery and file transfers in both directions.
- Internet connections using an invitation link and a reply link.
- **Encryption for every file transferred over the internet** (WebRTC/DTLS), with a device verification code.
- File acceptance prompts, transfer progress, and transfer speed indicators.
- A configurable download folder and a button to open it after receiving files.
- Light and dark themes that follow your Windows settings.
- Russian, English, French, and Spanish, with manual or automatic language selection.
- System tray support, notifications, and an optional launch-at-login setting.
- Update checks and installation from within the app.

Transfers to a mobile device require a compatible version of qnid.
The public iOS and Android apps are still being prepared for release.

## Installing on Windows

1. Open the [latest release](https://github.com/Kamradi/qnid/releases/latest).
2. Under **Assets**, download **qnid-…-win-x64.zip**.
3. Extract the archive into a folder you can write to, then run **qnid.exe**.

You do not need to install .NET separately. Internet connections require
**Microsoft Edge WebView2 Runtime**. The x64 build is intended for computers
with Intel/AMD processors.

## Interface language

Version 0.5.0 supports **Русский, English, Français and Español**.
Choose **Settings → Interface language**, use **Exit** in the tray menu,
then reopen qnid. Closing the main window only hides it in the tray.
The default follows Windows; unsupported system languages fall back to English.

## How file transfers work

Devices discover each other automatically on a local network. To connect over
the internet, exchange an invitation and a reply, then compare the verification code.

Internet mode uses a direct connection and **STUN only**.
TURN and server-based file relaying are not used. Some networks and NAT
configurations prevent a direct connection from being established.

## Moving from DirectDrop (working title)

**qnid 0.6.0** continues DirectDrop (working title) under a new name. In your existing app,
open **Settings → Check for updates**. The migration package is signed with the same key.
Your settings, language preference, and download folder are preserved.
The old executable name is retained on upgraded installations to preserve shortcuts
and startup registration; the app itself displays **qnid** and the new icon.

For a fresh installation, choose **qnid-…-win-x64.zip** and run **qnid.exe**.
The **DirectDrop-…-win-x64.zip** (filename retained from the working title) packages and `update-win-x64.json` metadata support
older updaters. The new client uses `update-qnid-win-x64.json`.
Legacy network identifiers are retained for compatibility and do not indicate
that you are running an old app version.

## Updates

Starting with version 0.4.0, open **Settings → Check for updates**
(**Настройки → Проверить обновления** if you use the Russian interface).
The startup check notifies you of a new version; downloading and installing
require your action. Finish any transfers and disconnect the device before installing.
The in-app update from **0.4.0 to 0.4.1** has been successfully tested on Windows.

The app verifies an RSA-3072 signature on the update metadata and the package's
SHA-256 hash. Settings and received files are preserved. If the new version fails
to start, the updater is designed to restore the previous executable; this recovery
scenario has not yet been tested separately.
Users of version 0.3.x must install their first update-capable release manually.

A Windows Authenticode certificate is not yet available. The update signature is
verified within qnid and does not replace a Windows publisher certificate.

## Source code and licenses

This repository distributes ready-to-use builds and release descriptions.
**qnid's source code is closed.** All rights to qnid are reserved.
Third-party licenses are included in the archive and can also be viewed in the app's settings.

The **Source code** archives generated automatically by GitHub contain only this
repository's public files, not the application's source code.
