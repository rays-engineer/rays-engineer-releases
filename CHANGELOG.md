# Changelog

All notable changes to Rays Engineer. The app shows this file under Settings › Changelog, and each
release publishes its version's section as the release notes.

<!--
Format (parsed by Rays_Engineer.Desktop/src/shared/changelog.ts):
  ## [Unreleased]            changes on main that are not released yet
  ## [1.2.0] – 2026-11-05    one section per release, newest first
  ### Added | Changed | Fixed | Removed
  - one line per change (`code` and **bold** are allowed)
Before creating release/x.y.z, rename [Unreleased] to [x.y.z] – <date>; the release fails
without a section for its version.
-->

## [0.0.1] – 2026-10-31

### Added

- **Le Mans Ultimate**: finds LMU's telemetry folder, watches it and indexes new recordings.
- **Assetto Corsa, ACC and Assetto Corsa Rally**: the app records them live from the games' shared memory. Pick the game on start (or set a startup game in Settings) and switch it in the sidebar; sessions, references and settings are kept per game.
- AC Rally stage runs with corners from the game's own pacenotes.
- ACC: the app measures the lap length itself, so analysis by distance works.
- AC, ACC and AC Rally recordings keep **every value the game sends**: DRS, ERS, KERS, TC/ABS, engine map, fuel, damage, tyre wear and temperatures (inner/middle/outer) and more, as extra channels in Analysis › **+ Channel** (with a filter). Values a car does not have are left out.
- Raw capture on the Recording page and in Settings › Diagnostics, to verify the games' data formats.
- Sessions with laps, official lap times, validity and sector times; notes and tags.
- Reference lap per game + track + car (fastest valid lap).
- Analysis by distance against the reference: delta, speed, throttle, brake, steering, gear and any other recorded channel.
- Track map and corner table.
- Analysis tabs **Corner map**, **Consistency**, **Balance** and **Setup**.
- Gear choice analysis per corner.
- **Tyres per lap** in the Conditions panel: the compound (AC, ACC with the tyre set; LMU from the setup, with tyre changes in the pits) and the tyres' condition (LMU, AC); laps on other tyres are highlighted, and the Setup tab's fair-test check uses the compound. Claude sees both too.
- Export and import of sessions (`.rses`) and single laps (`.rlap`).
- Live voice feedback: a race-engineer call after every valid lap (AC, ACC) and a debrief after each rally stage (AC Rally), German or English, optionally with local Piper voices.
- Claude integration: Claude Desktop or Claude Code on the same PC can analyse your laps and save tips as notes (Settings › Claude).
- Changelog under Settings › Changelog.
- **Report a bug (Discord)** and **Downloads** in Settings › About; they open in your browser.
