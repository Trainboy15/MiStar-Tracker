# MiStar-Tracker
Import grades and assignments from MiStar Student portal, create tasks, and be productive.

## Running

This is a static HTML app. Host `index.html` and `version.json` on the same origin (for example GitHub Pages or any static web server).  
Do not open `index.html` directly with `file://` if you want update checks to work.

## Automatic updates

- Current app version is defined in `index.html` (`APP_VERSION`).
- Update metadata is served from `version.json`.
- On load (and every 30 minutes), the app checks `version.json` for a newer version.
- If a newer version exists, the app reloads automatically when no unsaved form drafts are detected.
- If unsaved drafts exist, the app defers reload and shows an **Update now** button in **Settings → Updates**.
- Users can always run a manual update check from **Settings → Updates → Check now**.

## Release/update checklist

When publishing a new release:

1. Update `APP_VERSION` and (optionally) `APP_RELEASE_DATE` in `index.html`.
2. Update `version.json` with the same new version and release date.
3. Deploy both files together.
