# VAHINI WEDDINGS — gallery website and demo admin

## Open
Open `index.html` for the public gallery and `admin.html` for the demo media dashboard. For reliable browser storage, run on a local HTTP server (for example `python -m http.server 8000`) and visit `http://localhost:8000`.

## Features
- Responsive minimal gallery, photography and film filters, fullscreen photo/video viewer with keyboard arrows and mobile swipe.
- Cinematic hero that can play a chosen uploaded video (muted, looping, inline) or display a chosen image.
- Auto light/dark theme based on device setting.
- Admin demo with multi-file photo/video upload, delete, title editing for uploaded items, and hero selection.
- Uploaded media is stored **only in the current browser's IndexedDB**. Changes are visible to the public gallery **in that same browser/profile only**.
- Sample gallery photos are loaded from Unsplash via external URLs; these require an internet connection and can be replaced with your own photos. There are no sample videos; upload a video in admin and choose Set hero.

## Important limitations
This is a **demo**, not a hosted media service. It has no server-side authentication, shared admin changes, cloud storage, or video transcoding. IndexedDB capacity depends on browser/device, so 20 TB is **not supported** in this demo. Never use this dashboard as your only copy of important media.

For production: add an authenticated backend, a database, Cloudflare R2 or comparable object storage with multipart direct uploads, an asset CDN, and an adaptive HLS video encoding/streaming pipeline. Preserve original files in object storage, serve appropriately sized thumbnails, and offer adaptive 720p/1080p/4K renditions. Hosting and media egress/transcoding have real costs. Admin access must be secured server-side.

## Files
`index.html` public gallery; `admin.html` demo dashboard; `styles.css` styling; `shared.js` browser storage and samples; `main.js` gallery interactions; `admin.js` dashboard interactions; `assets/` reference logo and video placeholder.


## Updated sample visuals

The default hero now uses a real wedding photograph from Unsplash. Three sample wedding film entries are linked to Mixkit preview video streams (internet required). They are not embedded inside the ZIP. Their individual source pages are listed in shared.js; check each clip's license before publishing commercially. If a provider blocks remote playback, use the Admin page to upload your own MP4 clips instead. The website does not promise that external CDN links remain available.


Update: header has left SVG theme toggle, single-line brand and Film toggle; all media appear together by default. Film toggles videos-only view. Gallery cards retain natural image proportions; lightbox uses contain fitting. Admin remains available directly at admin.html (not linked from public header).


## Masonry gallery update
The public gallery now uses independent CSS columns so short images and video thumbnails fill gaps under each other, rather than sharing the height of the tallest item in a grid row. Original proportions are preserved. Desktop: three columns; tablets: two; narrow screens: one.

## Video files and offline use
The three included sample video URLs point to external Mixkit preview MP4s. They are **not downloaded or bundled**: this build environment cannot fetch the remote video bytes. They need an internet connection and may stop working if the provider changes its URLs. To package genuine local footage, use the separate `admin.html` page to upload MP4 videos on the viewing browser (demo-only local storage), or supply your licensed MP4 files for embedding in the ZIP. Do not present this demo as an offline video package or as production-scale storage.
