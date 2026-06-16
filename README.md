# Moondew Canyon html build

Version: 0.1.0-dev
Source commit: bb753c9
Prepared: 2026-06-16

## Changes

### Assets
- Added separated Craftpix grassland object sprite scenes for map props with starter collision on solid objects.
- Added layered strong smack impact sounds for player hits with a separate volume control.
### Gameplay
- Added a player movement tuning parameter for how long the player can stand still before sprint toggles off.
- Cleaned up player and slime tuning ownership by making wrapper resources explicit, moving sound pools into audio tuning resources, and using real-time player attack timing that preserves the current swing feel.
- Added a slime knockback distance cap so charged hits that also trigger stagger do not launch enemies too far.
- Fixed queued attack input so holding attack during rapid swings transitions into wave charge immediately when the current swing unlocks instead of forcing another basic attack or waiting on the tap/hold threshold.
### Fixed
- Kept charged attack wave visuals advancing during hitstop so enemy hits do not delay the released wave animation.
### Documentation
- Added project instructions to keep this changelog updated and include build README summaries from it.
- Added project version metadata, release preparation guidance, and a release-style changelog structure.
### Tools
- Added a platform build preparation helper that archives existing local build files and writes a build README from versioned changelog notes.
- Updated validation CI to parse all first-party GDScript files instead of a fixed script list.
