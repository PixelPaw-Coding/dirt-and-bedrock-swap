# Dirt ↔ Bedrock — Universal Java Texture Swap

Flip the ground and flip the rules. This pack swaps **dirt** with **bedrock** and **bedrock** with **dirt** — pure texture swap, no models, no sounds, just a visually broken world.

---

## What it does  
- Replaces the `dirt` block texture with the `bedrock` texture.  
- Replaces the `bedrock` block texture with the `dirt` texture.  
- Minimal, tiny, instant chaos: mines behave the same, visuals lie to you.

---

## Features
- Single-purpose: dirt ↔ bedrock texture swap.  
- Lightweight — only two textures changed.  
- Works across Java versions when you pick the correct `pack_format` file.  
- Safe for singleplayer and servers (textures only).

---

## Pack formats (Java Edition)
| pack_format | Minecraft versions supported |
|-------------:|------------------------------|
| 1  | 1.6.1 – 1.8.9 |
| 2  | 1.9 – 1.10.2 |
| 3  | 1.11 – 1.12.2 |
| 4  | 1.13 – 1.14.4 |
| 5  | 1.15 – 1.16.1 |
| 6  | 1.16.2 – 1.16.5 |
| 7  | 1.17 – 1.17.1 |
| 8  | 1.18 – 1.18.1 |
| 9  | 1.18.2 |
| 10 | 1.19 – 1.19.3 |
| 11 | 1.19.4 |
| 12 | 1.20 – 1.20.2 |
| 13 | 1.21 – 1.21.1 |
| 14 | 1.21.2 – 1.21.3 |
| 15 | 1.21.4 – 1.21.5 |
| 16 | 1.21.6 – 1.21.7 |
| 17 | 1.21.8 – 1.21.9 |
| 18 | 1.21.10 |

> Pick the `.zip` that matches the Minecraft version(s) you want to support. Each `.zip` uses the corresponding `pack_format in its pack.mcmeta`.

---

## Folder structure (what to include)
```
DirtBedrockSwap/
├─ pack.mcmeta
└─ assets/
   └─ minecraft/
      └─ textures/
         └─ block/
            ├─ dirt.png      <-- put the bedrock design here
            └─ bedrock.png   <-- put the dirt design here
```

`pack.mcmeta` example (for pack_format 14):
```json
{
  "pack": {
    "pack_format": 14,
    "description": "Dirt ↔ Bedrock — texture swap"
  }
}
```

---

## Installation (Java)
1. Download the `.zip` matching your Minecraft version range.  
2. Move the `.zip` to your `resourcepacks` folder (`%appdata%\.minecraft\resourcepacks\` on Windows).  
3. Open Minecraft → Options → Resource Packs → enable the pack.  
4. Enter world. The textures are swapped immediately.

**For very old versions (pre-1.6.1 / Alpha / Classic):** those use `terrain.png` inside the client `.jar`. Provide a `terrain.png` variant (16×16 sheet) for those versions and instruct users to replace the file inside the version `.jar` (manual install).

---

## Notes & compatibility
- Loading warnings are normal if your `pack_format` is newer than the client; textures still usually work.  
- This is visual-only. Block behavior (blast resistance, breakability) is unchanged.  
- Bedrock Edition is not supported by this Java pack — Bedrock uses a different format and manifest.  
- If you want wide compatibility, produce multiple `.zip`s with different `pack_format` values and bundle them in a single release.

---

## Credits & license
- Created by PixelPaw P..  
- Licensed under MIT License

---

## Quick dev note
If you only want one file that *most people* can use today: build for the latest Java `pack_format` you target (e.g., `14–18` for modern 1.21.x builds) and publish older `pack_format` zips separately for legacy installs.
