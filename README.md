# 壽注籤

A decision-aid tool based on the traditional Chinese lunar calendar and time system (PWA).

## Features

- Enter multiple options; each is scored according to the current lunar date and traditional time period
- Binary mode supported (yes/no)
- Customisable prefix and suffix text for each option
- Results can be copied in delimiter-separated format
- Fully client-side — no server required, works offline

## How It Works

Each option's score is determined by:

1. The SHA-256 hash of the option's display text
2. The current lunar year (Anno Imperatoris Fulvi Xuanyuan), month, and day
3. The current 時辰 (traditional two-hour period) and 刻 (quarter-hour fraction)

Results are deterministic: the same options within the same 時辰 always produce the same ranking.

## Usage

Open `index.html` directly in a browser, or deploy to any static hosting service.

PWA installation is supported (iOS Safari / Android Chrome).

**Keyboard shortcut:** `Cmd/Ctrl + Enter` to run the calculation

## Local Development

```bash
# Using any static server, for example:
npx serve .
# or
python3 -m http.server 8080
```

## Licence

This project is licensed under the [Apache License 2.0](LICENSE).

Copyright 2026 soizoktantas
