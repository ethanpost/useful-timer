# Useful Timer

`Useful Timer` is a static, single-page focus dashboard built with plain HTML, CSS, and JavaScript. Open `index.html` in a modern browser and you get a fullscreen-friendly timer, a live analog clock, interval gauges, rotating backgrounds, sticky notes, a rolling timeline, and local backup/restore without any build step or server.

Everything runs in the browser and persists locally on your machine.

## Features

- Two configurable timer presets from `1` to `120` minutes
- `Start`, `Pause`, and `Reset` controls with timer state restored after reload
- Visual warning state during the last `10%` of a session plus a completion alarm
- Analog clock rendered on `<canvas>`, including a live timer progress wedge
- Three configurable interval gauges with optional bell alerts on interval changes
- Draggable timer, clock, interval panel, and timeline strip with saved positions and snap-to-grid behavior
- Built-in background gallery plus local photo uploads from the settings panel
- Sticky notes that can be created, edited, dragged, resized, closed, and merged by dropping one note onto another
- Selectable sticky-note font from multiple monospace font stacks
- Rolling two-row timeline with per-day notes, hover previews, and an inline note editor
- Backup and restore for local app data, with automatic backup writes after saving settings when a backup folder is connected
- Fullscreen toggle and keyboard background navigation with the left and right arrow keys

## Getting Started

1. Clone or download this repository.
2. Open `index.html` in a modern desktop browser.

That is the full setup.

## How To Use

1. Pick one of the two timer preset buttons and press `Start`.
2. Drag the timer, analog clock, interval gauges, or timeline strip where you want them.
3. Open `Settings` to change timer lengths, interval lengths, sticky-note font, background photos, or backup options.
4. Click empty background space to create a sticky note.
5. Drag one sticky note onto another to merge them with a timestamp separator.
6. Double-click a day in the timeline to add or edit a note for that date.
7. Use the bell button on the interval panel to enable or disable interval alerts.
8. Use the fullscreen button in the top-right corner for a cleaner display.

## Keyboard Shortcuts

| Key | Action |
| --- | --- |
| `Left Arrow` | Previous background image |
| `Right Arrow` | Next background image |
| `Escape` | Close the timeline note editor |

## Backup And Restore

The app can export and restore your local data in two ways:

- In browsers that support the File System Access API, you can choose a backup folder and the app will write `useful-timer-backup.json` there
- In browsers without that API, the backup action falls back to downloading the JSON file manually
- Restore can load from the chosen backup folder when available, or from a selected `.json` file

Backups include settings, sticky notes, timeline notes, uploaded background images, timer state, saved panel positions, bell preference, and timeline position.

## Persistence

The app stores its state locally in the current browser profile. This includes:

- timer state
- panel positions
- timeline position
- bell preference
- sticky notes
- timeline notes
- settings values
- uploaded background images

When supported, the selected backup folder handle is also stored locally with `IndexedDB` so the app can reuse it later.

## Notes And Limitations

- Uploaded photos are stored in browser storage, so very large or numerous images can hit quota limits.
- The app is optimized for desktop pointer input; touch-specific drag behavior is not implemented.
- All notes, settings, and uploaded images are local unless you explicitly create a backup file.
- Automatic folder-based backup works best in Chromium-based browsers that support the File System Access API.
- The timeline is a rolling view around the current date, not a full traditional month calendar.

## Project Structure

- `index.html` contains the app markup and all JavaScript behavior
- `site.css` contains layout, styling, and panel visuals
- `images/` contains the bundled background artwork

## Customization

- Use the in-app `Settings` panel for everyday customization
- Replace or add files in `images/` if you want different bundled backgrounds
- Edit `site.css` to change typography, layout, glassmorphism, and note styling
- Edit the inline script in `index.html` if you want to change app behavior

## Browser Requirements

Use a modern browser with support for:

- `localStorage`
- `IndexedDB`
- `<canvas>`
- the Fullscreen API
- the Web Audio API
- `FileReader`

Optional features use:

- the File System Access API for choosing a backup folder and saving backups directly to disk

The bundled backgrounds use `.webp`, and uploaded images are re-encoded to JPEG before being stored locally.

## License

MIT. See [`LICENSE`](LICENSE).
