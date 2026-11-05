# VAHINI WEDDINGS — Deployment instructions

This ZIP has index.html at its root, suitable for static hosting.

## Netlify Drop
Upload this ZIP at https://app.netlify.com/drop (or drag the extracted folder).

## Cloudflare Pages
Use Workers & Pages > Create > Pages > Upload assets, then upload the extracted folder contents.

## GitHub Pages
Upload the files in the ZIP root to the publishing branch root.

## Important demo limitation
admin.html is a local-browser demo, NOT a secured production admin. Its uploads are stored in browser IndexedDB and are NOT deployed, synced to other visitors, or persisted on the hosting server. Do not upload sensitive files. For production uploads, a server backend, authentication and object storage are required.

Sample images and videos use third-party external URLs and may fail if blocked or removed.
