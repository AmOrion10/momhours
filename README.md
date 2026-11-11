# MomHours – Cayman Islands Work Log

Offline-first web app for tracking work hours, breaks, and bi-weekly payroll.

## Features
- Log shifts by date + start/end time
- Smart break suggestion (≥ 9 hours → 1 hour unpaid) – fully overridable (including 0)
- Running unpaid total (hours + CI$ amount)
- Mark periods as paid (moves to permanent history)
- Monthly summary + simple calendar of worked days
- One-tap share of current unpaid or any payslip (WhatsApp-friendly)
- Full JSON backup / restore
- Works completely offline after first load
- Installable as PWA (Add to Home Screen)

## How to use with your mom
1. Host the files (see below) or open `index.html` directly.
2. Send her the link in WhatsApp and ask her to pin the chat.
3. On first open she sets her hourly rate (CI$).
4. She taps **+ Add** on Home to log each day.
5. When paid, she uses **Mark Paid** and selects the shifts.

## Hosting options (free & easy)
- **Netlify Drop**: drag the `momhours` folder to https://app.netlify.com/drop
- **GitHub Pages**: push to a repo and enable Pages
- **Cloudflare Pages**, Vercel, etc.

Once hosted, the link works on her phone and she can “Add to Home Screen” for an app-like experience.

## Files
- `index.html` – the entire app (HTML + CSS + JS)
- `manifest.json` – PWA metadata
- `sw.js` – basic service worker for offline caching

## Data
Everything is stored in the browser’s `localStorage` under the key `momhours_v1`.  
Export regularly via Settings → Download Full Backup.
