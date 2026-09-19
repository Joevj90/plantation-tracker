# Rubber Plantation Tracker (public, Vercel + Firebase)

A phone-friendly plantation data tracker. Deployed on Vercel, data stored in
a free Firebase (Firestore) database, gated by a simple shared password.

See the setup walkthrough in the chat message this was delivered with for
full step-by-step instructions (Firebase project creation, GitHub repo,
Vercel deployment). This file is a quick reference once you've done that
once.

## Files
- `index.html` -- the whole app (UI + logic)
- `firebase-config.js` -- YOUR Firebase project keys + the shared password (edit this)
- `firestore.rules` -- paste into Firebase console > Firestore > Rules

## Local files you edit
Only `firebase-config.js` needs your own values. Never edit `index.html`
unless you want to change how the app behaves.

## Updating the site later
1. Make changes to the files in this folder.
2. `git add .`
3. `git commit -m "describe your change"`
4. `git push`
5. Vercel redeploys automatically within ~1 minute.

## Security note
The password screen is a basic deterrent, not real security -- it runs
entirely in the browser, so it can't stop someone determined from reading
the page's source or calling the database directly. Don't store anything
truly sensitive here. If you outgrow this, the upgrade path is Firebase
Authentication with per-user sign-in and Firestore rules tied to it.
