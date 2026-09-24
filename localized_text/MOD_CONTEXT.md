# Shadow Fleet Mod - Context & Conventions
As a translator i take keys from the de.localized_text and match them against the other *.localizd-files
## Localization Strategy
- **Reuse game assets**: Icon references like `advent_max_supply_0_research_subject_hud_icon` point to existing game textures
- **Reference game keys**: Files like `sf1_quick_start_mode.start_mode` reference original game localization keys (e.g., `start_mode.quick.name`)
- **Only localize custom content**: Custom research subjects and new features get full localization entries

### Existing Content
- Localization files: 15 languages ( ISO 3166 country codes en, de, es, fr, hu, id, it, ja, ko, pl, pt_br, ru, th, tr, zh_cn)

## Localization Language Codes (ISO-639)
- de, en, es, fr, hu, id, it, ja, ko, pl, pt_br, ru, th, tr, zh_cn

## Translation Workflow
1. **Edit German source**: Modify `de.localized_text` with German text for new/changed keys
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
- Expand with more units/structures
- Finalize starbase ability (remove `.try` when ready)
- Consider creating as independent race (vs. Trader variants)
- **Translations**: Request language support across all 15 languages when new content needs localization
