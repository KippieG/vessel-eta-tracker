# Vessel ETA Tracker — CSP Zeebrugge

Real-time vessel tracking dashboard for the port of Zeebrugge. Connects to live AIS data via [aisstream.io](https://aisstream.io) and compares actual vessel positions against the planned N4 vessel schedule — alerting planners when ships deviate significantly from their ETA.

## The problem it solves

Disrupted sailing schedules are one of the biggest operational challenges for container terminals. When a vessel arrives 6 hours late, the yard plan is wrong, crane crews are misallocated, and truck appointments don't match. This tool gives the operations team early warning — so they can adapt before the ship arrives.

## How it works

```
Live AIS feed (aisstream.io WebSocket)
        ↓
Filter vessels near Zeebrugge (bounding box: North Sea approach)
        ↓
Compare position + speed → calculate real ETA
        ↓
Compare against planned N4 schedule
        ↓
Alert if deviation > threshold (configurable)
```

## Setup

1. Get a free API key at [aisstream.io](https://aisstream.io) (sign up with GitHub)
2. Open `index.html` in your browser
3. Enter your API key → click Connect
4. Live vessels appear on the map and in the schedule table

## Tech stack

- Pure HTML / CSS / JavaScript — no framework, no server
- [aisstream.io](https://aisstream.io) — free WebSocket AIS API
- [Leaflet.js](https://leafletjs.com) — interactive map
- [Chart.js](https://chartjs.org) — ETA deviation chart

## Why this matters for CSP Zeebrugge

CSP Zeebrugge serves the UK, Ireland, Scandinavia and Baltic routes — vessels coming through the English Channel and North Sea. In 2025, disrupted alliance schedules caused significant yard planning challenges across Northwest European terminals. Early ETA visibility directly reduces rehandles, overtime, and crane idle time.
