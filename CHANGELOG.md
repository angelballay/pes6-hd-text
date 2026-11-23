# Changelog

All notable changes to PES6 HD Text are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.0.2.1] - 2026-11-23

The 1.0.2, clearer to install. Already have 1.0.2? Press **Update to 1.0.2.1** in `hdtext.exe`.

### Changed

- **Languages tab: "Load a language file (.zip)…".** The button, the line under it and the file dialog say it plainly: load the language's `.zip` as you downloaded it, without unzipping it.
- **The README starts with how to install:** extract the whole zip and double-click `Kitserver\hdtext.exe`, the installer.

### Fixed

- **Picking something that isn't a language's `.zip` now says what to load.** Before, the unzipped folder, a file from inside it (such as `ru_text.afs`) or another zip were ignored or called "damaged" or "not signed". If you drop several things at once, the zips are loaded and the rest is reported.

## [1.0.2] - 2026-11-21

From now on, PES6 HD Text can update itself, and it can add extra languages to the game. This version is installed with the new installer (or by hand, as before); the next ones arrive with the **Update** button of `hdtext.exe`.

### Added

- **Installer.** Extract the whole zip and open `Kitserver\hdtext.exe` from the extracted folder. Choose your PES6 folder and press **Install** (or **Update**, over an earlier version). It checks every file against the list signed by the author, saves a copy of whatever it replaces, adds the line to `kload.cfg` (saving the old one first) and opens the installed `hdtext.exe`. Your settings, your fonts and your font backups are kept.
- **Updates.** When the game starts in HD mode, the mod checks at most once a day whether there is a new version. If there is, a short notice appears at the bottom left for six seconds: `PES6 HD Text 1.0.3 is available. Open hdtext.exe to update.` Without internet, or if anything goes wrong, nothing is shown and the game starts as usual.
- **`hdtext.exe` updates the mod.** A new **Updates** box shows the installed version and, when there is a new one, **What's new** and **Update to …**. It downloads the new version, checks its signature and every file, and installs it with the game closed. Your settings, your chosen font, your own fonts and your font backups are kept.
- **Go back.** The previous version is kept: **Go back to …** puts it back (the new `hdtext.exe` stays, so you can return).
- **One switch for the notices:** "Show update notices (here and in the game)". **Check now** always works.
- **Languages tab.** It lists the languages available on the website, each with a link to its page. Download a language's `.zip` there, then **Load a language file…** (several at once, or drop them on the window): `hdtext.exe` checks that it's the author's and puts it in the game's language menu. **Use**, **None** and **Remove** work right away. PES6 HD Text itself doesn't include any translation: each language file brings the small PES6 Translations add-on that shows it in the menu, and `hdtext.exe` installs it and keeps it up to date.
- **Languages go where the game reads them.** PES6 reads its files from the folder written in its registry key, not always from the folder `pes6.exe` is in. `hdtext.exe` reads the key your `pes6.exe` uses (copies of the game and patches with their own key included), installs the language in that folder's `dat` and says where it went. If that isn't the folder you chose, it asks first.
- **Fonts with the language's letters.** When a language goes into the game's menu and your font lacks some of its letters (the game's own font has no Greek or Cyrillic), `hdtext.exe` asks right then whether to switch to the Original style font, which has them all. If you keep yours, the tab says which letters are missing. And with a language in the menu, **Apply** warns before switching to a font that lacks some of its letters.
- **Greek, Cyrillic and more Latin letters in the fonts.** Each included font now has every letter its original font has (Greek and Cyrillic only when the original has the whole alphabet). `HD_original_font` gains 297 letters (Greek, Cyrillic, extended Latin and №). Fonts with every letter used by each language: Russian, 6 (`HD_original_font`, `HD_fira_sans`, `HD_humanist`, `HD_montserrat`, `HD_oswald`, `HD_rubik`); Greek, 3 (`HD_original_font`, `HD_fira_sans`, `HD_humanist`); Turkish, Serbian and Croatian, 25; the game's six languages and Brazilian Portuguese, 32 of 35.
- **One more hooked function**, only while the update notice is on screen: `IDirect3DDevice8::EndScene`. See "For mod makers" in the README.

### Fixed

- **Skill numbers line up with HD fonts.** The game places each number by its width, and its own font has ten digits of the same width. With fonts whose digits have different widths (`HD_wide` and 29 more of the included ones), the columns of skill numbers came out shifted. Now every digit takes the width of the widest one, centred.
- **HD fonts with 16 shades of white** in their palette showed grey, see-through skill numbers. They are now converted to the game's palette when the font loads.
- **Letters no longer lose their last column** in HD fonts whose letter widths aren't a multiple of the font's scale: the width is rounded up, so the letter doesn't run into the next one.

### Changed

- `hdtext.exe` has two tabs, **Font** and **Languages**.
- `hdtext.exe` keeps every line of `hdtext.cfg` it doesn't know (for example `translation` and `translation_name`).
- `hdtext.exe` recognises the included fonts of earlier versions, so **Apply** replaces them with the new ones instead of keeping them as "Font before PES6 HD Text".

## [1.0.1.2] - 2026-11-15

The zip is the full mod. To update from an earlier version, copy its `Kitserver` folder over your old files and keep your `kload.cfg` line, then open `hdtext.exe` and press **Apply** (with `HD_original_font`, this installs the new one).

### Fixed

- **Menu text stays sharp in long sessions, such as Master League.** After a match and some time in the menus (player growth, line-up), menu items and player names could lose the sharp letters and come out blurry. The cause: the mod never found out when the game freed one of its letter sheets, so the old ones piled up until it dropped all of them, the sheets still on screen included. Now the mod lets go of each sheet when the game frees it.

### Changed

- **`HD_original_font`: its twelve symbols (℃ ← ↑ → ↓ □ ■ △ ▲ ○ ● ★) are now drawn in HD.** Before, they were the game's 16 px symbols upscaled.
- **`hdtext.exe` recognises the previous `HD_original_font`.** If it is still installed, the tool shows "older version; press Apply to update it", and your patch's font stays as "Font before PES6 HD Text".
- **One more hooked function**, `0x0095A6C0`: the game releases a letter from a letter sheet, and frees the sheet when it is empty. See "For mod makers" in the README.

## [1.0.1.1] - 2026-11-12

To update from 1.0.1, just replace `pes6_hd_text.dll`.

### Fixed

- **Works with PesAssetLoader** (Dmitri-F's Plugin Loader + Asset Loader). With 1.0.1, PES6 HD Text turned itself off when the Asset Loader was installed (with an HD font, the text came out huge). Now both mods work together.

### Changed

- **Hooks chain to other mods.** If another mod already hooked one of the same game functions with a plain jump, PES6 HD Text now hooks on top of it instead of turning off.

## [1.0.1] - 2026-11-11

### Added

- **HD fonts.** With a high-resolution text font installed, the text is drawn at the resolution of your screen instead of being stretched from 640x480 (tested at 1920x1080).
- **35 HD fonts** in `Kitserver\GDB\fonts`, all 4x:
  - `HD_original_font` keeps the look of the original PES 6 font (based on work by SimoneZ).
  - Clean sans: `HD_barlow_condensed`, `HD_dosis`, `HD_fira_sans`, `HD_humanist`, `HD_kanit`, `HD_montserrat`, `HD_oswald`, `HD_rubik`, `HD_semi_condensed`, `HD_titillium`.
  - Techno: `HD_chakra_petch`, `HD_rajdhani`, `HD_futuristic`, `HD_squared`, `HD_wide`.
  - Sports: `HD_teko` (condensed, in the style of TV match graphics).
  - Rounded and light: `HD_dynapuff`, `HD_marhey`, `HD_snowflake`, `HD_train` and `HD_hachimaru` (these two also draw their own Japanese letters).
  - Eye-catching: `HD_pixel` (retro arcade), `HD_marker` (hand-written marker), `HD_retro` (rounded retro), `HD_stencil` (military stencil), `HD_luckiest` (comic book), `HD_shrikhand` (bold retro script), `HD_kablammo` (cartoon), `HD_neon_lines` (neon tubes), `HD_speed` (speed lines), `HD_nabla` (blocky 3D), `HD_storybook` (storybook), `HD_tokyo_zoo` (small caps), `HD_poster_deco` (art deco poster).
- **`hdtext.exe`, a settings tool** that goes in the Kitserver folder:
  - Two modes: HD (mod on) and Original (mod off).
  - A font list with a preview drawn with the font's own letters.
  - "Add font..." checks that a file really is a game font before adding it.
  - "Installed" shows the font the game uses right now. It checks the file contents, not the name, and says "unknown" when the font was installed by another tool or patch and is not one it knows.
  - It warns you when `afs2fs.dll` is not loaded in `kload.cfg`, because the game would not use the font.
- **Backups.** Every font the tool replaces is kept in `Kitserver\GDB\fonts\backup`, one folder per date and time.
- **Going back to your previous font.** The font you had before PES6 HD Text (for example your patch's font) is saved the first time it is replaced, and it shows in the list as "Font before PES6 HD Text". Original mode puts it back.
- **`hdtext.cfg` settings file** with `mode = hd` or `mode = original`. The tool writes it; the DLL reads it when the game starts.
- **Support for HD fonts made by modders** at 2x, 3x or 4x (the DLL also accepts other scales) and with grey, coloured or black-outlined palettes, for the text font and for the other game fonts.

### Changed

- **More of the text is sharp:**
  - menu items and help texts, which the game draws from its letter sheets;
  - shrunk and italic labels.
- **Cleaner letters with the game's own 16 px fonts:**
  - Thin and narrow fonts (for example the one in PES 6 The Den Patch 2026) keep their faint strokes.
  - Letters that came out broken or with closed holes are repaired one by one.
  - Round letters such as "O" come out symmetric.
- **Text with a drop shadow** is rebuilt letter by letter, so the shadow follows the sharp letters.
- **Outlined menu text** gets an outline drawn around the sharp letter, with the same thickness as the game's.
- **With 4x HD fonts (all the included ones) the game's letter-pair spacing table is turned off,** so letters no longer stick together (for example in "Eto'o").
- **Menus load more smoothly.** Sharp copies are cached: up to 64 MB with the game's own fonts, plus up to 64 MB more with HD fonts.
- **The DLL now has settings** (`hdtext.cfg`) instead of none.

### Fixed

- **Club crests, flags, team-name badges, shirts and button icons are no longer processed by mistake.** In some patches 1.0 gave crests a dark, ragged border. Now only the game's text is touched.
- **Works with PES6 Flags Module (`flags6.dll`, HD crests).** With 1.0, flags6 replaced no crests at all: 1.0 handed the crests to the game at twice their size (128x128), and flags6 only replaces crests that arrive at their original size (64x64). 1.0.1 leaves crests untouched, so the HD crests show again. Tested with flags6 v4, with the game's font and with an HD font ([#1](https://github.com/angelballay/pes6-hd-text/issues/1)).

## [1.0] - 2026-11-07

### Added

- First public release: sharp in-game text for Pro Evolution Soccer 6 (PC) as a Kitserver 6 module.
- The game's text is handed to the video card at twice the resolution, with the same fonts and positions.
- Works with the font of any patch (tested with PES 6 The Den Patch 2026).

[1.0.2]: https://github.com/angelballay/pes6-hd-text/compare/v1.0.1.2...v1.0.2
[1.0.1.2]: https://github.com/angelballay/pes6-hd-text/compare/v1.0.1.1...v1.0.1.2
[1.0.1.1]: https://github.com/angelballay/pes6-hd-text/compare/v1.0.1...v1.0.1.1
[1.0.1]: https://github.com/angelballay/pes6-hd-text/compare/v1.0...v1.0.1
[1.0]: https://github.com/angelballay/pes6-hd-text/releases/tag/v1.0
