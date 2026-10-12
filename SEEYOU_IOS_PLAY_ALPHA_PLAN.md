# SeeYouIOS Play — Private Alpha

**Dedicated native iOS game-library prototype. Work in progress; NOT publicly released.**

This is an isolated feature branch for initial project planning. The existing seeyoustore website remains untouched on `main`.

## Confirmed architecture

- Native SwiftUI (Sorani Kurdish/RTL), admin catalog and metadata API.
- iPhone downloads **directly from an authorized HTTPS CDN/origin**. The VPS sends only lightweight catalog metadata, never proxies multi-gigabyte downloads.
- Pause/resume, size/SHA-256 checks, space checks and staged local ZIP extraction.
- A downloaded ZIP is **not** an iOS executable runtime. Play is disabled until a compatible signed runtime exists and is tested.
- GTA V game/data rights must be established independently; a third-party GoFile link is not distribution authorization.
- Multiplayer must be proven separately; do not describe generic multiplayer as iOS FiveM.

## Verification performed

- Python FastAPI API scaffold and HTML admin dashboard developed locally.
- 8/8 automated API authorization/catalog tests passing.
- Swift files syntax-parsed; **not yet built or tested on real iPhone**.
- GoFile link `https://gofile.io/d/pA901JJr` provided but its archive contents could not be accessed or verified through available inspection tools.
- Connected MacBookPro reports Intel x86_64/Xcode 26.5; upstream Muguet documents Apple Silicon requirement.

## Next engineering gates

1. Place the source package in a **dedicated** `SeeYouIOS-Aso/seeyouios-play` repository, not the production website branch.
2. Full Xcode QA with authorized tiny demo archive and dedicated test iPhone.
3. Persist download state and bind background URLSession completion/relaunch correctly.
4. Review runtime feasibility, hardware memory limits and written distribution rights.
5. Publish no gameplay/runtime promises until the above gates pass.

**No Store templates, live bots, VPS services, or production deployments are changed by this branch.**
