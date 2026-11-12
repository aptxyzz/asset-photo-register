ASSET PHOTO REGISTER - OFFLINE ANDROID PWA

WHAT IT DOES
- Imports a CSV with exactly two columns: Component Group, Component Name
- Lists every component on the phone
- Opens the rear camera for the selected component
- Stores photos offline on the device
- Automatically names photos Group_Name_001.jpg, etc.
- Exports a ZIP containing Photo_Register.csv and photos organised by folders

INSTALL (RECOMMENDED)
A PWA must be opened through HTTPS or localhost; Android does not install it correctly by opening index.html directly.
1. Put the three app files (index.html, manifest.webmanifest, sw.js) on any HTTPS static host. Examples: GitHub Pages, Netlify Drop, Cloudflare Pages, or an approved company web server.
2. Open the HTTPS link in Chrome on Android.
3. Chrome menu > Add to Home screen / Install app.
4. Open the installed app once while online. It will then work offline.

QUICK LOCAL TEST
- On a computer, serve the folder with: python -m http.server 8000
- Open http://COMPUTER-IP:8000 on the Android phone while both devices are on the same network. Camera access may require HTTPS on some Android/Chrome versions, so use an HTTPS host for field deployment.

USAGE
1. Tap Download template.
2. Edit the CSV in Excel. Keep headers exactly: Component Group, Component Name. Save as CSV UTF-8.
3. Tap Import CSV.
4. Tap the camera icon beside an asset.
5. Take one or more photos.
6. Tap Export register + ZIP.

IMPORTANT
- Data is stored only in the browser/app storage on that Android device until exported.
- Do not clear Chrome site data or uninstall the app before exporting.
- Large/full-resolution photo sets may consume significant phone storage and create large ZIP files. Export by inspection batch.
- Importing the same CSV updates/reuses matching asset IDs; it does not delete existing photos.
- CSV is used instead of XLSX so the app remains fully offline and has no third-party library dependency.
