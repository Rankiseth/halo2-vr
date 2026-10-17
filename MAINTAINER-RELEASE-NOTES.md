# Release preparation notes — R37 → v0.1.0-alpha.1

Prepared 17 October 2026 UTC. This is a technical/licensing review, not a legal opinion or a completed public release.

## 1. Source availability

R37 compiles its VR module into a modified Project Cartographer `xlive.dll`. The pinned source is `pnill/cartographer` commit `269d75483dea1b7ec7f7061d334ef113491e9131` (0.7.4.3). The local GPLv3 licence and third-party notice confirm this basis. A binary-only player ZIP is possible, provided the same release gives equivalent access to the matching complete Corresponding Source. Closing the derived source is not permitted by the present GPL terms. An exception would require the relevant rights holders' permission.

Provide the exact modified upstream tree, integration sources, patches, build/install scripts and required non-system dependency source/notices. R37's small source ZIP is a development kit that downloads upstream; it has not been certified as a self-contained Corresponding Source release. Preserve the exact revision and ensure all required source remains obtainable. A README linking only to unmodified upstream is insufficient.

Preserve upstream authorship and applicable third-party notices. Do not apply a new proprietary licence or a blanket noncommercial restriction to the GPL code. Separate artwork/game-asset conditions from software licensing.

## 2. Proposed player ZIP inventory

Paths are relative to the runtime game directory unless specified. This is an inventory, not an instruction to ZIP the existing `test-game` folder.

| File / directory | Source and purpose |
| --- | --- |
| `xlive.dll` | The final tested x86 R37-based build, not a stock Cartographer DLL. |
| `openvr_api.dll` | The matching official x86 OpenVR loader from the build output; include its BSD-3-Clause notice. |
| `cartographer-vr.ini` | Clean baseline defaults; preserve existing user settings during updates. |
| `vr-bindings/actions.json` | OpenVR action manifest. |
| `vr-bindings/quest_touch.json` | Quest controller bindings. |
| `vr-branding/halo2vr.vrmanifest` | App registration; the installer must generate correct paths for the player's installation. |
| `vr-branding/halo2vr-r25.png` | Current app image path; replace/clear the artwork before public distribution. |
| `vr-reload-audio/` | R37 expects 24 WAV cues. Resolve redistribution rights or replace with approved/local-game-derived playback. Include accurate provenance for distributed assets. |
| Installer or setup instructions | Baseline validation, backups, config preservation, app-manifest generation and launch working directory. |
| `README`, controls/reload guide, changelog | Player instructions and known scope/limits. |
| `LICENSE`, updated `THIRD_PARTY_NOTICES`, dependency notices, source link | Required code notices and clear access to corresponding source. |

Do not upload `halo2.exe`, maps, original game DLLs/assets, product keys, saves, accounts, diagnostics, personal paths, or the whole `test-game` directory. Existing game/runtime dependencies should be prerequisites unless their redistribution terms have been checked. Check the final DLL's imports on Windows to catch any missing permitted runtime dependency; no compiled DLL was available in this workspace for that check.

The existing Prepare tool requires the tested original Cartographer 0.7.4.2 DLL and Halo 2 executable 1.0.0.11122 by hash, while the modified source is based on 0.7.4.3. Keep this distinction explicit. The present Run tool also expects `out/`, a test-copy marker, and the R37 DLL marker. Simply shipping the two DLLs with the old launcher is not a finished end-user installer.

## 3. Game audio and artwork

The R37 bank contains 23 cues prepared from supplied game WAVs plus one retained video-derived Fuel Rod cue. Rankiseth identified [The Sounds Resource — Halo 2](https://sounds.spriters-resource.com/xbox/halo2/) as the source of the supplied raw WAVs. This records the user-provided origin; individual archive downloads have not been matched byte-for-byte. The retained Fuel Rod clip still has its separate video provenance.

The archive's [Help page](https://sounds.spriters-resource.com/page/help/) encourages completely free fan projects, but says the site does not own or license the game assets and has not obtained publisher permission to host them. Its [Terms of Use](https://sounds.spriters-resource.com/page/tou/) also restrict commercial uses. Archive attribution therefore does not establish a rights-holder grant for public distribution. These recordings are separate from the GPL software. Resolve rights, use licensed replacements, or implement and test a local-game audio path; local extraction is not itself legal clearance.

The GitHub description and this draft package now omit the banner, as requested. The existing R37 SteamVR app image is a separate runtime asset and still needs a public-release branding decision. Microsoft's fan rules restrict using game logos in an item's logo. A disclaimer alone does not clear that use. Consider distinct original project branding with plain compatibility wording, or obtain the necessary permission. Free distribution alone does not settle asset/EULA issues.

## 4. HaloCEVR provenance check

R37's third-party notice records adapted reload segmentation/corruption checks and workflow from the supplied HaloCEVR R1.35 fork. That archive's licence-file inventory shows only a third-party MinHook licence; no top-level HaloCEVR licence was located. Its build notes say a licence was retained, but that claim is not backed by a top-level licence file in the inspected ZIP. The current public upstream page also does not display a recognised project licence.

Trace the exact reused code to its author/version: distinguish newly written fork code from copied LivingFray code. Obtain/verify a compatible permission for any copied code lacking a grant, or replace it with an independently developed implementation. General encouragement to make free mods and attribution alone are not substitutes for a redistribution grant. This audit has not established that every adapted line needs separate permission; it has identified an unresolved provenance question.

## 5. Notices and release validation

- Update `THIRD_PARTY_NOTICES.txt`: it still describes 21 video-extracted cues from R30.1; R37 now has 23 raw cues plus the retained Fuel Rod cue.
- Retain Valve's complete OpenVR notice and all notices for incorporated Cartographer dependencies, including their required source obligations where applicable.
- Preserve GPL notices and record the changes/version. Use Rankiseth for public project credit without deleting upstream credits.
- Build the final x86 DLL on Windows and record its hash and source revision. R37 portable tests are not a Windows build or a release-package install test.
- Test the compiled archive on a clean copy of the supported game without Visual Studio or developer folders: install, launch, bindings, manifest paths, reload sounds/volume, saved settings and uninstall/rollback.
- Publish the player ZIP and complete corresponding source together, and mark the GitHub release as a prerelease. Keep the internal R37 identifier in diagnostics.

## 6. AI assistance

Suggested disclosure: “Development and documentation used OpenAI ChatGPT/Codex assistance. Rankiseth directed, reviewed and playtested the project.” This is a development credit, not a claim that OpenAI owns or endorses the mod. OpenAI's terms allocate output rights between user and OpenAI, but do not override third-party licences or IP. They prohibit misrepresenting generated output as human-generated; the publication policy also calls for disclosure in the sharing/publishing situations it covers. This review does not establish a universal GitHub source-code labelling law.

## References checked

- [The Sounds Resource Help](https://sounds.spriters-resource.com/page/help/) and [Terms of Use](https://sounds.spriters-resource.com/page/tou/). Rankiseth supplied the Halo 2 archive URL; the game listing itself returned HTTP 403 during this review.

- [Project Cartographer](https://github.com/pnill/cartographer) and this build's `LICENSE`, `UPSTREAM-PIN.json`, `THIRD_PARTY_NOTICES.txt`.
- [GNU GPL FAQ: source and binaries](https://www.gnu.org/licenses/gpl-faq.en.html#SourceAndBinaryOnDifferentSites) and [modified binary source](https://www.gnu.org/licenses/gpl-faq.en.html#DistributeExtendedBinary).
- [Microsoft Game Content Usage Rules](https://www.xbox.com/en-US/developers/rules).
- [Microsoft Trademark and Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks).
- [HaloCEVR upstream](https://github.com/LivingFray/HaloCEVR) and the supplied `HaloCEVR-Stylish-Restart-R1.35-Source(2).zip`.
- [GitHub: licensing a repository](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository).
- [OpenAI Terms of Use](https://openai.com/policies/terms-of-use/) and [Sharing & Publication Policy](https://openai.com/policies/sharing-publication-policy/).
- [Semantic Versioning](https://semver.org/) for the proposed initial-development / prerelease naming convention.
