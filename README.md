# Workout Calendar

A simple workout and period tracker for phones. It is a single web page that works offline and keeps all data on the device.

## Features

- Monthly calendar, Monday first. Tap a day to add or remove workouts.
- Your own workout list (starts with "gym" and "gravity").
- Mark period days and add a short note per day.
- Monthly count per workout and of period days.
- Export everything as a CSV file (date, weekday, exercises, note, period).

## Use it on a phone

1. Host the repo with GitHub Pages: Settings → Pages → Deploy from a branch → `main`, `/ (root)`.
2. Open the Pages link once while online.
3. Add it to the home screen:
   - iPhone: Safari → Share → Add to Home Screen
   - Android: Chrome → ⋮ → Add to Home screen

After that it opens from the icon, with or without a connection.

## Data

Data is stored in the browser's local storage on each phone. Nothing is uploaded and nothing syncs between devices. Clearing the browser's site data erases it, so export now and then as a backup.

## Development

No build step. Serve the folder and open it:

```bash
python3 -m http.server 8000
```

When you change any file, bump `VERSION` in `sw.js` so phones drop the old offline copy.

## Files

- `index.html`: the whole app (markup, styles, script)
- `sw.js`: offline support
- `manifest.webmanifest`, `icons/`: home-screen install
- `fonts/`: bundled Caveat and Inter (SIL Open Font License)
