# PES6 HD Text

**The first PES 6 mod that makes the game's text sharp in HD: same fonts, same layout, and it works with any patch.**

A Kitserver 6 module for Pro Evolution Soccer 6 (PC) by **pitycharly**. Version 1.0.1.

**[⬇ Download PES6 HD Text 1.0.1](https://github.com/angelballay/pes6-hd-text/releases/latest)** · [What's new](#whats-new-in-101) · [Install](#install) · [Choosing a font](#choosing-a-font) · [Compatibility](#compatibility) · [Known limitations](#known-limitations) · [Changelog](CHANGELOG.md) · [Español](#español)

## What's new in 1.0.1

- **HD fonts:** with an HD font the text is drawn at the resolution of your screen, so it stays crisp at 1080p, 1440p and 4K.
- **18 HD fonts included:** `HD_original_font` keeps the original PES 6 look, and 17 more change the style, from clean sans to pixel, marker or stencil.
- **`pes6_hd_text.exe`, a settings tool:** turn the mod on or off, pick a font with a preview, add your own fonts and go back to the font you had before.
- **Cleaner letters with the game's own fonts:** thin fonts keep their strokes, broken letters are repaired and round letters come out symmetric.
- **More text is sharp:** menu items, help texts, the match clock, and shrunk and italic labels.
- **Fixed:** club crests, flags and icons are no longer touched by mistake.

Full list in the [changelog](CHANGELOG.md).

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
- **Same positions:** nothing moves and nothing gets cut. Keep your game's font, made sharp, or switch to an HD font.
- **HD fonts at your screen's resolution:** 18 included, from the original PES 6 look to pixel, marker or stencil styles.
- **Works with whatever font your patch uses.** PES 6 The Den Patch 2026 ships its own font and gets sharp too.
- **Any game language.** It works on whatever text the game draws, so it doesn't depend on the language (tested in Spanish).
- **A settings tool** (`pes6_hd_text.exe`) to turn it on or off and choose the font, with a preview.

## How it works

PES 6 draws its text with tiny 16 px bitmap fonts, and the GPU stretches them to your resolution. That is why text looks blurry on modern screens. Simply using bigger fonts breaks the layout, because the game calculates every position from the original font sizes.

PES6 HD Text doesn't touch the fonts at all:

1. The game builds each piece of text exactly as it always did, with its original fonts and sizes.
2. When the game turns that text into a Direct3D texture, the module hands over a **copy at twice the resolution**. The upscale is edge-aware: the shape of each letter comes from the alpha channel with a threshold, and the colours come from the original palette. That covers outlines and the 256-colour letters of the big titles.
3. PES 6 maps textures by the image size, so the sharper copy lands in **exactly the same rectangle** on screen.

The game recreates many of these textures over and over, so the upscaled copies are cached and menus stay smooth.

**With an HD font** the module goes further. The game draws its menus in a 640x480 space and stretches it to your screen (at 1920x1080 that is 3x wide and 2.25x tall), so even a 2x copy ends up stretched. With an HD font, each piece of text is built at 4x and then sized to exactly the density of your screen. The game still measures and places the text with its original sizes, so nothing moves.

## Install

Requires **Kitserver 6** with `afs2fs.dll` loaded in `kload.cfg` (it comes with Kitserver 6 and with most patches). Don't have it yet? [Kitserver 6](https://www.mediafire.com/file/ljbcnczm893g1b6/kitserver.rar/file)

1. Download `PES6_HD_Text_v1.0.1.zip` from [Releases](https://github.com/angelballay/pes6-hd-text/releases/latest) and copy everything inside its `Kitserver` folder into your game's Kitserver folder (the one with `kload.cfg`).
2. Open `kload.cfg` with Notepad and add a line after the last `DLL.N`, using the next number. For example, if your last line is `DLL.25`:
   ```
   DLL.26 = "kitserver\pes6_hd_text.dll"
   ```
3. Increase `DLL.num` by 1 (in the example, `DLL.num = 26` becomes `DLL.num = 27`).
4. Run `Kitserver\pes6_hd_text.exe`, pick a font and press **Apply** (see [Choosing a font](#choosing-a-font)).
5. Start the game.

## Choosing a font

`pes6_hd_text.exe` is a small settings tool that lives in your Kitserver folder.

- **HD** turns the mod on. Pick a font from the list and check the preview. "Game font" keeps your game's own letters, made sharp.
- **Original (mod off)** turns the mod off and puts back the font the game had before PES6 HD Text.
- **Add font...** adds your own font file (`.bin`, the game's font 53 format). It is checked first, and files that are not a valid font are rejected.
- **Installed** shows the font the game uses right now. It checks the file contents; if a font was installed by another tool or patch and is not one it knows, it says "unknown".
- Fonts live in `Kitserver\GDB\fonts`, and the installed one is copied to `Kitserver\dat\0_text.afs`. Every replaced font is kept in `Kitserver\GDB\fonts\backup`, and the one you had before PES6 HD Text stays in the list as "Font before PES6 HD Text".
- Windows asks for permission when you open it, because it writes in the game folder (often inside Program Files).

## Uninstall

1. Run `pes6_hd_text.exe`, choose **Original (mod off)** and press **Apply**. This puts back the font you had before.
2. Remove the `pes6_hd_text.dll` line from `kload.cfg` and put `DLL.num` back to its previous value.
3. Delete `pes6_hd_text.dll`, `pes6_hd_text.exe`, `pes6_hd_text.cfg` and the `Kitserver\GDB\fonts` folder.

Don't leave an HD font installed without the DLL: the game can't load an HD font on its own.

## Compatibility

- Tested on the **original PES 6** + Kitserver 6.
- Tested on **PES 6 The Den Patch 2026**, together with its 26 other Kitserver modules, including [Change Physics Game](https://github.com/angelballay/pes6_game_physics_mod).
- Before changing anything, the module checks the game code where it hooks. If your `pes6.exe` is different, it does nothing and the game runs as usual.
- Sharp copies use at most 64 MB of memory with the game's own fonts, plus up to 64 MB more with HD fonts.

## Known limitations

- **Text only.** Graphics that are images stay as they are: the title screen ("Press any button"), logos, icons, menu widgets and the scoreboard numbers (they are part of a texture).
- **Big outlined titles keep the game's original outline,** so letters that overlap slightly in the original still overlap (now sharp).
- **Not a widescreen fix:** the menu layer is still 4:3, stretched to your screen.

Since it only touches text, it should sit nicely next to texture packs and other HD projects.

## FAQ

**Does it change the font?** Only if you want. "Game font" keeps the exact fonts your game or patch already has; the HD fonts are optional and you can go back at any time.

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

The included HD fonts are modified versions of free fonts (SIL Open Font License and Apache 2.0). The download lists each one with its source font and license in `Kitserver\GDB\fonts\FONT_LICENSES.txt`.

## Feedback

Found a screen where the text is still blurry? Open an [issue](https://github.com/angelballay/pes6-hd-text/issues) with a screenshot and the patch you use.

## About the author

I'm **pitycharly**, an Argentine software developer who makes mods for PES 6. I want to help keep this game alive, and I'd love to see my mods inside the patches people already play. I build them as Kitserver modules and keep them compatible with all the existing ones.

My other mod:

- **[Change Physics Game](https://github.com/angelballay/pes6_game_physics_mod)** (v1.1): first-time passes no longer die on the pitch. A faster pass impulse makes the ball roll faster and more smoothly. Tested on the original PES 6 and on PES 6 The Den Patch 2026. [Video](https://www.youtube.com/watch?v=KKfPKn4rNsg) · [Download](https://www.mediafire.com/file/fwqcw1omr98uekw/1.1_pes6_game_physics_mod.zip/file)

---

## Español

**El primer mod de PES 6 que pone el texto del juego nítido en HD: mismas fuentes, mismo diseño, y anda con cualquier parche.**

Los menús, los nombres de jugadores y de equipos y los títulos se ven nítidos en lugar de borrosos y estirados. El juego sigue usando sus posiciones: nada se mueve ni se corta. Podés quedarte con la fuente de tu juego, ahora nítida, o elegir una fuente HD.

**Novedades de la 1.0.1** (lista completa en el [changelog](CHANGELOG.md)):

- **Fuentes HD:** con una fuente HD el texto se dibuja a la resolución de tu pantalla y se ve nítido en 1080p, 1440p y 4K.
- **18 fuentes HD incluidas:** `HD_original_font` mantiene el aspecto del PES 6 original, y otras 17 cambian el estilo, desde fuentes limpias hasta pixel, marcador o esténcil.
- **`pes6_hd_text.exe`, una herramienta de configuración:** activa o apaga el mod, elige la fuente con vista previa, agrega tus propias fuentes y vuelve a la que tenías antes.
- **Letras más prolijas con las fuentes del juego:** las fuentes finas conservan sus trazos, las letras cortadas se reparan y las redondas salen simétricas.
- **Más texto nítido:** opciones de los menús, textos de ayuda, el reloj del partido y las etiquetas achicadas o en cursiva.
- **Arreglo:** los escudos, las banderas y los íconos ya no se tocan por error.

**Instalación** (requiere Kitserver 6 con `afs2fs.dll` cargada en `kload.cfg`):

1. Descargá `PES6_HD_Text_v1.0.1.zip` desde [Releases](https://github.com/angelballay/pes6-hd-text/releases/latest) y copiá todo lo que está dentro de su carpeta `Kitserver` en la carpeta Kitserver del juego (la que tiene `kload.cfg`).
2. Abrí `kload.cfg` y agregá una línea después de la última `DLL.N`, con el número siguiente, por ejemplo `DLL.26 = "kitserver\pes6_hd_text.dll"`.
3. Sumale 1 a `DLL.num`.
4. Abrí `Kitserver\pes6_hd_text.exe`, elegí una fuente y apretá **Apply**.
5. A jugar.

**Elegir la fuente:** en `pes6_hd_text.exe`, **HD** activa el mod con la fuente que elijas de la lista, y **Original (mod off)** lo apaga y vuelve a poner la fuente que tenías antes. Cada fuente reemplazada queda guardada en `Kitserver\GDB\fonts\backup`.

**Desinstalar:** en `pes6_hd_text.exe` elegí **Original (mod off)** y apretá **Apply**. Después borrá la línea de `kload.cfg`, volvé `DLL.num` a su valor anterior y borrá `pes6_hd_text.dll`, `pes6_hd_text.exe`, `pes6_hd_text.cfg` y la carpeta `Kitserver\GDB\fonts`. No dejes una fuente HD instalada sin la DLL: el juego solo no puede cargarla.

**Probado** en PES 6 original + Kitserver 6 y en PES 6 The Den Patch 2026, en español; como trabaja sobre el texto que dibuja el juego, no depende del idioma. Gracias a **The Den** por *PES 6 The Den Patch 2026*. **Limitaciones:** solo cambia el texto (la pantalla de título, los logos, los íconos y los números del marcador son imágenes y quedan igual), el contorno de los títulos grandes es el original y no es un parche de pantalla ancha.

**Licencia:** [MIT](LICENSE) con una condición de atribución. Si lo incluís en un parche, poné en los créditos: *"Mod PES6 HD Text Original creado por PityCharly."* Las fuentes HD incluidas son versiones modificadas de fuentes libres (SIL Open Font License y Apache 2.0); el detalle está en `Kitserver\GDB\fonts\FONT_LICENSES.txt` dentro de la descarga.

¿Una pantalla donde el texto se sigue viendo borroso? Abrí un [issue](https://github.com/angelballay/pes6-hd-text/issues) con una captura.

Soy **pitycharly**, desarrollador de software argentino, y hago mods para PES 6 para mantenerlo vivo. Mi otro mod: **[Change Physics Game](https://github.com/angelballay/pes6_game_physics_mod)**, para que los pases al primer toque no se mueran ([video](https://www.youtube.com/watch?v=KKfPKn4rNsg)).
