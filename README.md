# PES6 HD Text

**The first PES 6 mod that makes the game's text sharp in HD: same fonts, same layout, and it works with any patch.**

A Kitserver 6 module for Pro Evolution Soccer 6 (PC) by **pitycharly**. Version 1.0.

**[⬇ Download PES6 HD Text 1.0](https://github.com/angelballay/pes6-hd-text/releases/latest)** · [Install](#install) · [Compatibility](#compatibility) · [Known limitations](#known-limitations) · [Español](#español)

## Before / after

![Zoomed before / after of the player list in Edit Player](images/zoom-comparison.png)

*Zoomed crop of the Edit Player screen: same game, same screen, left without the mod and right with it.*

### Zoomed comparisons

Same zone of the same screen, before and after. The "after" capture is the one rescaled to line them up, so the comparison never favours the mod.

**Original PES 6**

![Pause menu, zoomed: before and after](images/zoom/original-pause-menu.png)

![Edit menu, zoomed: before and after](images/zoom/original-edit-menu.png)

![Match settings, zoomed: before and after](images/zoom/original-match-settings.png)

![Line-up, zoomed: before and after](images/zoom/original-lineup.png)

**PES 6 The Den Patch 2026 (its own font)**

![The Den Patch, match settings, zoomed: before and after](images/zoom/den-match-settings.png)

![The Den Patch, edit menu, zoomed: before and after](images/zoom/den-edit-menu.png)

![The Den Patch, line-up, zoomed: before and after](images/zoom/den-lineup.png)

![The Den Patch, pause menu, zoomed: before and after](images/zoom/den-pause-menu.png)

### Full screens: original PES 6

**Edit player**

| Before | After |
|---|---|
| ![Edit player, before](images/original/edit-player-before.png) | ![Edit player, after](images/original/edit-player-after.png) |

<details>
<summary><b>More screens: original PES 6</b> (edit menu, team selection, match settings, line-up, pause menu)</summary>

**Edit menu**

| Before | After |
|---|---|
| ![Edit menu, before](images/original/edit-menu-before.png) | ![Edit menu, after](images/original/edit-menu-after.png) |

**Team selection**

| Before | After |
|---|---|
| ![Team selection, before](images/original/team-select-before.png) | ![Team selection, after](images/original/team-select-after.png) |

**Match settings**

| Before | After |
|---|---|
| ![Match settings, before](images/original/match-settings-before.png) | ![Match settings, after](images/original/match-settings-after.png) |

**Line-up**

| Before | After |
|---|---|
| ![Line-up, before](images/original/lineup-before.png) | ![Line-up, after](images/original/lineup-after.png) |

**Pause menu (in match)**

| Before | After |
|---|---|
| ![Pause menu (in match), before](images/original/pause-menu-before.png) | ![Pause menu (in match), after](images/original/pause-menu-after.png) |

</details>

### Full screens: PES 6 The Den Patch 2026

<details>
<summary><b>Screens: The Den Patch 2026</b> (match settings, edit menu, line-up, pause menu)</summary>

**Match settings**

| Before | After |
|---|---|
| ![Match settings, before](images/den/match-settings-before.png) | ![Match settings, after](images/den/match-settings-after.png) |

**Edit menu**

| Before | After |
|---|---|
| ![Edit menu, before](images/den/edit-menu-before.png) | ![Edit menu, after](images/den/edit-menu-after.png) |

**Line-up**

| Before | After |
|---|---|
| ![Line-up, before](images/den/lineup-before.png) | ![Line-up, after](images/den/lineup-after.png) |

**Pause menu (in match)**

| Before | After |
|---|---|
| ![Pause menu (in match), before](images/den/pause-menu-before.png) | ![Pause menu (in match), after](images/den/pause-menu-after.png) |

</details>

## What it does

- Menus, player names, team names and titles are drawn **sharp** instead of blurry and stretched.
- **Same fonts, same positions:** nothing moves, nothing gets cut, and the original PES 6 style stays.
- **Works with whatever font your patch uses.** PES 6 The Den Patch 2026 ships its own font and gets sharp too.
- **Any game language.** It upscales whatever text the game draws, so it doesn't depend on the language (tested in Spanish).
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

PES6 HD Text is a plain Kitserver module that runs next to whatever your patch already has. If you want to include it in your patch, go ahead: just add this line to your patch credits, as the [license](LICENSE) requires:

> Mod PES6 HD Text Original creado por PityCharly.

And let me know if anything conflicts (open an [issue](https://github.com/angelballay/pes6-hd-text/issues)).

## Thanks

Thanks to **The Den** for *PES 6 The Den Patch 2026*, the patch where PES6 HD Text was tested next to 26 other Kitserver modules and with its own font.

## License

[MIT](LICENSE), with one extra condition: any patch, mod or project that includes or reuses PES6 HD Text, fully or partly, must show this line in its credits: *"Mod PES6 HD Text Original creado por PityCharly."*

## Feedback

Found a screen where the text is still blurry? Open an [issue](https://github.com/angelballay/pes6-hd-text/issues) with a screenshot and the patch you use.

## About the author

I'm **pitycharly**, an Argentine software developer who makes mods for PES 6. I want to help keep this game alive, and I'd love to see my mods inside the patches people already play. I build them as Kitserver modules and keep them compatible with all the existing ones.

My other mod:

- **[Change Physics Game](https://github.com/angelballay/pes6_game_physics_mod)** (v1.1): first-time passes no longer die on the pitch. A faster pass impulse makes the ball roll faster and more smoothly. Tested on the original PES 6 and on PES 6 The Den Patch 2026. [Video](https://www.youtube.com/watch?v=KKfPKn4rNsg) · [Download](https://www.mediafire.com/file/fwqcw1omr98uekw/1.1_pes6_game_physics_mod.zip/file)

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

**Probado** en PES 6 original + Kitserver 6 y en PES 6 The Den Patch 2026, en español; como agranda el texto que dibuja el juego, no depende del idioma. Gracias a **The Den** por *PES 6 The Den Patch 2026*. **Limitaciones:** solo cambia el texto (la pantalla de título, los logos, los íconos y los números del marcador son imágenes y quedan igual), el contorno de los títulos grandes es el original y no es un parche de pantalla ancha.

**Licencia:** [MIT](LICENSE) con una condición de atribución. Si lo incluís en un parche, poné en los créditos: *"Mod PES6 HD Text Original creado por PityCharly."*

¿Una pantalla donde el texto se sigue viendo borroso? Abrí un [issue](https://github.com/angelballay/pes6-hd-text/issues) con una captura.

Soy **pitycharly**, desarrollador de software argentino, y hago mods para PES 6 para mantenerlo vivo. Mi otro mod: **[Change Physics Game](https://github.com/angelballay/pes6_game_physics_mod)**, para que los pases al primer toque no se mueran ([video](https://www.youtube.com/watch?v=KKfPKn4rNsg)).
