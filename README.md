# FantasticMC

**A companion client for Minecraft: Bedrock Edition on Android.** Floating in-game HUD, pack import, skin editor and a customizable home screen, all in one app.

![Android](https://img.shields.io/badge/Android-10%2B-3DDC84?logo=android&logoColor=white)
![ABI](https://img.shields.io/badge/ABI-arm64--v8a-blue)
![Version](https://img.shields.io/badge/version-0.53-1E90FF)
![Status](https://img.shields.io/badge/status-preview-orange)

> **Not an official Minecraft product. Not approved by or associated with Mojang or Microsoft.**
> FantasticMC does not include Minecraft. You need your own legitimate copy of Minecraft: Bedrock Edition.

---

## Features

- **Gameplay HUD**: floating widgets on top of Minecraft (FPS, keystrokes, CPS and more). Drag them around with the built-in HUD editor.
- **HUD presets**: Minimal, Explorer, Survival and Builder layouts, plus per-widget opacity, size, color, outline and shape.
- **Pack import**: import `.mcpack` and `.mcaddon` files.
- **Skin editor**: upload a 64×64 or 64×32 PNG, switch Classic/Slim models, load skins by username and save multiple skins.
- **Servers list**: save servers and copy their IP quickly.
- **Customization**: themes, backgrounds, UI scale and profile picture.
- **Built-in game (experimental)**: run your own imported Minecraft APK (arm64) inside FantasticMC.
- **Device info and logs**: frame-rate graph, RAM/storage stats and a copyable debug log for bug reports.

## Download

Grab the latest APK from the [**Releases**](../../releases/latest) page.

1. Download `FantasticMC-v0.53.apk`.
2. Open it on your phone. Android will ask you to allow installs from your browser or file manager; allow it for this install.
3. Open **FantasticMC**, then go to **Settings** and grant the permissions you want (see below).
4. Press **START** to launch Minecraft with the HUD on top.

**Verify your download (optional):**

```bash
sha256sum FantasticMC-v0.53.apk
# 888f9f4fce98f8383c7ce19160104a04c4612c827a711250e28d1df544902ee2
```

## Requirements

| | |
|---|---|
| Android | 10 (API 29) or newer |
| CPU | 64-bit ARM (`arm64-v8a`) |
| Game | Minecraft: Bedrock Edition installed (or your own arm64 Minecraft APK for the experimental built-in mode) |
| Orientation | Landscape |

## Permissions

| Permission | Why it is needed |
|---|---|
| Display over other apps (`SYSTEM_ALERT_WINDOW`) | Draws the floating HUD above Minecraft |
| Usage access (`PACKAGE_USAGE_STATS`) | Detects when Minecraft closes so the HUD can hide itself |
| Foreground service / media projection | Keeps the HUD running and supports screen capture features |
| Notifications | Shows the running-service notification |
| Internet | Account sign-in, skin lookup by username, fonts |
| Wake lock, vibrate, network/Wi-Fi state | Keeps the HUD responsive, haptics, connectivity checks |

All of these are optional to grant in Android settings; features that need a missing permission simply won't work.

## Account

Optional sign-in is handled through Firebase Authentication. Skin-by-username lookup contacts third-party skin services (`minotar.net`, `mc-heads.net`) when used.

## Troubleshooting

- **HUD doesn't appear**: enable *Display over other apps* for FantasticMC in Android settings.
- **HUD stays after closing Minecraft**: grant *Usage access* once.
- **"Minecraft Bedrock is not installed"**: install Minecraft first, or import your own APK in *Settings → Built-in game*.
- **Something broke**: open **Settings → Add system log → Copy** and paste the text into a [bug report](../../issues/new?template=bug_report.yml).

## Status

This is an early **preview** build. Expect rough edges, and some home-screen data (for example example servers) is sample data for now.

## Source code

This repository currently distributes the compiled app only. See [LICENSE](LICENSE) for terms.

## Feedback

- Found a bug? [Open an issue](../../issues/new/choose).
- Have an idea? Open a feature request.

## Disclaimer

"Minecraft" is a trademark of Mojang Synergies AB / Microsoft. FantasticMC is an independent project and is not affiliated with, endorsed by, or sponsored by Mojang or Microsoft. Use at your own risk, and only on servers whose rules allow client-side HUDs and overlays.
