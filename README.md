# Color Match Puzzle — Stage 2 Web Project

## Included
- `index.html`: playable match-three game.
- Local best-score and highest-level saving on the same browser/device.
- `manifest.webmanifest`, `icon.svg`: installable web-app metadata and icon.
- `sw.js`: basic offline caching after the first successful load.

## Run locally
For a quick gameplay test, open `index.html` in a modern browser. The game itself works locally. Service-worker/PWA install behavior requires HTTPS or `localhost`.

For local PWA testing with Python installed:
1. Open a terminal in this folder.
2. Run `python -m http.server 8080`
3. Visit `http://localhost:8080`

## Website deployment
Upload the contents of this folder to a static host that serves HTTPS (for example, GitHub Pages, Cloudflare Pages, or Netlify). Confirm the site URL, mobile layout, and offline behavior after deployment.

## Google Play
This folder is a web project, not an Android APK/AAB. A practical next route is to deploy the HTTPS site and wrap it with a Trusted Web Activity (TWA) or a Capacitor Android project. Before publishing, set up app signing, screenshots, store listing, privacy policy, content rating, and testing tracks. Google Play requirements can change; verify current Play Console instructions before submission.

## Important limits
- LocalStorage progress is stored only in the current browser profile and can be cleared by the user. It is not account sync.
- Scores are client-side and can be modified. Do not use them to approve cash payouts or leaderboard prizes.
- No real-money wallet, payout, ads, or purchase SDK is connected yet.
- A real rewards program needs a server-side account ledger, anti-cheat checks, payout provider, age/region eligibility, fraud controls, privacy/security review, and legal/platform-policy review. Never ask users to pay a fee to unlock a promised prize.
