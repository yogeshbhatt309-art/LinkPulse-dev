# Team HLD — LinkPulse

**Repository:** `team-hld-linkpulse`  
**Live URL:** https://lnkpulse-dev.vercel.app/  

## Problem statement
A link-management platform must do more than map short codes to destinations. It should integrate link creation, redirect rules, click tracking, organization, analytics, QR codes, CSV import, and safety controls.

## Solution
LinkPulse is a Node.js/Express application with a responsive browser interface, SQLite data store, authenticated link management, rule-aware redirects, and click-event reporting.

## Implemented features
- Register/login, owner-scoped links and admin endpoints
- Random/custom short aliases, expiry, click caps and password-protected redirects
- Redirect events with time, referrer, device, browser, hashed visitor and basic bot flag
- Campaign and tag fields; folders; QR image endpoint; bio pages; device destination overrides
- Domain blocklist and link disabling; link creation rate limiting
- Dashboard frontend and analytics endpoints

**Scope / limitations:** Geolocation, team workspaces, background click queue, comprehensive anti-abuse scanning and production-grade bot detection are not implemented. Do not claim these in the demo. This code uses SQLite: do **not** deploy it on ephemeral filesystem hosting and expect durable data. Free static hosting (GitHub Pages) cannot run the backend. A public deployment needs persistent storage, or a database migration.

## Tech stack
Node.js 20+, Express 4, SQLite (`better-sqlite3`), vanilla HTML/CSS/JavaScript, JWT in HTTP-only cookie, bcryptjs, QRCode, Helmet, express-rate-limit.

## Local setup
```bash
# In extracted project folder
npm install
cp .env.example .env  # Windows: copy .env.example .env
# Configure JWT_SECRET in your shell or via your deployment environment.
# This app does not automatically load .env files.
npm start
```
Visit `http://localhost:3000`. PowerShell example: `$env:JWT_SECRET="your-unique-long-random-secret-at-least-32-characters"; npm start`. Do not commit your real secrets.

## Deployment
1. Create public GitHub repo `team-hld-linkpulse`, upload project contents, not the enclosing ZIP.
2. Choose Node-compatible hosting with persistent storage. `render.yaml` illustrates a persistent-disk setup **which may require a paid plan**; it is not a guaranteed free deployment. For a strict zero-cost deployment, first migrate SQLite to an available durable free-tier database and retest.
3. Set `NODE_ENV=production`, `JWT_SECRET` (32+ characters), and `DB_PATH` pointing to persistent storage. Install/build using `npm install`, start with `npm start`.
4. Verify `/health`, signup/login, new alias, redirect and analytics from a second device. Replace the live URL placeholder above.
5. Never submit localhost. Check hosting quotas and availability before promising zero cost.

## Screenshots
Add genuine screenshots after running the application; do not use mock screenshots as evidence of a working deployment.

| Screen | Screenshot |
| --- | --- |
| Dashboard | _Add `screenshots/dashboard.png`_ |
| Create link | _Add `screenshots/create-link.png`_ |
| Analytics | _Add `screenshots/analytics.png`_ |

## Git collaboration
Each member should clone and commit from their **own** GitHub account. Suggested messages: `feat: add redirect rules`, `docs: add setup and deployment notes`, `test: verify link lifecycle`. Do not fabricate team-member commits.

## Demo checklist
Create a link → open it → check recorded click → generate QR → disable link → confirm it stops redirecting. Show a CSV import only if verified in your running build.
