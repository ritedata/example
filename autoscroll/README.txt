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
When you change a file, raise the version number in sw.js (partitura-v14 -> v15).

BACKUP / SYNC BETWEEN DEVICES
Library screen > Export library saves one ZIP (library.json + the PDFs).
On the other device: Import library > choose Merge (adds new PDFs, newest edit wins,
no duplicates) or Overwrite (replaces that device's library).
