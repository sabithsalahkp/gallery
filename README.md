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
