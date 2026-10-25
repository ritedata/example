PARTITURA - installable app (PWA)

1. Upload this whole folder to any HTTPS static host
   (Netlify Drop, GitHub Pages, Cloudflare Pages, Firebase Hosting...).
   A PWA only installs from https:// (or localhost), not from a file.
2. Open the address on your phone.
   Android / Chrome: menu (three dots) > Install app (or Add to Home screen).
   iPhone / Safari: Share button > Add to Home Screen.
3. Open it from the home-screen icon. After the first visit it also works offline.

Files: index.html, manifest.webmanifest, sw.js, icon-192.png, icon-512.png,
icon-maskable-512.png, apple-touch-icon.png. Keep them together in one folder.
When you change a file, raise the version number in sw.js (partitura-v22 -> v23).

BACKUP / SYNC BETWEEN DEVICES (environment backup, format v2)
Library screen > Export library saves one ZIP (library.json + the PDFs).
On the other device: Import library > choose Merge (adds new PDFs, newest edit wins,
no duplicates) or Overwrite (replaces that device's library).
The backup contains: every PDF, titles/authors/pins/last page, crop settings, tempo grids
(BPM, beats, measure counts, systems, per-box on/off, page-loop setting), YouTube links, all annotations and erasures, and the audio / brightness /
eraser settings. Overwrite restores everything including settings; Merge keeps the device's own settings.
Notes: deletions are not synced by Merge (use Overwrite); a PDF is matched by id or by its content,
so the same PDF is never duplicated.

PAGE EDITS (duplicate / delete page)
These rewrite the stored PDF itself, so the changed file travels with Export / Import. When the same
document exists on both devices, Merge keeps the version that was changed most recently (its PDF file,
crop, tempo grids and annotations together). Export a library backup before deleting pages you may need.

ZOOM & PAN (edit and calibrate modes)
Pinch with two fingers or Ctrl + mouse wheel to zoom; drag with two fingers, the Pan tool, Space + drag or
the middle mouse button to move around. + / - / 0 keys zoom in / out / fit. Zoom resets when you leave edit mode.
