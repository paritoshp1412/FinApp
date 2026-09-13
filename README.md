# Ledger — one file, hosted for free on GitHub Pages

This folder is the entire deployable app: `FinanceApp.html` (dashboard + Quick Add,
in one file) plus the four small files that make it installable to a phone home screen
(`manifest.json`, `sw.js`, two icons).

## What NOT to put in this repo
Your actual data — `Personal_Finance.xlsx`, anything with real numbers — never goes here.
This folder is only the empty app shell (code). Your data lives in your browser's local
storage on your own device, and the workbook itself stays wherever you keep it
(phone Files app, Drive, iCloud) — you only ever pick it locally via the file picker
when you tap Merge.

## Hosting steps
1. Create a public GitHub repo (private works too on GitHub Free).
2. Upload all 5 files in this folder to the repo root.
3. Settings → Pages → Source: `main` branch, root. Save.
4. GitHub gives you `https://yourusername.github.io/reponame/FinanceApp.html`.
   Open that on your phone.
5. Add to Home Screen (Safari: Share → Add to Home Screen. Chrome: menu → Install app).
   It now opens full-screen, offline-capable, like a native app.

## Keeping it up to date
Whenever you (or Claude) change `FinanceApp.html` — a new feature, a bug fix, a new
Txn Kind — just re-upload the changed file(s) to the same repo. GitHub Pages picks up
the change automatically within a minute or two; refreshing the installed app on your
phone gets the new version.

## Nothing else needs to change on the workbook side
The Personal_Finance.xlsx buffer-row setup (the pre-formatted blank rows Merge writes
into) is independent of how this app is hosted — same workbook works whether you open
this app from GitHub Pages, from a local file, or however else.
