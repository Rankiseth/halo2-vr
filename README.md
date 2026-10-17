# VR Mod for Halo 2 Vista/Project Cartographer

**An unofficial PC VR mod for Halo 2 Vista / Project Cartographer.**

> **First public alpha in preparation: v0.1.0-alpha.1**, based on development revision **R44**. No playable download has been published yet. Release packaging and audio/code provenance checks are in progress.

Step into Halo 2's campaign with stereoscopic VR, tracked weapons, physical interactions and manual reloading. Developed and playtested by **Rankiseth**, building on Project Cartographer and Valve OpenVR.

## Features

- Stereoscopic gameplay, menus and cutscenes, with controller pointers for menu interaction.
- Tracked weapon aiming, two-handed support, hand transfers and dual wielding with independent weapon reticles.
- Grip-based weapon handling, hip and shoulder holsters, and left-handed controls.
- Physical grenade throwing and swing-based melee, including Energy Sword gestures.
- Weapon-specific manual reloads: magazine insertion, charging handles, the Magnum slide, Shotgun pumping, and Rocket Launcher / Brute Shot loading.
- Adjustable recoil and controller haptics.
- First-person vehicle and turret views, adjustable camera positions and a third-person option.
- Snap or smooth turning, recentering, adjustable world scale, HUD size/distance and scope settings.
- Categorized VR settings, a bindings/reloading guide and a desktop eye mirror for recording.
- Adjustable manual reload volume from 0–200%.

## Requirements and scope

- A Windows PC and a legitimate Halo 2 Vista installation with the supported Project Cartographer baseline.
- SteamVR / OpenVR and tracked motion controllers. This is a PC VR mod; the headset does not run the game standalone.
- The main playtest setup is **Meta Quest 3 → Virtual Desktop → SteamVR**. Other headsets and controller layouts need wider testing.
- This alpha targets **local single-player campaign**. Multiplayer and co-op are not validated release features.
- Halo 2 in **The Master Chief Collection is not supported** by this build.

The development build uses the pinned Cartographer 0.7.4.3 source. Its existing Prepare tool accepts the specific tested Cartographer 0.7.4.2 installation and Halo 2 executable 1.0.0.11122. The final installer must identify this compatibility clearly; arbitrary Cartographer versions are not interchangeable.

## First launch

The public player ZIP and final installation instructions will be attached after release preparation. The existing R44 source playtest uses **Build-R3 → Prepare-R3 → Run-R3**, creating a separate game copy. Players of the planned compiled release will not need Visual Studio.

Start Virtual Desktop and SteamVR before launching. VR starts automatically by default. **F6** toggles VR, **hold Y** recenters height/orientation, and **F7** is the keyboard recenter fallback. Open **VR Settings → Guide** for the complete control scheme and reload instructions, also available in [the guide](docs/Bindings-and-Reload-Guide.txt).

## Feedback

When reporting a problem, include the release version, mission/checkpoint, headset, runtime/streaming setup, controller layout, and steps to reproduce it. F8 can capture diagnostic views. Check logs for personal paths or account details before posting them publicly.

The first public alpha is intended to broaden testing across PCs, missions and comfort preferences. Successful testing on the main development setup does not establish compatibility with every system.

## Credits and development

- **Rankiseth** — project direction, gameplay design, tuning and headset testing.
- **Project Cartographer contributors** — the Halo 2 Vista integration on which this build is based.
- **Valve and OpenVR contributors** — VR runtime integration.

## Licence and game content

The Cartographer-based code is subject to GPLv3; the VR integration files are marked GPL-3.0-only. A public binary release must provide its matching complete Corresponding Source and preserve applicable notices. Individual dependencies retain their own licences.

Halo 2 and related characters, assets and marks belong to their respective rights holders. This is an unofficial community project, not endorsed by Microsoft, Halo Studios, Bungie, Valve, Meta or the Project Cartographer team. 
