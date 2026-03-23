# Useful Timer

`Useful Timer` is a single-page focus timer built with plain HTML, CSS, and JavaScript. Open it in a browser and you get a large Pomodoro timer, a live analog clock, interval chimes, draggable panels, fullscreen mode, rotating backgrounds, and lightweight sticky notes that all persist locally in the browser.

There is no build step, no framework, and no account setup. It is just a static page you can keep open on a laptop or second monitor during a work session.

## Features

- `25 min` and `50 min` timer modes with start, pause, and reset controls
- End-of-session alarm generated with the Web Audio API
- Warning state during the last 10% of a session and pulsing when time reaches zero
- Analog clock with a live wedge showing how much of the next hour your remaining session occupies
- Three interval gauges running on a repeating 90-second cycle with optional bell chimes
- Draggable timer, clock, and interval panels with snap-to-position behavior
- Click-to-create sticky notes that can be moved, resized, edited, and dismissed
- Random fullscreen background images with left/right arrow navigation
- Fullscreen toggle for distraction-free use
- Persistent timer state, panel positions, bell preference, and sticky notes via `localStorage`

## Getting Started

1. Clone or download this repository.
2. Open `index.html` in any modern browser.

That is the entire setup.

## How To Use

1. Pick `25 min` or `50 min`.
2. Press `Start` to begin the session.
3. Drag the timer, clock, or interval panel to the part of the screen you prefer.
4. Click anywhere on the background to create a sticky note.
5. Use the bell button on the interval panel to mute or enable interval chimes.
6. Press the fullscreen button in the top-right corner when you want a cleaner display.

## Keyboard Shortcuts

| Key | Action |
| --- | --- |
| `Left Arrow` | Previous background image |
| `Right Arrow` | Next background image |

## Project Structure

- `index.html` contains the full app markup and JavaScript behavior
- `site.css` contains the visual styling and layout rules
- `images/` contains the bundled background artwork

## Customization

- Update the `IMAGES` array in `index.html` to use your own backgrounds
- Adjust `INTERVAL_DURATION` and `INTERVAL_COUNT` in `index.html` to change the interval cycle
- Edit `site.css` to change typography, spacing, overlays, note styling, and overall look

## Browser Requirements

Use a modern browser with support for:

- `localStorage`
- `<canvas>`
- the Fullscreen API
- the Web Audio API

The included background images are `.webp` files, so if you replace them for older browsers you may prefer different formats.

## License

MIT. See [`LICENSE`](LICENSE).
