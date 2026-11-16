# BSP S-InTeL — cybersecurity intelligence prototype

## What is included
- `android/`: mobile-first Progressive Web App (PWA), designed for Android Chrome.
- `desktop/`: responsive laptop/desktop build, with local launch scripts.
- `S-InTeL-Promo.mp4`: short promotional concept video.
- `S-InTeL-Interactive-Promo.html`: interactive promotional walkthrough.

## Important status and limits
This is a **prototype for evaluation**, not a production cybersecurity platform and not an official BSP product. All alerts, counts, assets, severity distributions, trends and control scores are fabricated sample data. It does not connect to, scan, access, or monitor BSP networks, endpoints, banking systems, accounts, customers or staff. No automated remediation is executed.

The interface demonstrates the intended workflow: incident visibility, severity prioritisation, charts, sample asset posture, incident review, management report export, and human-approved remediation request drafting.

## Android phone test (no APK supplied)
The Android build is an installable PWA, not a signed APK. To install it on Android, it must be served from an HTTPS website (or localhost). Easiest test route:
1. Extract this ZIP.
2. Upload the **contents** of the `android` folder to a new GitHub repository.
3. In GitHub: Settings → Pages → deploy from branch → choose `main` and `/ (root)` → Save.
4. Wait for the GitHub Pages HTTPS URL. Open it in Chrome on your Android phone.
5. Chrome menu → **Install app** or **Add to Home screen**.
6. Launch BSP S-InTeL from the phone home screen. It also works in the browser.

Do not upload real BSP data or secrets to a public GitHub repository. For an internal BSP pilot, use an approved private hosting environment and security review.

## Laptop / Windows / Mac test
- Windows: open `desktop/start-windows.bat` (requires Python 3), then visit `http://localhost:8000`.
- macOS/Linux: run `./start-mac-linux.sh`, then visit `http://localhost:8000`.
- Or serve the desktop folder using any static web server.

## Demo features to try
- Overview: threat activity chart, severity donut, posture bars and priority queue.
- Security incidents: filter severity and click **Simulate alert**.
- Remediation centre: create a demo approval request; no system changes occur.
- Reports: download the sample HTML management report or incident CSV.
- Integrations: review required data sources and deployment prerequisites.

## What is needed for a real BSP deployment
A BSP-appointed sponsor and security owner; written authorisation; architecture and threat model; approved SIEM/log, EDR, identity, network and cloud integrations; least-privilege read-only credentials; secrets management; data residency/retention and privacy controls; RBAC/MFA; immutable audit trails; alert tuning; incident playbooks; human approval gates; penetration testing; disaster recovery; and BSP change-management acceptance. Actual remediation requires a separate, tightly scoped and tested execution service.

## BSP identity and logo
The build uses a green BSP-labelled text wordmark and a generic S-InTeL shield icon. It does **not** reproduce BSP's protected official logo. BSP states that it owns its trademarks and that unauthorised use of brand assets is prohibited. Replace the placeholder with an official logo file only after BSP supplies or authorises the asset and its use. The green palette and contextual company information are based on public BSP brand/company pages.

## Public BSP references
- BSP official brand story: https://www.bsp.com.pg/about/our-brand/
- BSP FY2025 results (published 20 February 2026): https://www.bsp.com.pg/about/news-and-media/bsp-financial-group-fy25-results/
- BSP annual reports: https://www.bsp.com.pg/investor-centre/results-and-reports/annual-reports/
- PNGX issuer profile: https://www.pngx.com.pg/bank-south-pacific-limited-2/

## Browser compatibility
Responsive modern HTML/CSS/JavaScript. PWA installation requires HTTPS or localhost and a browser supporting service workers. No native iOS, Android APK, Windows EXE or macOS app binary is included. iPhone/iPad: open the hosted HTTPS version in Safari and use Share → Add to Home Screen.


## Android install troubleshooting (updated build)
This build includes 192x192 and 512x512 PNG icons in the web app manifest. Upload the CONTENTS of the android folder to the repository root (index.html must be at the repository root), keep GitHub Pages set to main / (root), and use the HTTPS URL. After publishing, open the URL in Chrome, refresh once, then use Chrome menu > Install app. If Chrome still does not offer installation, use Chrome menu > Add to Home screen; the website remains usable in the browser. Do not use a GitHub file-preview URL or the repository Code page as the app URL.
