# CampusConnect — Mobile Web App (PWA)

A responsive, mobile-first progressive web app designed to run in Android Chrome and be added to the home screen. It includes faculty search/filtering, campus offices, admin service guides/checklists, a campus building directory, sample timetable, local profile preferences and an offline app shell.

## Important before real campus use
This is a working front-end starter with clearly labelled **illustrative sample data**. Names, email addresses, availability, room numbers, office hours and timetable entries are not verified SRM data. It does **not** yet connect to SRM systems, Firebase authentication/database, push notifications, official maps or live faculty status. Do not present demo data as official information.

## Publish it so Android Chrome can install it
A PWA install requires a secure HTTPS site (or localhost). Easiest free option: GitHub Pages.

1. Extract this ZIP.
2. Create a GitHub repository named `campusconnect` (public is simplest for Pages).
3. Upload **the contents of this folder** to the repository root: `index.html`, `manifest.webmanifest`, `sw.js`, `icons/`, and this README.
4. In the repository open **Settings → Pages**. Under Build and deployment, choose **Deploy from a branch**, branch `main`, folder `/(root)`, then Save.
5. Wait for GitHub Pages to publish and open the HTTPS URL it provides.
6. On Android, open that URL in Chrome → tap **⋮** → **Install app** or **Add to Home screen**.

You can test locally on a computer with a local web server, but opening `index.html` directly as a `file://` URL will not enable the service worker/PWA installation.

## Where to customise sample data
Open `index.html` and edit the JavaScript arrays named `faculty`, `offices`, `guides`, `buildings`, and `timetable`. Use real, approved college directory data only. The sample faculty emails use `example.edu` intentionally and are not contactable addresses.

## Recommended next production steps
- Get approval for official room, faculty, office-hours and timetable data.
- Add Firebase Authentication with SRM-approved sign-in and enforce roles in Firestore Security Rules (never rely on UI role selection for security).
- Store faculty profiles and availability in Firestore; require faculty/admin authentication for updates.
- Add verified campus coordinates/maps and a server-side notification flow.
- Have the college review privacy, data retention, accessibility and security before launch.

## Project files
- `index.html` — complete responsive app interface and demo functionality
- `manifest.webmanifest` — PWA name, theme and install settings
- `sw.js` — offline caching of app shell
- `icons/` — app icons
