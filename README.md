# Xiaomi Smart Band 10 — Digital Classic Red

This repository is for the custom Xiaomi Smart Band 10 watch face.

## Design specification
- Canvas: 212 × 520 px
- Black / metallic background with red accents
- Decorative numbered analog dial at the top (static artwork)
- Large digital time in HH:MM format with a visible colon
- Date: YYYY/MM/DD with Japanese weekday
- Small weather icon and temperature
- Small battery percentage only (no bar)
- AOD disabled

## Build
The GitHub Actions workflow builds the watch-face project with the upstream Band 10 Toolkit and publishes the generated files as a downloadable artifact.

The editable source project must be placed at `watchface/DigitalClassicRed/` before running the workflow.
