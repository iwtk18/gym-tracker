# Gym Tracker

A personal workout tracking app built to plan sessions, log exercises and track progress over time. Runs entirely in the browser with no account or internet connection required at the gym.

Live at: [your-url.netlify.app](https://your-url.netlify.app)

---

## What it does

- **Plan** reusable workout templates with exercises, sets, reps and weights
- **Track** active sessions in real time, then complete or abandon them
- **Log** both weights and cardio exercises (duration + distance) in the same session
- **Review** history with a timeline view and a per-exercise progress view
- **Analyse** volume, personal bests, most trained exercises and progression charts in Stats
- **Filter** history and stats by year and month
- **Back up** and restore all data via JSON export and import

## How it's built

A single HTML file — no frameworks, no build tools, no backend. All data is stored locally in the browser using `localStorage`. Works offline once loaded.

| File | Purpose |
|------|---------|
| `index.html` | The entire app — HTML, CSS and JavaScript in one file |
| `manifest.json` | Tells iOS/Android how to install it as a home screen app |
| `sw.js` | Service worker — caches the app for offline use |
| `icon.svg` | Home screen icon |

## Features

- Weights and cardio support in the same workout
- Per-exercise type toggle (Weights / Cardio) when building plans
- Auto title-case and fuzzy match warning to prevent duplicate exercise names
- Exercise library with duplicate detection, quick-select and inline rename
- Plan copying, editing and one-time use (removed from My Plans on completion)
- Abandoning a workout restores the plan to My Plans
- Global workout numbering (#1, #2, #3...)
- Year and month date filters on History and Stats
- Progression chart per exercise (top weight or duration per session)
- Data export and import via JSON backup file
- Ember dark theme
- iPhone safe area support (no clash with status bar)
- In-app changelog accessible via the version badge

## Data and privacy

All workout data is stored locally on your device in the browser's localStorage. No data is sent to any server. GitHub and Netlify only host the app files — they have no access to your workout history.

Because data lives on your device, it is worth exporting a backup regularly using the Export button in the Stats tab. Save the file to iCloud or similar so it is not lost if you clear your browser or switch devices.

## Deploying updates

When the app is updated, download the new `index.html` (and any other changed files) and upload them to this repository via **Add file → Upload files**. Netlify will detect the change and redeploy automatically within about 30 seconds.

Commit message format used in this project:

```
Add [feature]
Fix [bug]
Update [thing]
```

## Version history

| Version | Date | Summary |
|---------|------|---------|
| v1.1 | Mar 2026 | Cardio support, exercise library, changelog overlay, date filters, data export/import |
| v1.0 | Mar 2026 | Initial release |
