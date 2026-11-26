# iGate login test

This project contains the iGate login and profile test.

## Setup

Install Node.js and ensure you can access the iGate development environment (including VPN if required). In PowerShell, run:

```powershell
npm.cmd ci
npx.cmd playwright install chromium
Copy-Item .env.example .env
```

Edit `.env` and set `TEST_USERNAME`, `TEST_PASSWORD`, `API_PASSWORD` (the encrypted API password for the same username), and `API_CLIENT_SECRET`. Obtain these through your organization's approved channel. Adjust the URLs and organization domain if necessary. Never commit `.env`.

## Run

```powershell
npx.cmd playwright test tests/igate-login.spec.ts --project=chromium
```

The test pauses at the end. Press Resume in the Playwright Inspector to finish.

