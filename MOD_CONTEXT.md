# Shadow Fleet Mod - Context & Conventions

## Project Overview
- **Game**: Sins of a Solar Empire 2 (Sins2)
- **Mod Path**: `c:\Users\a_hen\AppData\Local\sins2\mods\Shadow_fleet`
- **Status**: v0.0.3 - Adding new player factions (Corsairs & Smugglers)

## Mod Structure & Conventions

### Key File Naming Patterns
- `.try` extension = Template/work-in-progress files (do NOT include in localization)
- Prefixed start modes: `sf1_*.start_mode` (copies of game's original files with new faction configs)
- Faction variants: `trader_corsair.player` and `trader_smuggler.player`

### Localization Strategy
- **Reuse game assets**: Icon references like `advent_max_supply_0_research_subject_hud_icon` point to existing game textures
- **Reference game keys**: Files like `sf1_quick_start_mode.start_mode` reference original game localization keys (e.g., `start_mode.quick.name`)
- **Only localize custom content**: Custom research subjects and new features get full localization entries

### Current Localization Status (v0.0.3)
✅ Complete:
- `trader_corsair_civic_lore_0_research_subject_*` (3 keys)
- `trader_smuggler_civic_lore_0_research_subject_*` (3 keys)

🔲 Not yet:
- `trader_starbase_self_destruct_*` (pending finalization, currently in `.try` file)

### Existing Content
- 2 player factions (Corsairs, Smugglers) - variants of Trader race
- 2 civic research subjects (one per faction)
- 4 start modes (Quick, Basic, Normal, Advanced)
- 1 starbase ability (self-destruct) in template form
- Localization files: 15 languages (en, de, es, fr, hu, id, it, ja, ko, pl, pt_br, ru, th, vie, zh_cn)

## Localization Language Codes (ISO-639)
- en, de, es, fr, hu, id, it, ja, ko, pl, pt_br, ru, th, vie, zh_cn

## Translation Workflow
1. **Edit German source**: Modify `localized_text/de.localized_text` with German text for new/changed keys
2. **Commit to Git**: Push your German changes with a descriptive commit message
3. **Request sync**: Tell me which keys were added/changed in German
4. **Auto-translate**: I translate those keys to all 14 other languages and update their respective `.localized_text` files
5. **Commit translations**: All translated files are committed together

This ensures German is the source language and all translations stay synchronized.

## Next Development Areas
- Expand with more units/structures
- Finalize starbase ability (remove `.try` when ready)
- Consider creating as independent race (vs. Trader variants)
- **Translations**: Request language support across all 15 languages when new content needs localization
