# MSTHub

A modular Luau hub with Arvn UI, persistent character effects, an active-feature panel and managed session cleanup.

[Türkçe kullanım](README.tr.md) · [Changelog](CHANGELOG.md) · [Third-party credits](THIRD_PARTY_NOTICES.md)

## Load current distribution

```lua
loadstring(game:HttpGet("https://cdn.jsdelivr.net/gh/Cryvess/MSTHub@main/MSTHub-Arvn.lua"))()
```

This requires an environment providing `loadstring`, `game:HttpGet`, `getgenv` and Drawing APIs. It is not a standalone application or a standard Roblox Studio LocalScript. Availability of individual features depends on the game and runtime.

Press **P** to show or hide the menu. Use **Home → Session → Clean Unload** to stop MSTHub before running the loader again. Hiding the menu does not stop enabled features. When upgrading from a version without Clean Unload, start a fresh game session first.

## Features

- **Movement:** speed, jump, flight, noclip, player teleport, emotes and character effects.
- **Visual:** player/team ESP, fullbright, field of view and third-person camera.
- **Murder Mystery 2:** round-aware ESP, role teleports, gun tools and existing automation controls. Role detection uses client-visible tools; hidden roles are not guaranteed.
- **Valley Prison:** existing game-specific movement and stamina controls.
- **Active Features:** an event-driven list of enabled toggle settings, with a visibility switch. An enabled setting does not guarantee an effect when its required character or target is unavailable.
- **Clean Unload:** stops owned listeners, tasks and render callbacks; removes owned visuals; restores tracked character/camera/lighting properties; permits a fresh load. Teleports and actions already performed cannot be undone.
- **Configuration:** Arvn autosave and legacy Luna configuration import. Settings are saved before shutdown, so saved enabled features may resume when reloading.

UI animations, blur, particles and sounds are disabled by default. The supplied Arvn snapshot is bundled so a UI-library update does not silently change this release. The existing client-side key screen is retained; its key is visible in the source and is not a server authentication system.


## Distribution

This public repository contains the packed distribution. Development sources and tests are maintained separately. Obfuscation is not server-side authentication or a guarantee against source extraction.
