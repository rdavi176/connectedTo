# Connected to New York

A streets-only map of New York City with every free public Wi-Fi spot drawn as a coverage bubble.

- Search a street or a corner ("Bedford Ave & N 7th St") to zoom to a couple of blocks around it
- Hover a street to see its name; hover a Wi-Fi bubble to see the network and star it
- Starred spots live in the Saved list (stored in your browser)
- The camera button saves a PNG of the current view

## Files
- `index.html` — the whole page (HTML, CSS and JavaScript)
- `streets.json` — NYC street centerlines, simplified (~5 MB)
- `wifi.json` — free Wi-Fi locations (LinkNYC kiosks, subway stations, libraries, street & park networks)

## Run it
The page loads the two JSON files with `fetch`, so it needs to be served over http, not opened as a file.

- **GitHub Pages:** push these files to a repo, then Settings → Pages → deploy from the `main` branch, root folder.
- **Locally:** `python3 -m http.server` in this folder, then open http://localhost:8000

## Data
- Street centerlines: NYC Open Data, *NYC Street Centerline (CSCL)*
- Wi-Fi: NYC Open Data, *NYC Wi-Fi Hotspot Locations* (last updated 2022) and *LinkNYC Kiosk Locations* (live kiosks only). Limited-free spots (Spectrum / Optimum "GuestWiFi") are excluded.

Coverage bubble sizes are rough estimates, not measured signal strength.

## Font
The page asks for Neue Haas Grotesk Text Pro and falls back to Helvetica Neue / Arial if it isn't installed. To show it to everyone, add licensed web font files and an `@font-face` rule.
