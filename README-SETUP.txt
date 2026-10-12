DAILY STOCK REPORTER — UPDATE FILES

Upload these files to the ROOT of your existing GitHub repository (the same folder where your current index.html is):
- index.html (replace existing file)
- manifest.webmanifest
- sw.js
- icon-192.png
- icon-512.png

On GitHub website: repository → Add file → Upload files → select all 5 files → Commit changes directly to main. If GitHub asks whether to replace existing files, confirm.

Then open the GitHub Pages URL and refresh. If an older version remains, close the app and open the URL in Chrome, refresh again, and wait briefly for the service worker to update.

BEHAVIOR
- IN STOCK adds the entered quantities to saved balances.
- OUT STOCK subtracts entered quantities, and prevents dispatching more than available stock.
- Saved balances persist in IndexedDB on that phone/browser. They are not shared between users.
- Download 7-Day JSON Backup saves current balances plus recent transaction history. Restore replaces current local stock/history after confirmation.
- Quantities are tracked using the unit shown under each item. Reel inventory is tracked in reel counts; reel waste and packing cover weights are in kg.
- Existing free-text values from the old form are not automatically converted. Start with opening balances using IN STOCK entries, or enter the opening quantities after testing.
