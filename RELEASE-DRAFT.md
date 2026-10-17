# Rankiseth VR for Halo 2 — Public Alpha 0.1.0

Proposed tag: `v0.1.0-alpha.1`  
Development baseline: `R37`  
GitHub release status: **Draft / prerelease**

This first public alpha brings Halo 2 Vista's campaign into PC VR through Project Cartographer and SteamVR.

Aim tracked weapons, use hip and shoulder holsters, support a rifle with both hands, dual wield, throw grenades physically, and reload each weapon by hand. The build also includes VR menus and cutscenes, vehicle/turret camera options, weapon-specific reticles, configurable comfort settings and an in-headset guide.

The primary tested setup is Meta Quest 3 with Virtual Desktop and SteamVR. The current scope is local single-player campaign; this is not an MCC mod or a standalone Quest APK. Broader hardware, mission and controller testing is the purpose of the alpha.

## Planned downloads

| File | Purpose |
| --- | --- |
| `Halo2VR-v0.1.0-alpha.1-win32.zip` | Compiled mod, support files, installation instructions and licence notices for players. |
| `Halo2VR-v0.1.0-alpha.1-source.zip` | Complete matching source, patches and build/install scripts. |
| `SHA256SUMS.txt` | Hashes of the final release archives. |

These are proposed asset names, not existing downloads. This draft package contains no compiled game mod and no game installation.

## Controls and settings

VR starts automatically by default; F6 toggles VR. Hold Y to recenter. The VR Settings menu includes Basic, Comfort, HUD & Menus, Weapons, Vehicles, Audio & Feedback, Graphics, All Settings, Guide and About. Use the Guide for physical reload steps and handedness-specific bindings.

The R37 baseline includes raw reload cue mappings and a 0–200% reload-volume control, defaulting to 100%. Public audio packaging remains subject to the asset review in the maintainer notes.

## Credits

Project direction and headset testing: **Rankiseth**. Built on Project Cartographer and Valve OpenVR, with inspiration and reference work from LivingFray's HaloCEVR. Development and documentation used OpenAI ChatGPT/Codex assistance, with direction, review and headset testing by Rankiseth.

This is an unofficial community modification. Halo 2 belongs to its respective rights holders. No affiliation or endorsement is claimed.

## Before publishing this draft

Resolve the checks in `MAINTAINER-RELEASE-NOTES.md`, supply the final tested Windows binaries and matching source, confirm the artwork/audio permissions or replace those assets, and replace the planned-download section with actual release links. Keep the release marked as a prerelease.
