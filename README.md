# Epicenter PH — Earthquake Plotter

A Philippines-focused earthquake monitor and bulletin image creator.

## Features

- USGS earthquake updates every 60 seconds while the page is open
- Geographic epicenter map with zoom controls
- Magnitude, depth, coordinates, and Philippine time
- Manual entry of verified bulletin information and source attribution
- Square (1200 × 1200) and landscape (1600 × 1000) PNG export

## Run locally

No build step or package installation is required. Serve the `dist` directory with a static web server:

```sh
python3 -m http.server 8000 --directory dist
```

Open http://localhost:8000 in your browser. Internet access is required for live USGS data and optional web fonts. The geographic basemap is included locally.

## Source layout

- `dist/index.html` — app interface
- `dist/style.css` — responsive styling
- `dist/app.js` — earthquake feed, canvas plotting, manual editor, and PNG export
- `dist/countries.json` — simplified geographic basemap derived from datasets/geo-countries
- `.openai/hosting.json` — configuration for the existing ChatGPT Site

## Data and scope

Live data comes from USGS, not an automatic PHIVOLCS feed. PHIVOLCS bulletin details can be entered manually. Samples and manual entries are labeled. Automatic refresh runs while the page is open; this app does not run a background monitoring service.

This is an independent visualization, not an official earthquake or tsunami advisory. Refer to PHIVOLCS for official Philippine advisories.

## Validation

JavaScript syntax and mocked initialization/feed parsing/canvas drawing checks passed. Browser layout and downloads have not yet been verified.
