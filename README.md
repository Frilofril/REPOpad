# R.E.P.O. Custom Soundboard

A mod for R.E.P.O. that adds a custom soundboard: play `.wav` and `.mp3` sounds and broadcast them directly through the in-game microphone!

### Features:
- Open the menu with the **F6** key (or assign your own key in the settings).
- Broadcast sounds to other players via voice chat.
- Easily add your own files using the **Open Sounds Folder** button.
- Customizable key to instantly stop sound playback.

### Technical Overview
- [Thunderstore](https://thunderstore.io/c/repo/p/FriloFril_Team/REPOpad/).
- Language & Target: C# (.NET Framework 4.7.2) | BepInEx Plugin Architecture.
- Network & Audio Pipeline: Integrates with **Photon Voice (`Photon.Voice.Unity`)** by dynamically switching the active `Recorder` input source between hardware microphone and custom `AudioClip` buffers with sample-level volume scaling.
- Asynchronous I/O & Persistence: Uses `UnityWebRequestMultimedia` coroutines for non-blocking `.wav`/`.mp3` loading and `BepInEx.Configuration` for persistent per-track keybinds and volume states.
- UI: Custom in-game overlay built with `UnityEngine.IMGUI`.
