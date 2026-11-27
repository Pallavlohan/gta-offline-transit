# Changelog

## v1.1.0 — Google Maps-Style Live Grey Traveled Route (2026-11-27)

Feature and reliability update for **GTA Offline Transit** (`com.gta.offlinetransit`, `arm64-v8a`, Android 8.0+).

### Highlights
- **Live Grey Traveled Route Line:** While tracking an active trip (`Start trip`), covered walk dots and transit segments behind your live GPS position turn muted grey (`#9AA0A6`) underneath the remaining vibrant route lines and `#1A73E8` blue walk dots.
- **Dimmed Passed Stops:** Passed intermediate and transfer stops along completed or traveled segments dim to muted grey while upcoming stops and the destination pin stay crisp and bright.
- **Loop & Out-and-Back Safe Shape Projection:** Monotonic forward-window projection constrained to the active stop interval (`lastPassedStopIndex..nextStopIndex`) prevents out-and-back or looping buses from snapping onto the return half of the route or jumping backward.
- **Battery-Friendly Updates & Instant Restore:** Map overlay GeoJSON refreshes are throttled (`>= 8 m` movement or leg/stop change) and tapping `Stop` restores the full bright route immediately (`86 / 86` JVM unit tests passing across `17` suites; zero `INTERNET` or `ACCESS_BACKGROUND_LOCATION`).
- **APK Checksum (`143.78 MiB`):** `1200a3b401befafb018c14abd9096a732522268ce88e0f7db8b20d152ee489e7` (same release signing certificate `84b72575610dc24b340a4854f53b24befe0d263ef3f7a1d416e048562004886b`).

## v1.0.0 — Initial Public All-in-One Release (2026-11-25)

First public standalone release of **GTA Offline Transit** (`com.gta.offlinetransit`, `arm64-v8a`, Android 8.0+).

### Highlights
- **All-in-One Offline Bundle (`143.78 MiB`):** Includes GTA vector basemap (`gta_basemap.pmtiles`), `989,215` OSM addresses + `50,933` stores/landmarks (`gta_addresses.db`), `3,319 / 3,329` road-snapped GTFS transit shapes (`gta_shapes.db`), tiled pedestrian walk network (`gta_walk_graph.db`), and `11` GTHA transit feeds (`gta_transit.db`: `28,657` stops, `746` routes, `3,329` patterns, `322,507` trips, `189,110` transfers).
- **11 GTHA Agencies:** GO Transit, UP Express, TTC (including Line 5 Eglinton & Line 6 Finch West LRT backbone + aliases), MiWay, Brampton Transit (Züm, with exact `50`/`50A`, `511`/`511C`, `1`/`1A`, `4`/`4C`, `11`/`11A` branches), YRT (Viva), DRT, Oakville, Burlington, Milton, and HSR.
- **Trip Planner & Timetables:** Door-to-door RAPTOR routing (`Best`, `Fastest`, `Less walking`, `Fewer transfers`), `Leave | Arrive | Last` wheel picker, `"Also at ..."` alternatives, 5-tab Nearby board (`Suggested | Train | Tram | Bus | Subway`), 2-step Stop Departures -> Route Trip Schedule with horizontal departure tabs & `"Show previous stops"`.
- **Navigation & Convenience:** Road-following blue dotted walks, Heading-Up compass cone & North needle FAB, foreground live GPS stop-rail tracking with 1-stop exit vibration, Saved Places (`Home`, `Work`, `Favorites`, `Want to go`, starred stops), and 0%-battery `"Last ride home"` evening reminder.
- **Zero-Internet Privacy:** Zero `INTERNET` permission, zero `ACCESS_BACKGROUND_LOCATION`, zero analytics, zero background services.
