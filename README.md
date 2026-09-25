# IL-Tools-PAA-Utility-1.0.0
Drag-and-drop texture converter for Arma: Cold War Assault Remastered/Resistance.

**File:** `IL-Tools-PAA-Utility-1.0.0.exe`  
**Version:** 1.0.0  
**Date:** 25 Sep 2026  

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
