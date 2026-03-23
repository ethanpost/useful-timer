# Useful Timer

A calm, full-screen Pomodoro timer you can open in a browser and actually *live with* for a work session. No accounts, no build step, no framework churn—just HTML, CSS, and a little JavaScript that tries to get the small details right.

## Why it exists

Focus tools often feel either bare or busy. This one sits in the middle: a big readable countdown, a real analog clock, optional gentle structure from repeating short intervals, and backgrounds that are pleasant to stare at when you glance up. State persists if you refresh or close the tab by accident, and the pieces you care about can be dragged where your screen layout needs them.

## Try it

1. Clone or download this repository.
2. Open `index.html` in a modern desktop or mobile browser (double-click, or serve the folder with any static file server if you prefer).

That is the whole install story.

## What you get

- **Sessions** — Choose **25** or **50** minutes, start, pause, and reset. The display soft-warns in the last 10% of the run and pulses when time is up.
- **Alarm** — A simple synthesized buzzer when the session ends (toggle with the bell next to the timer). Preference is remembered.
- **Analog clock** — Canvas-drawn, shows the real time. While a session is running, a wedge shows roughly how much of the next hour your remaining time occupies—handy for orienting without doing mental math.
- **Three interval gauges** — A repeating **90-second** wall-clock cycle split into three **30-second** segments. When the interval bell is on, you get a short chime at each boundary—useful for micro-check-ins, hydration, or posture without leaving flow. The bell is independent of the main timer alarm and can be muted separately.
- **Backgrounds** — A small curated set of full-bleed images (stored under `images/`). Press **←** and **→** to change the scene; the app picks one at random on load.
- **Layout** — The clock, timer block, and interval panel are **draggable** (grab away from buttons). They snap to sensible anchor points and **positions are saved** in the browser. On window resize, layouts re-snap so nothing drifts off-screen.
- **Fullscreen** — One click to fill the display when you want fewer distractions.
- **Resilience** — Timer progress and running/paused state are stored in `localStorage`, with elapsed time corrected if you return after a break.

## Keyboard

| Key | Action        |
| --- | ------------- |
| ←   | Previous image |
| →   | Next image    |

## Customizing

Everything lives in `index.html` and `site.css`.

- **Images** — Edit the `IMAGES` array near the top of the script to point at your own files (keep `images/` or update paths).
- **Interval length** — Constants `INTERVAL_DURATION` (seconds per segment) and `INTERVAL_COUNT` control the gauge cycle and chime rhythm.
- **Look and feel** — Typography, shadows, and overlay styling are in `site.css`.

## Requirements

Any recent browser with **Canvas**, **localStorage**, **Fullscreen API**, and **Web Audio** (for alarms) is enough. The bundled art is **WebP**; very old browsers may need different image formats if you swap assets.

## License

MIT — see [LICENSE](LICENSE).

---

Made to be useful on a second monitor, a laptop at a café, or anywhere you want focus without signing up for another service. If it helps your day, that is enough.
