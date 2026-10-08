# Subtitles.gr — Context Menu Item

Global context-menu companion for the [Subtitles.gr subtitle service](https://github.com/Twilight0/service.subtitles.subtitles.gr).

Adds a single **Subtitles.gr: Context Menu** submenu to Kodi's core context menu (`kodi.core.main`), so subtitle actions are available from any playable item without opening the fullscreen video OSD.

- Addon id: `context.subtitles.gr`
- Author: Twilight0
- License: GPL-3.0-only
- Kodi: Omega (v21) and later, Python 3
- Requires: `service.subtitles.subtitles.gr` (installed automatically as dependency)

## Context menu entries

All entries appear only on non-folder items (`!ListItem.IsFolder`), i.e. playable movies, episodes and videos:

| Entry | What it does | Implementation |
|---|---|---|
| Check subtitle availability for given item | Opens Kodi's subtitle search window (`ActivateWindow(subtitlesearch)`) for the selected item | `resources/lib/check_sub.py` |
| Open settings menu | Opens the settings dialog of `service.subtitles.subtitles.gr` | `resources/lib/options.py` |
| Clear function cache | Deletes `special://profile/addon_data/service.subtitles.subtitles.gr/cache` and shows an `OK` notification | `resources/lib/clear_cache.py` |

The submenu label itself (`30003`) resolves to *Subtitles.gr: Context Menu*.

## Localization

| Code | Language |
|---|---|
| `en_gb` | English (default) |
| `el_gr` | Greek |

String ids `30001`–`30004` in `resources/language/`.

## Installation

Install from the Twilight0 repository, or download a release zip and install via Kodi's *Install from zip file*. The required subtitle service addon is pulled in automatically.

Source: <https://github.com/Twilight0/context.subtitles.gr>
