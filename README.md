# Superssential Admin Panel (AdminUI)

A lightweight admin panel for Hytale with a black/transparent theme, cleaned-up navigation, and built-in server tools.

## Features
- Players: view players, heal/kill, teleport/teleport here, kick, ban, open inventory.
- Whitelists & Bans: manage entries quickly.
- Warps & Backups: access existing warp/backup pages.
- Stats: server stats page.
- Commands tab:
  - Sleep controls: skip night, set required sleep ratio (0–100%) or player count, custom input + save; chat feedback on actions.
  - Welcome message: toggle on/off, set prefix (yellow) and message (green), save per server; shows privately on player join.
- UI polish: "Superssential Panel" title everywhere, transparent buttons, no back buttons, navbar order: Players, Whitelists, Bans, Warps, Backups, Stats, Commands.

## Command / Admin entry
- In game: `/admin` to open the panel.

## Build & Install
1. From `AdminUI-main`, build the jar:
   ```bash
   ./gradlew clean build jar
   ```
2. Drop the jar from `build/libs` into your server plugins folder.
3. Restart the server.

## Using the Commands tab
- Sleep Controls (collapsed by default):
  - Skip Night Now.
  - Set sleep requirement to 25%, 50%, 0%, or 1 player.
  - Custom: enter percent (e.g., `30%`) or count (e.g., `2`) and Save. Chat shows feedback.
- Welcome Message:
  - Enable/disable, set prefix and message, Save. On player join, prefix is yellow and message is green.

## Persistence
- Sleep settings: `sleep-settings.properties` in the plugin data folder.
- Welcome settings: `welcome-settings.properties` in the plugin data folder.

## Notes
- Sleep logic is implemented locally (no external MassSleep dependency) and ticks every second to skip night when thresholds are met.

## License
Add your preferred license here.
