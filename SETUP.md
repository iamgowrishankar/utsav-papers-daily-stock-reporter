# Daily Stock Report – Local/PWA version

## What this version does

- Stores current stock on the phone using IndexedDB.
- Add/receive stock increases the saved balance.
- Out stock decreases the saved balance.
- Prevents stock from going below zero.
- Keeps daily add/out/sales history.
- JSON backup contains current stock plus the latest 7 calendar days that have saved records.
- JSON restore can recover the saved stock/history.
- WhatsApp report uses the current stock and that day's out stock/cash/UPI values.
- Includes PWA files (`manifest.webmanifest` and `sw.js`).

## Important setup

Do NOT rely on opening `index.html` with `file://` if you want reliable PWA installation.

The recommended setup is to host these 3 files on HTTPS:

- `index.html`
- `manifest.webmanifest`
- `sw.js`

You can use GitHub Pages, Netlify, Cloudflare Pages, or any simple HTTPS static hosting.

Once opened over HTTPS on the phone:

1. Open the website in Chrome.
2. Use Chrome's menu → "Add to Home screen" / "Install app".
3. Open it from the home screen.
4. The stock data will remain in that browser's IndexedDB until the site/browser data is cleared.

## Backup recommendation

Use **💾 Backup 7 Days** at least once a day or every few days.

The JSON contains the current stock and the latest 7 saved calendar days. Keep the downloaded JSON somewhere safe (Google Drive, WhatsApp to yourself, etc.).

## Important limitation

IndexedDB is local to the browser/device. Clearing browser/site data can remove it. A JSON backup is therefore strongly recommended.

## Units

Reels have two balances: reel count and kilograms.
M-Fold has boxes and pieces.
Other fields use the units shown beside their inputs.

Tape, Clib, Pati Roll and Stretch Film are currently stored as `qty` because their exact unit was not specified. Change their unit in the `groups` configuration if you want kg/nos/rolls.
