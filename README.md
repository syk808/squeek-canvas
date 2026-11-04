# Squeek Canvas

Squeektoshi paints. A daily generative painting drawn only from the hamster's real runs on Squeekchain.

- **The canvas is a 24-hour clock (UTC)**, midnight at the top.
- **Every half hour he runs is a brushstroke** from the centre outward: more wheel work, longer and heavier stroke. Quiet half hours leave bare canvas.
- **Every Squeekchain settlement is a paint drop**, placed and coloured by its transaction hash, so each drop is unique and can be checked on Sepolia.
- **Every day has its own palette**, seeded by the date, so the same day always paints the same picture.
- **Gallery** of every day since the wheel was wired up, **Replay the day** stroke by stroke, and **Save PNG**.
- Live status: shows whether Squeektoshi is on the wheel right now (RPM, speed).

## Data

Read-only, from the public Squeekchain API (CORS open):

- `GET /v1/measurement/stats?range=30d`: per-day work in 30-minute buckets
- `GET /v1/settlements?range=24h`: recent settlements (tx hash, work added, timestamp)
- `GET /v1/status`: live wheel telemetry

No wallet, no signatures, no backend. One static `index.html`.

## Run locally

Open `index.html` through any static server, e.g. `python -m http.server`.

Fan-made for the Squeekchain Genesis code lane. Not affiliated with Squeekchain.
