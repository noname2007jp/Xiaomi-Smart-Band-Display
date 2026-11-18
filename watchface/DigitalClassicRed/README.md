# Digital Classic Red — Xiaomi Smart Band 10 project

Target: Xiaomi Smart Band 10 (212x520, codename o66)

## Design
- Static metallic analog clock artwork at the top (decorative, not time-synchronized)
- Live digital hour and minute widgets with a visible colon (`HH:MM`)
- Live date as `YYYY/MM/DD (weekday)` using Japanese weekday image sprites
- Compact weather icon + temperature in Celsius
- Battery percentage only; no battery bar
- AOD disabled

## Build into an installable .face/.bin
This folder is a source project, not yet a compiled watch-face binary.
1. Install Node.js 22+.
2. Download/clone https://github.com/utsabfdahal/band10-toolkit
3. Copy this entire `DigitalClassicRed` folder into the toolkit's `examples/` directory.
4. From the toolkit root run:
   `npm install`
   `npm run band10 -- validate examples/DigitalClassicRed`
   `npm run band10 -- build examples/DigitalClassicRed`
   `npm run band10 -- package examples/DigitalClassicRed --target native`
5. The generated `.face`/`.bin` should be in `examples/DigitalClassicRed/dist/`.
6. Import the generated `.face` in Notify for Mi Band on Android and sync to the Band 10.

## Important
- The analog hands are part of the background artwork and do not move.
- Weather values are supplied by the phone/companion synchronization; this project does not fetch weather from the internet.
- The toolkit is reverse-engineered and not an official Xiaomi format. Validate the generated package and test on your own band before relying on it.
