# VR Mod for Halo 2 Vista/Project Cartographer

**An unofficial PC VR mod for Halo 2 Vista / Project Cartographer.**

> **Latest public alpha : [v0.2.0-alpha.3](https://github.com/Rankiseth/halo2-vr/releases#release-v0.2.0-alpha.3) <--- Click here to download the mod**, based on development revision **R99**. See releases.

> Youtube Highlight Footage: [Click here](https://www.youtube.com/watch?v=A6_uVG1LhiM)

Step into Halo 2's campaign AND multiplayer with stereoscopic VR, tracked weapons, physical interactions and manual reloading. Developed and playtested by **Rankiseth**, building on Project Cartographer and Valve OpenVR.

### What’s new in v0.2.0-alpha.3/R99 — Four-Player Co-op Update

**Bring the whole squad!** R98 brings tested **four-player campaign co-op**, improved mission startup and synchronization, and a cleaner way to host and join games—with VR and native desktop players together.

- **Four-player co-op, now playtested:** Successful four-player sessions across multiple missions, including The Great Journey’s opening. Most missions have been reported playable, with some mission-specific quirks.
- **Improved mission startup:** Fixes for starting-state transfer failures that could disconnect guests while loading into campaign.
- **Better Player 3 and 4 spawning:** Extra players can spawn near teammates when authored starting positions are unavailable and normal co-op respawning is allowed.
- **Checkpoint and recovery improvements:** Improved checkpoint reversion and automatic resynchronization for some simulation mismatches while players remain connected.
- **Cleaner Advanced Options:** Separate **Co-op**, **Multiplayer**, and **Setup & help** tabs, expandable instructions, and a compact invite-entry screen. The **Home** shortcut still works.
-  **Co-op Campaign Player Colours:** Player 1 is Chief or Arbiter, Players 2 to 4 adapt a blue, red and gold colour respectively to easily differentiate teammates!

**All your VR interactions remain:** Manual reloads on supported weapons, physical grenade throwing and melee, holsters, two-handed support, and independently aimed dual-wielded weapons in matching private sessions. **F6** switches between VR and native controls.

**Everyone should use R99.** Join the same **Radmin VPN** network—or use **Local LAN**—and start a fresh campaign mission. Existing settings and calibration can be retained.

**Four-player co-op remains experimental.** Some cutscenes, teleports, and vehicle sections still assume two players. Legendary/Iron retain authored starts, and extra Banshees are not included. Older-build checkpoints and mid-mission joining are unsupported; disconnected players must rejoin from the lobby.

## Motivation

I first played Halo CE on the original Xbox as a young pre-teen. Since then, I have always dreamt of truly feeling immersed as the Master Chief after having played Bungie's sequels. Ultimately, Halo 2 became my absolute favourite of the game series. This mod is a love-letter to the fans of the Halo universe, and VR gamers. I hope you enjoy it. :)

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

- A Windows PC and a legitimate Halo 2 Vista installation with the supported [Project Cartographer](https://www.halo2pc.com/) baseline.
- SteamVR / OpenVR and tracked motion controllers. This is a PC VR mod; the headset does not run the game standalone.
- The main playtest setup is **Meta Quest 3 → Virtual Desktop → SteamVR**. Other headsets and controller layouts need wider testing.
- This alpha targets **local single-player campaign**. Multiplayer and co-op are not validated release features.
- Halo 2 in **The Master Chief Collection is not supported** by this build.

## First launch

In your Halo 2 Project Cartographer folder - back up xlive.dll, extract all Win32 ZIP contents beside halo2.exe, start SteamVR, and launch.

Start Virtual Desktop and SteamVR before launching. VR starts automatically by default. **F6** toggles VR, **hold Y** recenters height/orientation, and **F7** is the keyboard recenter fallback. Open **VR Settings → Guide** for the complete control scheme and reload instructions, also available in [the guide](Bindings-and-Reload-Guide.txt). Or you may refer to the [posters](Halo2VR-R47-Quest3-Bindings-Posters.pdf) below:

<img width="2160" height="2880" alt="Halo2VR-R44-01-Ground-Combat" src="https://github.com/user-attachments/assets/44691c50-16cd-433e-b06f-4bb1f44bb271" />

<img width="2160" height="2880" alt="Halo2VR-R44-02-Weapons-and-Holsters" src="https://github.com/user-attachments/assets/c9cda244-63e4-44f2-82b1-46a2eccfc3b1" />

<img width="2160" height="2880" alt="Halo2VR-R44-03-Grenades-and-Melee" src="https://github.com/user-attachments/assets/6f4e6add-a165-4a93-b0dc-a81561cddc01" />

<img width="2160" height="2880" alt="Halo2VR-R44-04-Magazine-Reloads" src="https://github.com/user-attachments/assets/bd370bb9-5127-4f8d-88d2-eff925a235ac" />

<img width="2160" height="2880" alt="Halo2VR-R44-05-Shotgun-and-Heavy-Reloads" src="https://github.com/user-attachments/assets/02d98e9e-2d4e-4147-9494-04fc8f566853" />

<img width="2160" height="2880" alt="Halo2VR-R44-06-Vehicles-and-Turrets" src="https://github.com/user-attachments/assets/a33d31ca-403a-4c42-b328-7e2cf36d4df9" />

<img width="2160" height="2880" alt="Halo2VR-R47-07-Menus-and-Comfort" src="https://github.com/user-attachments/assets/d4f3f9c3-ab2a-4cdb-b037-998cd6e9ebc0" />

## AI Disclosure

This mod was created with the help of AI-assistance.

## Feedback

When reporting a problem, include the release version, mission/checkpoint, headset, runtime/streaming setup, controller layout, and steps to reproduce it. F8 can capture diagnostic views. Check logs for personal paths or account details before posting them publicly. You may also send your crash report in your "halo2_crash_reports" folder, which is held in your "Documents" folder in PC.

The first public alpha is intended to broaden testing across PCs, missions and comfort preferences. Successful testing on the main development setup does not establish compatibility with every system.

## Credits and development

- **Rankiseth** — project direction, gameplay design, tuning and headset testing.
- **Project Cartographer contributors** — the Halo 2 Vista integration on which this build is based.
- **Valve and OpenVR contributors** — VR runtime integration.

## Licence and game content

The Cartographer-based code is subject to GPLv3; the VR integration files are marked GPL-3.0-only. A public binary release must provide its matching complete Corresponding Source and preserve applicable notices. Individual dependencies retain their own licences.

Halo 2 and related characters, assets and marks belong to their respective rights holders. This is an unofficial community project, not endorsed by Microsoft, Halo Studios, Bungie, Valve, Meta or the Project Cartographer team. 
