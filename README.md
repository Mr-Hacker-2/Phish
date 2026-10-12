# Browser Environment Audit Demo

This repository contains a single-page browser dashboard that displays locally available environment details such as screen size, browser capabilities, language, and privacy signals.

## Run locally

Open `index.html` in a modern browser. The page uses external libraries and fonts, so those assets may contact their providers when loaded.

## Privacy improvements

The dashboard no longer calls an advertising endpoint to infer ad status or a third-party IP lookup service to fetch the visitor's IP address and ISP. Those fields now show **NOT CHECKED / NOT QUERIED** rather than making external lookups.

Some browser values can still be identifying when combined. Treat collected output as potentially sensitive and do not publish it without the user's consent.

## Recommended next steps

- Self-host dependencies if you want to reduce third-party requests.
- Add a clear notice before displaying any browser fingerprint values.
- Avoid claiming that a device is “encrypted” or “anonymous” based only on browser signals.
- Test in a browser with network developer tools to verify which external assets are requested.

This project is a diagnostic demo, not a security certification tool.
