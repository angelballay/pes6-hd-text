# PES6 HD Text

**The first PES 6 mod that makes the game's text sharp in HD: same fonts, same layout, and it works with any patch.**

A Kitserver 6 module for Pro Evolution Soccer 6 (PC) by **pitycharly**. Version 1.0.

**[⬇ Download PES6 HD Text 1.0](https://github.com/angelballay/pes6-hd-text/releases/latest)** · [Install](#install) · [Compatibility](#compatibility) · [Known limitations](#known-limitations) · [Español](#español)

## Before / after

| Before | After |
|---|---|
| ![Before](images/before.png) | ![After](images/after.png) |

## What it does

- Menus, player names, team names and titles are drawn **sharp** instead of blurry and stretched.
- **Same fonts, same positions:** nothing moves, nothing gets cut, and the original PES 6 style stays.
- **Works with whatever font your patch uses.** PES 6 The Den Patch 2026 ships its own font and gets sharp too.
- **No settings and no files written.** Drop it in, add one line to `kload.cfg`, play.

## How it works

PES 6 draws its text with tiny 16 px bitmap fonts, and the GPU stretches them to your resolution. That is why text looks blurry on modern screens. Simply using bigger fonts breaks the layout, because the game calculates every position from the original font sizes.

PES6 HD Text doesn't touch the fonts at all:

1. The game builds each piece of text exactly as it always did, with its original fonts and sizes.
2. When the game turns that text into a Direct3D texture, the module hands over a **copy at twice the resolution**. The upscale is edge-aware: the shape of each letter comes from the alpha channel with a threshold, and the colours come from the original palette. That covers outlines and the 256-colour letters of the big titles.
3. PES 6 maps textures by the image size, so the sharper copy lands in **exactly the same rectangle** on screen.

The game recreates many of these textures over and over, so the upscaled copies are cached and menus stay smooth.

## Install

Requires **Kitserver 6**. Don't have it yet? [Kitserver 6](https://www.mediafire.com/file/ljbcnczm893g1b6/kitserver.rar/file)

1. Download `PES6_HD_Text_v1.0.zip` from [Releases](https://github.com/angelballay/pes6-hd-text/releases/latest) and copy `pes6_hd_text.dll` into your Kitserver folder (the one with `kload.cfg`).
2. Open `kload.cfg` with Notepad and add a line after the last `DLL.N`, using the next number. For example, if your last line is `DLL.25`:
   ```
   DLL.26 = "kitserver\pes6_hd_text.dll"
   ```
3. Increase `DLL.num` by 1 (in the example, `DLL.num = 26` becomes `DLL.num = 27`).
4. Start the game.

**Uninstall:** remove that line, put `DLL.num` back to its previous value and delete the DLL.

## Compatibility

- Tested on the **original PES 6** + Kitserver 6.
- Tested on **PES 6 The Den Patch 2026**, together with its 26 other Kitserver modules, including [Change Physics Game](https://github.com/angelballay/pes6_game_physics_mod).
- Before changing anything, the module checks the game code where it hooks. If your `pes6.exe` is different, it does nothing and the game runs as usual.
- Upscaled copies use at most 32 MB of memory.

## Known limitations

- **Text only.** Graphics that are images stay as they are: the title screen ("Press any button"), logos, icons, menu widgets and the scoreboard numbers (they are part of a texture).
- **Big outlined titles keep the game's original outline,** so letters that overlap slightly in the original still overlap (now sharp).
- **Not a widescreen fix:** the menu layer is still 4:3, stretched to your screen.

Since it only touches text, it should sit nicely next to texture packs and other HD projects.

## FAQ

**Does it change the font?** No. It uses the exact fonts your game or patch already has.

**Will text move or get cut?** No. Every size and position is the game's own; only the texture behind the text is sharper.

**Does it slow the game down?** No noticeable impact. Each text texture is upscaled once and then reused from a cache.

## For patch makers

PES6 HD Text is a plain Kitserver module that runs next to whatever your patch already has. If you want to include it in your patch, go ahead, and let me know if anything conflicts (open an [issue](https://github.com/angelballay/pes6-hd-text/issues)).

## Feedback

Found a screen where the text is still blurry? Open an [issue](https://github.com/angelballay/pes6-hd-text/issues) with a screenshot and the patch you use.

## About the author

I'm **pitycharly**, an Argentine software developer who makes mods for PES 6. I want to help keep this game alive, and I'd love to see my mods inside the patches people already play. I build them as Kitserver modules and keep them compatible with all the existing ones.

My other mod:

- **[Change Physics Game](https://github.com/angelballay/pes6_game_physics_mod)** (v1.1): first-time passes no longer die on the pitch. A faster pass impulse makes the ball roll faster and more smoothly. [Video](https://www.youtube.com/watch?v=KKfPKn4rNsg) · [Download](https://www.mediafire.com/file/fwqcw1omr98uekw/1.1_pes6_game_physics_mod.zip/file)

Both mods are tested on the original PES 6 and on PES 6 The Den Patch 2026.

---

## Español

**El primer mod de PES 6 que pone el texto del juego nítido en HD: mismas fuentes, mismo diseño, y anda con cualquier parche.**

Los menús, los nombres de jugadores y de equipos y los títulos se ven nítidos en lugar de borrosos y estirados. El juego sigue usando sus fuentes y sus posiciones; el módulo solo le pasa a la placa de video una copia del texto al doble de resolución, que cae exactamente en el mismo lugar.

**Instalación** (requiere Kitserver 6):

1. Descargá `PES6_HD_Text_v1.0.zip` desde [Releases](https://github.com/angelballay/pes6-hd-text/releases/latest) y copiá `pes6_hd_text.dll` en la carpeta de Kitserver (la que tiene `kload.cfg`).
2. Abrí `kload.cfg` y agregá una línea después de la última `DLL.N`, con el número siguiente, por ejemplo `DLL.26 = "kitserver\pes6_hd_text.dll"`.
3. Sumale 1 a `DLL.num`.
4. A jugar.

**Desinstalar:** borrá la línea, volvé `DLL.num` a su valor anterior y borrá la DLL.

**Probado** en PES 6 original + Kitserver 6 y en PES 6 The Den Patch 2026. **Limitaciones:** solo cambia el texto (la pantalla de título, los logos, los íconos y los números del marcador son imágenes y quedan igual), el contorno de los títulos grandes es el original y no es un parche de pantalla ancha.

¿Una pantalla donde el texto se sigue viendo borroso? Abrí un [issue](https://github.com/angelballay/pes6-hd-text/issues) con una captura.

Soy **pitycharly**, desarrollador de software argentino, y hago mods para PES 6 para mantenerlo vivo. Mi otro mod: **[Change Physics Game](https://github.com/angelballay/pes6_game_physics_mod)**, para que los pases al primer toque no se mueran ([video](https://www.youtube.com/watch?v=KKfPKn4rNsg)).
