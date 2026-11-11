# Changelog

All notable changes to PES6 HD Text are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

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
  - menu items, help texts and the match clock, which the game draws from its letter sheets;
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
- **Works with the HD crests module (`flags6.dll`).** With 1.0, flags6 replaced no crests at all: 1.0 handed the crests to the game at twice their size (128x128), and flags6 only replaces crests that arrive at their original size (64x64). 1.0.1 leaves crests untouched, so the HD crests show again. Tested with flags6 v4, with the game's font and with an HD font ([#1](https://github.com/angelballay/pes6-hd-text/issues/1)).

## [1.0] - 2026-11-07

### Added

- First public release: sharp in-game text for Pro Evolution Soccer 6 (PC) as a Kitserver 6 module.
- The game's text is handed to the video card at twice the resolution, with the same fonts and positions.
- Works with the font of any patch (tested with PES 6 The Den Patch 2026).

[1.0.1]: https://github.com/angelballay/pes6-hd-text/compare/v1.0...v1.0.1
[1.0]: https://github.com/angelballay/pes6-hd-text/releases/tag/v1.0
