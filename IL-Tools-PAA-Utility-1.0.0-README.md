# IL Tools PAA Utility 1.0.0

Drag-and-drop texture converter for Operation Flashpoint / Arma: Cold War Assault Remastered.

**File:** `IL-Tools-PAA-Utility-1.0.0.exe`  
**Version:** 1.0.0  
**Date:** 25 Sep 2026  
**Project:** https://github.com/Ironlion1970/IL-Tools-PAA-Utility

Sister tools:

- Pack / unpack: [IL Tools PBO Utility](https://github.com/Ironlion1970/IL-Tools-PBO-Utility/releases)
- Models: [IL Tools Arma CWA Blender Plugin](https://github.com/Ironlion1970/IL-Tools-ARMA-CWA-Addon-Blender-Plugin)

---

## What it does

| Drop | Writes next to the source |
|---|---|
| `.png` `.jpg` `.tga` | `.paa` (OFP DXT1 if opaque, DXT5 if alpha, with mipmaps) |
| `.paa` `.pac` | `.png` |

Non–power-of-two images are resized to the next power of two (minimum 4).

---

## How to use

1. Run `IL-Tools-PAA-Utility-1.0.0.exe`
2. Drop a texture, several files, or a folder
3. Click **Convert**

Or drop files onto the EXE in Explorer.

Pipeline with the other IL Tools:

1. Paint `barrel.png` in Blender
2. Convert → `barrel.paa`
3. In the Blender plugin, material name stays `YourAddon\barrel.paa`
4. Pack the folder with PBO Utility (prefix blank, Cprs off)

---

## Command line

```
IL-Tools-PAA-Utility-1.0.0.exe
IL-Tools-PAA-Utility-1.0.0.exe barrel.png
IL-Tools-PAA-Utility-1.0.0.exe convert C:\Work\textures
```

---

## Notes

- Leave this tool for textures only. It does not pack a `.pbo`.
- Pal2PacE output is still the BIS reference. This writes the same OFP header layout used by ILCTI addons (`0xFF01` / `0xFF05`, `AVGCTAGG`, `OFFSTAGG`).
- `.paa` types `0x4444` and `0x8080` decode when possible; new files are written as DXT.
- Windows SmartScreen may warn on an unsigned EXE: **More info → Run anyway**.

## Support

- Bugs: https://github.com/Ironlion1970/IL-Tools-PAA-Utility/issues
- Questions: https://github.com/Ironlion1970/IL-Tools-PAA-Utility/discussions
