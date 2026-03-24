# Useful Timer

`Useful Timer` is a static, single-page focus dashboard built with plain HTML, CSS, and JavaScript. Open `index.html` in a modern browser and you get a fullscreen-friendly timer, a live analog clock, configurable interval gauges, rotating backgrounds, and lightweight sticky notes that all persist locally in the browser.

There is no build step, no framework, and no server requirement for normal use.

## Features

- Two timer presets with configurable durations from `1` to `120` minutes
- `Start`, `Pause`, and `Reset` controls with progress restored after reload
- Visual warning state during the last `10%` of a session and a completion alarm via the Web Audio API
- Analog clock rendered on `<canvas>`, including a progress wedge while the timer is running
- Three configurable interval gauges based on a repeating wall-clock cycle
- Bell toggle for interval alerts, saved between sessions
- Draggable timer, clock, and interval panels with saved positions
- Built-in background image gallery plus local image uploads from the settings panel
- Sticky notes that can be created, edited, dragged, resized, closed, and merged by dropping one note onto another
- Selectable sticky-note font from several monospace stacks
- Fullscreen toggle and background navigation with the left and right arrow keys

## Getting Started

1. Clone or download this repository.
2. Open `index.html` in a modern desktop browser.

That is the full setup.

## How To Use

1. Choose one of the two timer buttons and press `Start`.
2. Drag the timer, analog clock, or interval panel wherever you want on screen.
3. Open `Settings` to change timer lengths, interval lengths, sticky-note font, or manage uploaded background photos.
4. Click empty background space to create a sticky note.
5. Use the bell button on the interval panel to enable or disable interval alerts.
6. Use the fullscreen button in the top-right corner for a cleaner display.

## Keyboard Shortcuts

| Key | Action |
| --- | --- |
| `Left Arrow` | Previous background image |
| `Right Arrow` | Next background image |

## Persistence

The app stores its state in `localStorage`, including:

- timer state
- draggable panel positions
- bell preference
- sticky notes
- settings values
- uploaded background images

All data stays in the current browser profile on the current machine.

## Notes And Limitations

- Uploaded photos are stored in browser storage, so large or numerous images can hit `localStorage` quota limits.
- The app is optimized for mouse-driven desktop use; drag interactions are not implemented with touch-specific handlers.
- Uploaded images and notes are local only. There is no sync, export, or account system.
- The interval bell toggle currently also blanks the gauge progress display instead of muting sound only.

## Project Structure

- `index.html` contains the app markup and all JavaScript behavior
- `site.css` contains layout, styling, and note/settings visuals
- `images/` contains the bundled background artwork

## Customization

- Use the in-app `Settings` panel for most day-to-day customization
- Replace or add files in `images/` if you want different bundled backgrounds
- Edit `site.css` to change typography, layout, glassmorphism, and sticky-note styling
- Edit the inline script in `index.html` if you want to change app behavior

## Browser Requirements

Use a modern browser with support for:

- `localStorage`
- `<canvas>`
- the Fullscreen API
- the Web Audio API
- `FileReader`

The bundled backgrounds use `.webp`, and uploaded images are re-encoded to JPEG before being saved locally.

## License

MIT. See [`LICENSE`](LICENSE).
