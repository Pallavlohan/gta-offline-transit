# Changelog

## v1.0.0 — Initial Public All-in-One Release (2026-11-25)

First public standalone release of **GTA Offline Transit** (`com.gta.offlinetransit`, `arm64-v8a`, Android 8.0+).

### Highlights
- **All-in-One Offline Bundle (`143.72 MiB`):** Includes GTA vector basemap (`gta_basemap.pmtiles`), `989,215` OSM addresses + `50,933` stores/landmarks (`gta_addresses.db`), `3,319 / 3,329` road-snapped GTFS transit shapes (`gta_shapes.db`), tiled pedestrian walk network (`gta_walk_graph.db`), and `11` GTHA transit feeds (`gta_transit.db`: `28,657` stops, `746` routes, `3,329` patterns, `322,507` trips, `189,110` transfers).
- **11 GTHA Agencies:** GO Transit, UP Express, TTC (including Line 5 Eglinton & Line 6 Finch West LRT backbone + aliases), MiWay, Brampton Transit (Züm, with exact `50`/`50A`, `511`/`511C`, `1`/`1A`, `4`/`4C`, `11`/`11A` branches), YRT (Viva), DRT, Oakville, Burlington, Milton, and HSR.
- **Trip Planner & Timetables:** Door-to-door RAPTOR routing (`Best`, `Fastest`, `Less walking`, `Fewer transfers`), `Leave | Arrive | Last` wheel picker, `"Also at ..."` alternatives, 5-tab Nearby board (`Suggested | Train | Tram | Bus | Subway`), 2-step Stop Departures -> Route Trip Schedule with horizontal departure tabs & `"Show previous stops"`.
- **Navigation & Convenience:** Road-following blue dotted walks, Heading-Up compass cone & North needle FAB, foreground live GPS stop-rail tracking with 1-stop exit vibration, Saved Places (`Home`, `Work`, `Favorites`, `Want to go`, starred stops), and 0%-battery `"Last ride home"` evening reminder.
- **Zero-Internet Privacy:** Zero `INTERNET` permission, zero `ACCESS_BACKGROUND_LOCATION`, zero analytics, zero background services.
