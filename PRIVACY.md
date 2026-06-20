# Privacy Policy — ProxySwitcher

**Effective Date:** June 20, 2026
**Last Updated:** June 20, 2026

## Overview

ProxySwitcher is a Chrome extension that manages browser proxy settings. This privacy policy explains what data the extension accesses, how it is used, and how it is protected.

## Data Collection

### What We Collect
- **Proxy server credentials** (host, port, username, password): Entered by the user to configure proxy connections. Stored locally on the user's device using Chrome's built-in storage API. Never transmitted to our servers.
- **Device identifier**: A randomly generated anonymous ID used solely for license key validation and device count enforcement. This ID cannot be traced back to the user.
- **License key**: If the user purchases a subscription, a license key is stored locally to validate the subscription status.

### What We Do NOT Collect
- Browsing history or web activity
- Personal information (name, email, phone number)
- IP addresses (the IP check feature queries third-party APIs directly from the user's browser — our servers are not involved)
- Cookies or tracking data
- Website content or form data
- Location data

## Data Storage

All user data (proxy profiles, settings, credentials) is stored locally on the user's device using Chrome's `chrome.storage` API. Data is not synced across devices unless the user enables Chrome Sync.

## Data Transmission

The extension connects to external services in the following cases:

1. **License server** (`proxy-switcher-production.up.railway.app`): To validate subscription status and license keys. Only the anonymous device ID and license key are transmitted. No browsing data or personal information is sent.

2. **IP check services** (`api.ipify.org`, `ip-api.com`, `proxycheck.io`): When the user manually clicks the "Check IP" button, the extension queries these public APIs to display the user's current IP address and reputation score. These requests are made directly from the user's browser.

3. **Proxy servers**: The extension routes web traffic through proxy servers configured by the user. The extension does not operate its own proxy servers.

## Third-Party Services

The extension does not share any user data with third parties. The extension does not include analytics, advertising, or tracking code.

## Data Retention

All data is stored locally on the user's device and persists until the user uninstalls the extension or clears the extension's data through Chrome settings.

License records on our server are retained for the duration of the subscription period plus 30 days after expiration.

## User Rights

Users can:
- View all stored data through Chrome's extension storage inspector
- Delete all data by uninstalling the extension
- Export and import proxy configurations through the extension's options page
- Remove their license key through the extension's settings

## Children's Privacy

ProxySwitcher is not directed at children under 13 and does not knowingly collect data from children.

## Changes to This Policy

We may update this privacy policy from time to time. Changes will be posted to this page with an updated "Last Updated" date.

## Contact

For privacy-related questions or concerns, please open an issue at:
https://github.com/Dwayne353/proxy-switcher/issues
