# PES6 HD Text

**PES 6's in-game text, sharp in HD: same fonts, same layout, and it works with any patch.**

A Kitserver 6 module for Pro Evolution Soccer 6 (PC) by **pitycharly**. Version 1.0.2.1.

**[⬇ Download PES6 HD Text 1.0.2.1](https://github.com/angelballay/pes6-hd-text/releases/latest)** · [What's new](#whats-new-in-102) · [Make your own font](#-make-your-own-hd-font-right-in-your-browser) · [Install](#install) · [Choosing a font](#choosing-a-font) · [With your patch's font](#using-it-with-your-patchs-font) · [Languages](#languages) · [Updates](#updates) · [Compatibility](#compatibility) · [Known limitations](#known-limitations) · [Changelog](CHANGELOG.md) · [Español](#español)

**▶ [Video (4 min): before vs after, install, the font picker and all 35 fonts](https://www.youtube.com/watch?v=AISb6npriI4)**

## 🎨 Make your own HD font, right in your browser

**[Pes6FontCreator](https://pes6fontcreator.com/en/) turns any TTF or OTF font into an HD font for PES6 HD Text.** Load your font, fill in the letters it is missing (automatically or one by one) and download your `HD_<name>.bin`. Then open `hdtext.exe` → **Add font...** → **Apply**. Nothing to install and nothing is uploaded: everything runs in your browser.

**[✏️ Create your font at pes6fontcreator.com](https://pes6fontcreator.com/en/)**

## What's new in 1.0.2

- **1.0.2.1:** the **Languages** tab says plainly that it loads the language's `.zip` as you downloaded it, without unzipping it, and says what to load if you pick something else (the unzipped folder, a file from inside it, another zip).
- **Installer:** extract the zip, open `Kitserver\hdtext.exe` from it, choose your PES6 folder and press **Install** (or **Update** over an earlier version). See [Install](#install).
- **Updates from `hdtext.exe`:** when there is a new version, the game shows a short notice and `hdtext.exe` installs it with **Update to …**, checking the author's signature first. **Go back** returns to the previous one. See [Updates](#updates).
- **Languages:** the new **Languages** tab loads the extra languages from the [Translations section of the website](https://pes6fontcreator.com/translations/) into the game's language menu, in the folder the game really reads. See [Languages](#languages).
- **Greek, Cyrillic and more Latin letters** in the included fonts (`HD_original_font`, `HD_fira_sans` and `HD_humanist` have them all).
- **Fixed:** skill numbers line up again with HD fonts.

Full list in the [changelog](CHANGELOG.md).

## What's new in 1.0.1.2

- **Menu text stays sharp in long sessions, such as Master League.** After a match and some time in the menus, menu items and player names could come out blurry. Now they stay sharp.
- **`HD_original_font` draws its symbols in HD** (℃ ← ↑ → ↓ □ ■ △ ▲ ○ ● ★). Before, they were the game's 16 px symbols upscaled.

  ![HD_original_font symbols: upscaled in 1.0.1.1, redrawn in HD in 1.0.1.2](images/1.0.1.2/hd-original-font-symbols.png)
- **Make your own HD font:** [Pes6FontCreator](https://pes6fontcreator.com/en/) turns any TTF or OTF font into an HD font for PES6 HD Text, in your browser.
- Already have an earlier version? See [Install](#install).

## What's new in 1.0.1.1

- **Works with PesAssetLoader** (the Plugin Loader and Asset Loader by Dmitri-F). With 1.0.1, PES6 HD Text turned itself off when the Asset Loader was installed, and with an HD font the text came out huge. Now both mods work together.

## What's new in 1.0.1

- **HD fonts:** with an HD font the text is drawn at the resolution of your screen instead of being stretched from 640x480 (tested at 1920x1080).
- **35 HD fonts included:** `HD_original_font` keeps the original PES 6 look, and 34 more change the style, from clean sans to pixel, marker, stencil, comic or neon.
- **`hdtext.exe`, a settings tool:** turn the mod on or off, pick a font with a preview, add your own fonts and go back to the font you had before.
- **Cleaner letters with the game's own fonts:** thin fonts keep their strokes, broken letters are repaired and round letters come out symmetric.
- **More text is sharp:** menu items, help texts, and shrunk and italic labels.
- **Fixed:** club crests, flags and icons are no longer touched by mistake, and PES6 Flags Module (`flags6.dll`, HD crests) now works alongside it ([#1](https://github.com/angelballay/pes6-hd-text/issues/1)).

Full list in the [changelog](CHANGELOG.md).

## Before / after

Every image compares the same screen. "No mod" is the game without the mod; only the modded side is rescaled to line them up, so the comparison never favours the mod.

**Original PES 6, line-up:** no mod, the game font sharpened 2x, and HD_original_font

![Original PES 6, line-up: no mod, game font sharpened 2x, HD_original_font](images/1.0.1/original-lineup.png)

**PES 6 The Den Patch 2026, line-up:** no mod, its own font sharpened 2x, and HD_stencil (one of the 35 HD fonts)

![The Den Patch 2026, line-up: no mod, its own font sharpened 2x, HD_stencil](images/1.0.1/den-lineup.png)

**One screen, eight looks**

![Line-up with no mod, the game font made sharp and six HD fonts](images/1.0.1/fonts-lineup.png)

<details>
<summary><b>More comparisons</b> (pause menu, edit player, match settings, edit menu, kit selection)</summary>

**The Den Patch 2026, pause menu**

![The Den Patch 2026, pause menu](images/1.0.1/den-pause-menu.png)

**The Den Patch 2026, edit player**

![The Den Patch 2026, edit player](images/1.0.1/den-edit-player.png)

**The Den Patch 2026, match settings**

![The Den Patch 2026, match settings](images/1.0.1/den-match-settings.png)

**The Den Patch 2026, edit menu**

![The Den Patch 2026, edit menu](images/1.0.1/den-edit-menu.png)

**Original PES 6, pause menu**

![Original PES 6, pause menu](images/1.0.1/original-pause-menu.png)

**Original PES 6, match settings**

![Original PES 6, match settings](images/1.0.1/original-match-settings.png)

**Original PES 6, edit menu**

![Original PES 6, edit menu](images/1.0.1/original-edit-menu.png)

**Pause menu, four looks**

![Pause menu with no mod and three HD fonts](images/1.0.1/fonts-pause-menu.png)

**Kit selection, two HD fonts** (no capture without the mod of this screen)

![Kit selection with HD_original_font and HD_montserrat](images/1.0.1/fonts-kit-select.png)

</details>

<details>
<summary><b>1.0 vs 1.0.1</b> (the same font at 2x, cleaner letters in 1.0.1)</summary>

With the game's own fonts, 1.0.1 keeps faint strokes, repairs broken letters and makes round letters symmetric. Both sides use the same font, sharpened 2x.

**The Den Patch 2026, pause menu**

![The Den Patch 2026, pause menu: 1.0 vs 1.0.1](images/1.0.1/upgrade/den-pause-menu.png)

**The Den Patch 2026, match settings**

![The Den Patch 2026, match settings: 1.0 vs 1.0.1](images/1.0.1/upgrade/den-match-settings.png)

**The Den Patch 2026, edit menu**

![The Den Patch 2026, edit menu: 1.0 vs 1.0.1](images/1.0.1/upgrade/den-edit-menu.png)

**Original PES 6, line-up**

![Original PES 6, line-up: 1.0 vs 1.0.1](images/1.0.1/upgrade/original-lineup.png)

**Original PES 6, edit menu**

![Original PES 6, edit menu: 1.0 vs 1.0.1](images/1.0.1/upgrade/original-edit-menu.png)

</details>

<details>
<summary><b>Screenshots of version 1.0</b> (the game's own fonts at 2x)</summary>

![Zoomed before / after of the player list in Edit Player](images/zoom-comparison.png)

*Zoomed crop of the Edit Player screen: same game, same screen, left without the mod and right with it.*

#### Zoomed comparisons

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

#### Full screens: original PES 6

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

#### Full screens: PES 6 The Den Patch 2026

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

</details>

## What it does

- Menus, player names, team names and titles are drawn **sharp** instead of blurry and stretched.
- **Same positions:** nothing moves and nothing gets cut. Keep your game's font, made sharp, or switch to an HD font.
- **HD fonts at your screen's resolution:** 35 included, from the original PES 6 look to pixel, marker, stencil, comic or neon styles.
- **Works with whatever font your patch uses.** PES 6 The Den Patch 2026 ships its own font and gets sharp too.
- **Any game language.** It works on whatever text the game draws, so it doesn't depend on the language (tested in Spanish).
- **A settings tool** (`hdtext.exe`) to turn it on or off and choose the font, with a preview. It also installs and updates the mod.
- **Extra languages:** the **Languages** tab of `hdtext.exe` adds the languages of the website (Greek, Croatian, Indonesian, Brazilian Portuguese, Russian, Serbian, Turkish…) to the game's language menu.

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

The zip is the full mod, not a patch: you don't need any earlier version.

**With the installer (recommended)**

1. Download `PES6_HD_Text_v1.0.2.1.zip` from [Releases](https://github.com/angelballay/pes6-hd-text/releases/latest) and extract the whole zip (right click → **Extract All**). Don't run anything from inside the zip.
2. Double-click `Kitserver\hdtext.exe` in the extracted folder: it's the installer.
3. Check the PES6 folder it proposes (or press **Browse…**) and press **Install**. Over an earlier version (1.0 to 1.0.2) the button says **Update**: your settings and fonts are kept.
4. The installed `hdtext.exe` opens: pick a font and press **Apply** (see [Choosing a font](#choosing-a-font)).
5. Start the game.

The installer checks every file against the list signed by the author, saves a copy of whatever it replaces, and adds `DLL.N = "kitserver\pes6_hd_text.dll"` to `Kitserver\kload.cfg` (saving the old one in `Kitserver\pes6pkg\backup\kload.cfg\`). If your `kload.cfg` has an unusual layout, it doesn't touch it and tells you the line to add. From 1.0.2 on, new versions are installed from `hdtext.exe` itself (see [Updates](#updates)).

**Is this zip the author's?** Before the first install, compare the zip's SHA-256 with the one shown on the [release page](https://github.com/angelballay/pes6-hd-text/releases): `certutil -hashfile PES6_HD_Text_v1.0.2.1.zip SHA256`. After that, every update is checked by `hdtext.exe` itself.

**By hand**

1. Copy everything inside the zip's `Kitserver` folder into your game's Kitserver folder (the one with `kload.cfg`).
2. Open `kload.cfg` with Notepad and add a line after the last `DLL.N`, using the next number. For example, if your last line is `DLL.25`:
   ```
   DLL.26 = "kitserver\pes6_hd_text.dll"
   ```
3. Increase `DLL.num` by 1 (in the example, `DLL.num = 26` becomes `DLL.num = 27`).
4. Run `Kitserver\hdtext.exe`, pick a font and press **Apply** (see [Choosing a font](#choosing-a-font)).
5. Start the game.

Updating by hand from an earlier version: copy the zip's `Kitserver` folder over your old files and keep the `pes6_hd_text.dll` line you already have in `kload.cfg` (don't add another one). Then run `hdtext.exe` and press **Apply** (if your font is one of the included ones, this installs its new version).

## Choosing a font

`hdtext.exe` is a small settings tool that lives in your Kitserver folder. The **Font** tab picks the font (and has the **Updates** box); the **Languages** tab adds languages (see [Languages](#languages)).

![The settings tool, Font tab: mode, font list with preview, the font in use and the Updates box](images/1.0.2/settings-tool.png)

- **HD** turns the mod on. Pick a font from the list and check the preview. "Game font" keeps your game's own letters, made sharp.
- **Original (mod off)** turns the mod off and puts back the font the game had before PES6 HD Text.
- **Add font...** adds your own font file (`.bin`, the game's font 53 format). It is checked first, and files that are not a valid font are rejected. To make your own HD font from any TTF or OTF font, use [Pes6FontCreator](https://pes6fontcreator.com/en/), in your browser.
- **Installed** shows the font the game uses right now. It checks the file contents; if a font was installed by another tool or patch and is not one it knows, it says "unknown".
- Fonts live in `Kitserver\GDB\fonts`, and the installed one is copied to `Kitserver\dat\0_text.afs`. Every replaced font is kept in `Kitserver\GDB\fonts\backup`, and the one you had before PES6 HD Text stays in the list as "Font before PES6 HD Text".
- Windows asks for permission when you open it, because it writes in the game folder (often inside Program Files).

**The 35 HD fonts**, as the tool previews them (also in the [fonts](fonts) folder of this repo, with their licenses):

![The 35 HD fonts, as the settings tool previews them](images/1.0.1/fonts-all-35.png)

## Using it with your patch's font

PES6 HD Text works with the font your patch already has. Open `hdtext.exe` and choose:

| You want | In `hdtext.exe` |
|---|---|
| **Your patch's font, sharpened 2x** | Leave **HD** and the selected font as they are, and press **Apply**. The font in use is already selected. |
| **An HD font instead** | **HD**, pick an `HD_…` font, **Apply**. Your patch's font is saved and stays in the list. |
| **Back to your patch's font, still sharp** | **HD**, select it again, **Apply**. |
| **Back to your patch's font, without the mod** | **Original (mod off)**, **Apply**. The font comes back exactly as the patch had it, and the mod stops doing anything. |

Where your patch's font shows up in the list:

- **"Game font"** if the patch keeps it inside the game's own files (`dat\0_text.afs`), as PES 6 The Den Patch 2026 does. "Installed" then says *game font (The Den Patch 2026)*.
- **"Font before PES6 HD Text"** if the patch installed it with Kitserver (`Kitserver\dat\0_text.afs\unknow_00053.bin` or `unnamed_53*.bin`). The first time you open the tool, it is copied to `Kitserver\GDB\fonts\backup\before_pes6_hd_text`.

If your patch ships a font that is already bigger than the original (an HD font), the mod detects it and uses it as HD by itself.

## Languages

PES6 HD Text doesn't include any translation. The **Languages** tab of `hdtext.exe` adds the languages you download from the [Translations section of the website](https://pes6fontcreator.com/translations/) to the game's language menu:

1. Download the language's `.zip`. **Don't unzip it:** `hdtext.exe` needs the whole `.zip`. The **Get it ↗** link next to each language in the tab opens its page.
2. Open `Kitserver\hdtext.exe` → **Languages** → **Load a language file (.zip)…** and pick that `.zip` (or drop it on the window; several at once work too).
3. Start PES6 and choose the language on its language screen.

![The Languages tab with the seven languages installed and Greek in the game menu](images/1.0.2/languages.png)

**Use** puts another installed language in the game's menu, **None** leaves only the game's own languages, and **Remove** deletes a language (you can load it again later). Each language file is checked before anything is installed: it must be signed by its author.

**Where the language goes.** PES6 reads its files from the folder written in its registry key, not always from the folder `pes6.exe` is in (patches and copies of the game often have their own key). `hdtext.exe` reads the key your `pes6.exe` uses and installs the language in that folder's `dat`; the tab always says which folder that is. If it isn't the folder you chose, `hdtext.exe` asks before installing there. If it can't find out (no key, for example), it installs in the folder you chose and tells you.

**The add-on.** Each language file also brings the small PES6 Translations add-on (`Kitserver\translations.dll`) that puts it in the game's menu: `hdtext.exe` installs it the first time, adds it to `kload.cfg` after PES6 HD Text, and keeps it up to date. It can also be installed on its own from [its page](https://pes6fontcreator.com/mods/pes6-translations/).

**Fonts and letters.** The game's own font has no Greek or Cyrillic. When a language goes into the menu and your font lacks some of its letters, `hdtext.exe` asks right then: **Use Original style** switches to `HD_original_font`, which has the letters of every language (and turns HD on, if it was off); **Keep my font** leaves it, and the tab says which letters are missing (they would show as gaps) with a **Change font** link. With a language in the menu, **Apply** in the Font tab also warns before you switch to a font that lacks some of its letters (**Apply anyway** / **Cancel**). Fonts with every letter: Russian, `HD_original_font`, `HD_fira_sans`, `HD_humanist`, `HD_montserrat`, `HD_oswald` and `HD_rubik`; Greek, `HD_original_font`, `HD_fira_sans` and `HD_humanist`; Turkish, Serbian and Croatian, 25 of the 35 fonts.

## Updates

- **What is checked, and when.** When the game starts in HD mode, the mod downloads a small signed file (the update index, `index.json` and `index.json.minisig` from [pes6-package-pc](https://github.com/angelballay/pes6-package-pc)) at most once a day, in the background. It sends nothing about you: the request only says `PES6-HD-Text/<version>`. If there is a new version, a notice shows at the bottom left for six seconds. `hdtext.exe` checks the same file when it opens, and the **Languages** tab reads it for the list of languages.
- **Updating.** In `hdtext.exe`, the **Updates** box shows **What's new** and **Update to …**. Close the game and press it: `hdtext.exe` downloads the new version, checks it and installs it. Your settings, your chosen font, your own fonts and your font backups are kept. **Go back to …** puts the previous version back.
- **What is trusted.** Only files signed with the author's keys, which are built into the DLL and `hdtext.exe`. The index has a number that only goes up and an expiry date, so an old or frozen index is refused. The new version is downloaded only from this repository's releases, and every file is checked (size and SHA-256) before anything is replaced. The game's DLL never downloads or installs anything: only `hdtext.exe` does, with the game closed.
- **Where things go.** The installed version's signed list is `Kitserver\pes6pkg\installed\hdtext.json` (and one per language and for the add-on, next to it); the copy of the previous version is in `Kitserver\pes6pkg\backup\hdtext\`; the last check is in `%LOCALAPPDATA%\pes6pkg\state.json`. Nothing else is written.
- **Turn it off.** In `hdtext.exe`, untick "Show update notices (here and in the game)" and press **Apply** (or write `update_notices = off` in `Kitserver\hdtext.cfg`). **Check now** still works, and opening the **Languages** tab still gets the list of languages (that's all it does: nothing is installed without you).
- **Check a release by hand.** Each release has `hdtext-<version>.manifest.json` and its `.minisig`. With [minisign](https://jedisct1.github.io/minisign/): `minisign -V -m hdtext-1.0.2.manifest.json -P <key>`, where `<key>` is `RWS7wuC0DnGGHP2i5pQqa+6i1+2jlKAAKZy2lTZE7Oowjpj+Q20SM8bk` (or the backup key `RWRnKVDQsYSi5wxWs3QDeC6a7oytrgvwWKsqOxGS0IUMwkw8CGTsF9lL`). The manifest lists the SHA-256 of every file in the zip.

## Uninstall

1. Run `hdtext.exe`. If you added languages, **Remove** each one in the **Languages** tab. Then, in the **Font** tab, choose **Original (mod off)** and press **Apply**. This puts back the font you had before.
2. Remove the `pes6_hd_text.dll` line from `kload.cfg` (and the `translations.dll` line, if you added languages) and lower `DLL.num` by the number of lines you removed.
3. Delete `pes6_hd_text.dll`, `hdtext.exe`, `hdtext.cfg`, `translations.dll` (if it's there) and the `HD_*.bin` fonts in `Kitserver\GDB\fonts`. Keep the `backup` folder there: it has your previous fonts.
4. Delete `Kitserver\pes6pkg` (signed lists and backups) and, if you like, `%LOCALAPPDATA%\pes6pkg\state.json`.

Don't leave an HD font installed without the DLL: the game still loads it, but without the DLL it draws every letter at the font's HD size, so all text comes out several times too big.

## How the mod handles each font

When the game loads a font, the mod compares its size with the original size of that font (the text font, entry 53, is 16x16 per letter cell):

- **Original size** (the game's font or your patch's font): each piece of text is made sharp at 2x.
- **Bigger, so it's an HD font:** the game is handed a copy shrunk back to the original size, so it measures and places every text exactly as always, and the HD letters are what ends up on screen.
- **HD at 4x or more** (like the 35 included): each text is built at 4x and then sized to exactly the pixel density of your screen.
- **Smaller than the original, or unreadable:** left as it is.

Any scale works (2x, 3x, 4x, even non-integer), with grey, coloured or black-outlined palettes, 16 or 256 colours, and for any of the game's fonts, not only the text font. With 4x fonts the game's letter-pair spacing table is turned off, so letters drawn from a TTF don't stick together.

### Installing a font by hand

Copy the `.bin` to `Kitserver\dat\0_text.afs\` as `unnamed_53_<anything>.bin` and make sure no other `unnamed_53*` or `unknow_00053*` file is there. That is all the tool does, plus the backup.

## For font makers

If you make fonts for PES 6, HD versions are very welcome:

- Same format as the game's font file (`0_text.afs` entry 53 for the text font), with the same letter table.
- 16 colours, and every letter cell at an integer multiple of the original (2x, 3x, 4x...). 4x gives the best result.
- For a widescreen look, draw the letters 0.75 times as wide: the game stretches its menus from 4:3 to 16:9.

[Pes6FontCreator](https://pes6fontcreator.com/en/) makes fonts in this format from any TTF or OTF font, in your browser. "Add font..." in the tool checks all of this and says what is wrong. Share yours in an [issue](https://github.com/angelballay/pes6-hd-text/issues) and it can join the next version, with your credit.

## For mod makers: hooked functions

Each hook is a 5-byte jump at the start of a function of `pes6.exe` (PC); if the instructions it overwrites are longer, the rest is filled with NOPs (**Bytes**). Every hook calls the original function and none of them replaces it: **Runs** says whether the mod's code runs before the original, after it, or both. Before writing, the mod checks that the original bytes are there; if another mod already changed one of these spots, it skips that part (or does nothing at all) and the game keeps running. In "Original" mode nothing is hooked. If your mod hooks any of these, let's coordinate in an [issue](https://github.com/angelballay/pes6-hd-text/issues).

| Address | Group | Bytes | Runs | What the game does there | Why PES6 HD Text hooks it |
|---|---|---|---|---|---|
| `0x0087A810` | Required | 7 | before | TexAdd: every image enters the texture system | marks which images are text |
| `0x0040C270` | Required | 7 | before and after | builds a Direct3D texture from a game image | hands over the sharp copy |
| `0x00953350` | Required | 5 | after | creates a text object | marks the text image |
| `0x00953660` | Required | 5 | before | registers an image | follows text images |
| `0x00958FA0` | Required | 6 | before and after | rescales a text (menu labels) | sharp shrunk labels |
| `0x00958EA0` | Required | 6 | before and after | slants a text (italic labels) | sharp italic labels |
| `0x0095A1E0` | Required | 7 | after | adds a letter to a letter sheet (menus, help, outlined titles) | sharp letter sheets |
| `0x0094D920` | HD fonts | 6 | after | a font finished loading | HD font detection |
| `0x0094DD20` | HD fonts | 5 | before | a font is freed | gives the game back its own font data |
| `0x00959520` | HD fonts | 10 | after | prepares a font's letter-pair spacing | turned off for 4x fonts |
| `0x00959780` | Letter sheets | 8 | before (only notes its arguments) | draws a letter into a letter sheet | keeps the sharp sheet in step |
| `0x008D18C0` | Letter sheets | 8 | before | copies pixels into an image | keeps the sharp sheet in step |
| `0x00953080` | Shadow text | 10 | after | composes the image of a text, letter by letter | rebuilds shadow text with sharp letters |
| `0x0095A6C0` | Freed sheets | 5 | before and after | releases a letter from a letter sheet, and frees the sheet when it is empty | lets go of the sharp copy of a freed sheet |
| `IDirect3DDevice8::EndScene` (method 35 of the device table) | Update notice | — (table entry, not code) | before | ends a frame | draws the 6-second update notice |

Groups:

- **Required:** if any of these has different bytes, the mod installs nothing.
- **HD fonts:** hooked together. Without them there are no HD fonts, but the game's font is still sharpened.
- **Letter sheets:** hooked together. Without them the sharp sheet is still built, a bit later, and the selected menu option may flicker.
- **Shadow text:** on its own. If it can't be hooked, only the letter-by-letter rebuild of shadow text is turned off.
- **Freed sheets** (since 1.0.1.2): on its own. If it can't be hooked, the mod keeps up to 64 sharp sheets and, when it needs room, drops the one used least recently.
- **Update notice** (since 1.0.2): the only hook outside `pes6.exe` and the only temporary one. While the notice is on screen (six seconds, at most once a day, only when there is a new version), the mod points entry 35 of the Direct3D 8 device table to its own function, which draws the notice and then calls whatever was there before (d3d8, a wrapper such as dgVoodoo, or another mod). When the notice ends, it puts the previous entry back, unless another mod changed the entry in the meantime: then it stays in the chain and just passes through.

**If another mod already hooked one of these functions** (since 1.0.1.1): when a spot starts with a plain 5-byte jump (`E9`) into another module and the rest of the original bytes are intact, PES6 HD Text chains to it instead of turning off. Our code runs first, then the other mod's, then the game's. Any other change at a spot is left alone, as before. If your mod is loaded after ours and finds our jump there, please chain to it the same way instead of refusing to hook.

It also calls Direct3D 8 `CreateTexture` on the game's device (no hook there). [Change Physics Game](https://github.com/angelballay/pes6_game_physics_mod) hooks `0x005A5905`, `0x005A637B`, `0x005ADEC9`, `0x005AF6D6`, `0x005AFB43` and `0x0047810D`: no overlap, and both run together in The Den Patch 2026.

## Compatibility

- Tested on the **original PES 6** + Kitserver 6.
- Tested on **PES 6 The Den Patch 2026**, together with its 26 other Kitserver modules, including [Change Physics Game](https://github.com/angelballay/pes6_game_physics_mod).
- Works together with PES6 Flags Module (`flags6.dll`, HD crests; tested with v4).
- Works together with **PesAssetLoader**, the Plugin Loader and Asset Loader by Dmitri-F (since 1.0.1.1; tested with an HD font and with HD crests loaded by the Asset Loader).
- Before changing anything, the module checks the game code where it hooks. If your `pes6.exe` is different, it does nothing and the game runs as usual.
- In "Original" mode the DLL hooks nothing: the game is exactly as without the mod.
- Sharp copies use at most 64 MB of memory with the game's own fonts, plus up to 64 MB more with HD fonts.

**With PES6 Flags Module** (original PES 6, flags6 v4 and the HD_wide font): the HD crests and the team acronyms (FCB, RMA) come from flags6, the text from PES6 HD Text.

![Team selection: HD crests from PES6 Flags Module and HD text from PES6 HD Text](images/1.0.1/flags6-team-select.png)

![Match menu: team acronyms from PES6 Flags Module and HD text from PES6 HD Text](images/1.0.1/flags6-match-menu.png)

## Known limitations

- **Text only.** Graphics that are images stay as they are: the title screen ("Press any button"), logos, icons, menu widgets and the scoreboard numbers (they are part of a texture).
- **Big outlined titles keep the game's original outline,** so letters that overlap slightly in the original still overlap (now sharp).
- **Not a widescreen fix:** the menu layer is still 4:3, stretched to your screen.
- **Chinese and Japanese versions** of the game aren't supported yet. To add them I need the game in that language (a zip of the game or its `dat` folder) to see how its text works. If you have one, please open an [issue](https://github.com/angelballay/pes6-hd-text/issues).

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

Thanks to **SimoneZ**: `HD_original_font` is based on their work (Roboto, Apache 2.0).

## License

[MIT](LICENSE), with one extra condition: any patch, mod or project that includes or reuses PES6 HD Text, fully or partly, must show this line in its credits: *"Mod PES6 HD Text Original creado por PityCharly."*

The included HD fonts are modified versions of free fonts (SIL Open Font License and Apache 2.0). The download lists each one with its source font and license in `Kitserver\GDB\fonts\FONT_LICENSES.txt` (also in [fonts/FONT_LICENSES.txt](fonts/FONT_LICENSES.txt) in this repo).

## Feedback

Found a screen where the text is still blurry? Open an [issue](https://github.com/angelballay/pes6-hd-text/issues) with a screenshot and the patch you use.

## About the author

I'm **pitycharly**, an Argentine software developer who makes mods for PES 6. I want to help keep this game alive, and I'd love to see my mods inside the patches people already play. I build them as Kitserver modules and keep them compatible with all the existing ones.

My other mod:

- **[Change Physics Game](https://github.com/angelballay/pes6_game_physics_mod)** (v1.1): first-time passes no longer die on the pitch. A faster pass impulse makes the ball roll faster and more smoothly. Tested on the original PES 6 and on PES 6 The Den Patch 2026. [Video](https://www.youtube.com/watch?v=KKfPKn4rNsg) · [Download](https://www.mediafire.com/file/fwqcw1omr98uekw/1.1_pes6_game_physics_mod.zip/file)

---

## Español

**El texto de PES 6, nítido en HD: mismas fuentes, mismo diseño, y anda con cualquier parche.**

Los menús, los nombres de jugadores y de equipos y los títulos se ven nítidos en lugar de borrosos y estirados. El juego sigue usando sus posiciones: nada se mueve ni se corta. Podés quedarte con la fuente de tu juego, ahora nítida, o elegir una fuente HD.

**▶ [Video (4 min, narración en inglés con subtítulos en español): antes y después, instalación, el selector y las 35 fuentes](https://www.youtube.com/watch?v=AISb6npriI4)**

### 🎨 Hacé tu propia fuente HD, directo en el navegador

**[Pes6FontCreator](https://pes6fontcreator.com/) convierte cualquier fuente TTF u OTF en una fuente HD para PES6 HD Text.** Cargás tu fuente, completás las letras que le faltan (automáticamente o una por una) y descargás tu `HD_<nombre>.bin`. Después abrís `hdtext.exe` → **Add font...** → **Apply**. No hay que instalar nada y no se sube nada: todo pasa en tu navegador.

**[✏️ Creá tu fuente en pes6fontcreator.com](https://pes6fontcreator.com/)**

**Novedades de la 1.0.2** (lista completa en el [changelog](CHANGELOG.md)):

- **1.0.2.1:** la pestaña **Languages** dice claro que carga el `.zip` del idioma tal como lo descargaste, sin descomprimirlo, y qué cargar si elegís otra cosa (la carpeta descomprimida, un archivo de adentro, otro zip).
- **Instalador:** extraés el zip, abrís `Kitserver\hdtext.exe` desde ahí, elegís la carpeta de PES6 y tocás **Install** (o **Update** sobre una versión anterior).
- **Actualizaciones desde `hdtext.exe`:** cuando hay una versión nueva, el juego muestra un aviso corto y `hdtext.exe` la instala con **Update to …**, comprobando antes la firma del autor. **Go back** vuelve a la anterior.
- **Idiomas:** la pestaña nueva **Languages** carga los idiomas de la [sección Traducciones de la web](https://pes6fontcreator.com/translations/) en el menú de idiomas del juego, en la carpeta que el juego lee de verdad.
- **Letras griegas, cirílicas y más latinas** en las fuentes incluidas (`HD_original_font`, `HD_fira_sans` y `HD_humanist` las tienen todas).
- **Arreglo:** los números de habilidad vuelven a quedar alineados con las fuentes HD.

**1.0.1.2:** el texto de los menús sigue nítido en sesiones largas, como la Liga Master. Después de un partido y un rato de menús, las opciones y los nombres de los jugadores podían salir borrosos; ya no. Además, `HD_original_font` dibuja sus símbolos en HD (℃ ← ↑ → ↓ □ ■ △ ▲ ○ ● ★). Y para hacer tu propia fuente HD: [Pes6FontCreator](https://pes6fontcreator.com/) convierte cualquier fuente TTF u OTF en una fuente HD para PES6 HD Text, en el navegador. ¿Ya tenés una versión anterior? Mirá la instalación más abajo.

**1.0.1.1:** anda junto con PesAssetLoader (el Plugin Loader y Asset Loader de Dmitri-F). Con la 1.0.1, PES6 HD Text se apagaba si estaba instalado y, con una fuente HD, el texto salía gigante.

**Novedades de la 1.0.1** (lista completa en el [changelog](CHANGELOG.md)):

- **Fuentes HD:** con una fuente HD el texto se dibuja a la resolución de tu pantalla en lugar de estirarse desde 640x480 (probado a 1920x1080).
- **35 fuentes HD incluidas:** `HD_original_font` mantiene el aspecto del PES 6 original, y otras 34 cambian el estilo, desde fuentes limpias hasta pixel, marcador, esténcil, cómic o neón.
- **`hdtext.exe`, una herramienta de configuración:** activa o apaga el mod, elige la fuente con vista previa, agrega tus propias fuentes y vuelve a la que tenías antes.
- **Letras más prolijas con las fuentes del juego:** las fuentes finas conservan sus trazos, las letras cortadas se reparan y las redondas salen simétricas.
- **Más texto nítido:** opciones de los menús, textos de ayuda y las etiquetas achicadas o en cursiva.
- **Arreglo:** los escudos, las banderas y los íconos ya no se tocan por error, y el PES6 Flags Module (`flags6.dll`, escudos HD) ya anda junto con el mod.

**Instalación** (requiere Kitserver 6 con `afs2fs.dll` cargada en `kload.cfg`):

El zip es el mod completo, no un parche: no hace falta ninguna versión anterior.

**Con el instalador (recomendado):**

1. Descargá `PES6_HD_Text_v1.0.2.1.zip` desde [Releases](https://github.com/angelballay/pes6-hd-text/releases/latest) y extraé el zip entero (clic derecho → **Extraer todo**). No abras nada desde adentro del zip.
2. Hacé doble clic en `Kitserver\hdtext.exe`, en la carpeta extraída: es el instalador.
3. Revisá la carpeta de PES6 que propone (o tocá **Browse…**) y tocá **Install**. Sobre una versión anterior (de la 1.0 a la 1.0.2) el botón dice **Update**: tu configuración y tus fuentes se conservan.
4. Se abre el `hdtext.exe` instalado: elegí una fuente y apretá **Apply**.
5. A jugar.

El instalador comprueba cada archivo contra la lista firmada por el autor, guarda una copia de lo que reemplaza y agrega la línea a `kload.cfg` (con una copia del anterior en `Kitserver\pes6pkg\backup\kload.cfg\`). Si tu `kload.cfg` tiene un formato raro, no lo toca y te dice la línea a agregar. ¿Querés comprobar que el zip es el del autor? Antes de la primera instalación, compará su SHA-256 con el de la [página del release](https://github.com/angelballay/pes6-hd-text/releases): `certutil -hashfile PES6_HD_Text_v1.0.2.1.zip SHA256`.

**A mano:** copiá todo lo que está dentro de la carpeta `Kitserver` del zip en la carpeta Kitserver del juego (la que tiene `kload.cfg`), agregá en `kload.cfg` una línea después de la última `DLL.N`, con el número siguiente (por ejemplo `DLL.26 = "kitserver\pes6_hd_text.dll"`), sumale 1 a `DLL.num`, abrí `Kitserver\hdtext.exe`, elegí una fuente y apretá **Apply**. Si ya tenías una versión anterior, dejá la línea que ya tenés en `kload.cfg` (no agregues otra).

**Elegir la fuente:** en `hdtext.exe`, **HD** activa el mod con la fuente que elijas de la lista, y **Original (mod off)** lo apaga y vuelve a poner la fuente que tenías antes. Cada fuente reemplazada queda guardada en `Kitserver\GDB\fonts\backup`. Las 35 fuentes HD también están en la carpeta [fonts](fonts) de este repo, con sus licencias.

**Con la fuente de tu parche:** abrí `hdtext.exe` y elegí:

- **Tu fuente, nítida (x2):** dejá **HD** y la fuente elegida como están y apretá **Apply** (la que usás ya aparece seleccionada).
- **Una fuente HD:** **HD**, elegí una `HD_…` y **Apply**. La de tu parche queda guardada en la lista.
- **Volver a tu fuente, nítida:** **HD**, volvé a elegirla y **Apply**.
- **Volver a tu fuente, sin el mod:** **Original (mod off)** y **Apply**. Vuelve tal como la tenía el parche y el mod deja de hacer cosas.

En la lista, la fuente de tu parche es **"Game font"** si el parche la trae dentro de los archivos del juego (como The Den Patch 2026), o **"Font before PES6 HD Text"** si la instaló con Kitserver.

**Idiomas:** PES6 HD Text no trae traducciones. En `hdtext.exe` → **Languages**: descargá el `.zip` del idioma en la [web](https://pes6fontcreator.com/translations/) (el enlace **Get it ↗** de cada idioma abre su página) y, sin descomprimirlo, cargalo con **Load a language file (.zip)…** (o soltalo sobre la ventana; podés cargar varios a la vez). Después elegí el idioma en la pantalla de idiomas del juego. **Use** pone otro idioma instalado en el menú, **None** deja solo los del juego y **Remove** borra uno. El idioma se instala en la carpeta `dat` que el juego lee de verdad (la de la clave de registro de tu `pes6.exe`, que en los parches y las copias del juego puede ser otra); la pestaña dice cuál es y, si no es la carpeta que elegiste, pregunta antes. Cada archivo de idioma trae el complemento PES6 Translations (`Kitserver\translations.dll`), que `hdtext.exe` instala y mantiene al día. La fuente del juego no tiene griego ni cirílico: cuando un idioma entra al menú y a tu fuente le faltan letras suyas, `hdtext.exe` pregunta en ese momento; **Use Original style** pasa a `HD_original_font`, que las tiene todas, y **Keep my font** la deja (la pestaña dice qué letras faltan). Con un idioma en el menú, **Apply** también avisa antes de pasar a una fuente a la que le faltan letras suyas. Tienen todas, para el ruso, `HD_original_font`, `HD_fira_sans`, `HD_humanist`, `HD_montserrat`, `HD_oswald` y `HD_rubik`; para el griego, `HD_original_font`, `HD_fira_sans` y `HD_humanist`.

**Actualizaciones:** cuando el juego arranca en modo HD, el mod consulta como mucho una vez por día un archivo firmado (el índice de [pes6-package-pc](https://github.com/angelballay/pes6-package-pc)); no manda nada tuyo. Si hay una versión nueva, muestra un aviso abajo a la izquierda durante seis segundos. En `hdtext.exe`, el recuadro **Updates** la instala con **Update to …** (con el juego cerrado, comprobando la firma y cada archivo; tu configuración y tus fuentes se conservan) y **Go back to …** vuelve a la anterior. La DLL del juego nunca descarga ni instala nada. Para apagar los avisos, destildá "Show update notices (here and in the game)" y apretá **Apply**; **Check now** sigue andando. Los detalles, en inglés, en [Updates](#updates).

**Desinstalar:** en `hdtext.exe`, si agregaste idiomas, borralos con **Remove** en **Languages**; después, en **Font**, elegí **Original (mod off)** y apretá **Apply**. Borrá la línea de `pes6_hd_text.dll` de `kload.cfg` (y la de `translations.dll`, si agregaste idiomas), bajá `DLL.num` en la cantidad de líneas que borraste y borrá `pes6_hd_text.dll`, `hdtext.exe`, `hdtext.cfg`, `translations.dll` (si está), la carpeta `Kitserver\pes6pkg` y las fuentes `HD_*.bin` de `Kitserver\GDB\fonts` (dejá la carpeta `backup`: tiene tus fuentes anteriores). No dejes una fuente HD instalada sin la DLL: el juego la carga igual, pero sin la DLL dibuja cada letra al tamaño HD de la fuente y todos los textos salen varias veces más grandes.

**¿Hacés fuentes o mods?** Las fuentes HD son bienvenidas: el formato está en [For font makers](#for-font-makers). Si tu mod engancha alguna función del juego, fijate la lista en [For mod makers](#for-mod-makers-hooked-functions) y coordinemos para no pisarnos.

**Probado** en PES 6 original + Kitserver 6 y en PES 6 The Den Patch 2026, en español, y junto con el PES6 Flags Module y con PesAssetLoader; como trabaja sobre el texto que dibuja el juego, no depende del idioma. Gracias a **The Den** por *PES 6 The Den Patch 2026*. **Limitaciones:** solo cambia el texto (la pantalla de título, los logos, los íconos y los números del marcador son imágenes y quedan igual), el contorno de los títulos grandes es el original y no es un parche de pantalla ancha. Las versiones china y japonesa del juego todavía no están soportadas: para sumarlas necesito el juego en ese idioma (un zip o su carpeta `dat`); si lo tenés, abrí un [issue](https://github.com/angelballay/pes6-hd-text/issues).

**Licencia:** [MIT](LICENSE) con una condición de atribución. Si lo incluís en un parche, poné en los créditos: *"Mod PES6 HD Text Original creado por PityCharly."* Las fuentes HD incluidas son versiones modificadas de fuentes libres (SIL Open Font License y Apache 2.0); el detalle está en `Kitserver\GDB\fonts\FONT_LICENSES.txt` dentro de la descarga.

¿Una pantalla donde el texto se sigue viendo borroso? Abrí un [issue](https://github.com/angelballay/pes6-hd-text/issues) con una captura.

Soy **pitycharly**, desarrollador de software argentino, y hago mods para PES 6 para mantenerlo vivo. Mi otro mod: **[Change Physics Game](https://github.com/angelballay/pes6_game_physics_mod)**, para que los pases al primer toque no se mueran ([video](https://www.youtube.com/watch?v=KKfPKn4rNsg)).
