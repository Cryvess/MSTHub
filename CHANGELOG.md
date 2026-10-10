# Changelog

## 1.1.0

- Add an Active Features widget that updates on toggle changes without a new polling loop.
- Add Home → Session → Clean Unload and connect the built-in eject action to the same cleanup.
- Stop MSTHub-owned connections, yielding tasks and render bindings during unload.
- Remove owned effects and drawings, stop emotes and restore tracked reversible properties.
- Preserve configuration before shutdown and release the session guard to allow reloading.
- Restore original speed/jump and noclip collision values when disabled.
- Restore fullbright values safely, including the original fog distance.
- Replace repeated Anti-AFK listener registration and heartbeat polling with one idle listener.
- Retain the previous MM2 round refresh, persistent headless/right-leg effects and role teleports.
- Add lifecycle tests, reproducible bundle generation and continuous validation.
