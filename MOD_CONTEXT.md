# Shadow Fleet Mod - Context & Conventions

## Project Overview
- **Game**: Sins of a Solar Empire 2 (Sins2)
- **Mod Path**: `c:\Users\a_hen\AppData\Local\sins2\mods\shadow_fleet`
- **Status**: v0.0.3 - Adding new player factions (Corsairs & Smugglers)

## Mod Structure & Conventions

### Key File Naming Patterns
- `.try` extension = Template/work-in-progress files (do NOT include in localization)
- Prefixed start modes: `sf1_*.start_mode` (copies of game's original files with new faction configs)
- new race factions: `sf1_shadow_rebel.player` and `sf1_shadow_loyalist.player`

### Localization Strategy
- **Reuse game assets**: Icon references like `advent_max_supply_0_research_subject_hud_icon` point to existing game textures
- **Reference game keys**: Files like `sf1_quick_start_mode.start_mode` reference original game localization keys (e.g., `start_mode.quick.name`)
- **Only localize custom content**: Custom research subjects and new features get full localization entries

### Current Localization Status (v0.0.3)
✅ Complete:

🔲 Not yet:

### Existing Content
- 2 player factions (Corsairs, Smugglers) - variants of Trader race
- 2 civic research subjects (one per faction)
- 4 start modes (Quick, Basic, Normal, Advanced)
- Localization files: 15 languages (en, de, es, fr, hu, id, it, ja, ko, pl, pt_br, ru, th, vie, zh_cn)

## Localization Language Codes (ISO-639)
- en, de, es, fr, hu, id, it, ja, ko, pl, pt_br, ru, th, zh_cn
- vie wurde entfernt.

## Translation Workflow
1. **Edit German source**: Modify `localized_text/de.localized_text` with German text for new/changed keys
2. **Commit to Git**: Push your German changes with a descriptive commit message
3. **Request sync**: Tell me which keys were added/changed in German
4. **Auto-translate**: I translate those keys to all 14 other languages and update their respective `.localized_text` files
5. **Commit translations**: All translated files are committed together

This ensures German is the source language and all translations stay synchronized.

### Translation Process Notes
- Use the exact same key structure from `de.localized_text` in all language files
- Replace only the German **text values** with translations for each language
- Preserve JSON formatting, tabs/spaces, and the trailing "end" key
- When replacing, match the exact context including surrounding lines to avoid mismatches
- All 15 language files must have identical keys; only the values differ

## Next Development Areas
Incorporation of the new entries for Update to release 2.0 .