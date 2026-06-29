# Privacy Policy — ProxySwitcher

**Last Updated:** June 29, 2026  
**Extension Name:** ProxySwitcher  
**Developer:** Dwayne353  
**Contact:** al68998e@gmail.com

---

## Overview

ProxySwitcher ("the Extension") is a Chrome browser extension that manages proxy connections, provides privacy protection features, and monitors proxy performance. This Privacy Policy explains what data the Extension collects, how it is used, and how it is stored.

**We are committed to your privacy. ProxySwitcher does not collect, transmit, sell, or share your personal data or browsing history with anyone.**

---

## Data Collection & Usage

### Data Stored Locally on Your Device

The following data is stored **exclusively on your device** using Chrome's built-in `chrome.storage.local` API. This data **never leaves your device** and is **never transmitted** to any external server:

| Data Type | Purpose | Storage Duration |
|---|---|---|
| **Proxy profile configurations** | Store your proxy server details (host, port, protocol, authentication credentials) so you can switch between them | Until you delete the profile |
| **Extension preferences** | Remember your settings (privacy toggles, auto-rotation interval, theme, etc.) | Until you change or reset settings |
| **Traffic statistics** | Display per-proxy request counts and bandwidth usage in the Traffic Analytics dashboard | Rolling 30-day window |
| **Health monitoring data** | Display proxy latency, uptime percentage, and status in the Health Dashboard | Until you clear health data |
| **Connection event logs** | Display connection activity history for debugging and monitoring | Rolling log (last 200 events) |
| **License/subscription status** | Track whether your subscription is active for premium features | Until subscription expires |

### Data Transmitted Off-Device

| Data Type | Destination | Purpose | When |
|---|---|---|---|
| **License key** | Self-hosted license validation server (`proxyswitcher-license.onrender.com`) | Validate subscription status for premium features | When you activate or verify a license key |
| **Proxy traffic** | Your configured proxy server(s) | Route your web browsing traffic through the proxy you selected | When a proxy profile is active |

**No other data is ever transmitted off your device.**

### Data NOT Collected

The Extension does **NOT** collect, store, or transmit:

- ❌ Browsing history or visited URLs
- ❌ Search queries
- ❌ Personal information (name, email, address, phone number)
- ❌ Financial or payment information
- ❌ Location data
- ❌ Cookies or session data
- ❌ Form data or passwords (other than proxy authentication credentials you enter)
- ❌ Website content
- ❌ IP addresses
- ❌ Device identifiers or hardware fingerprints
- ❌ Analytics or telemetry data
- ❌ Crash reports

---

## Privacy Protection Features

ProxySwitcher includes several privacy-enhancing features that run **entirely locally** on your device:

### WebRTC Leak Protection
Configures Chrome's WebRTC policy (`disable_non_proxied_udp`) to prevent your real IP address from leaking through WebRTC STUN/TURN connections when a proxy is active.

### DNS Leak Prevention
Disables speculative DNS prefetching to ensure all DNS queries are routed through your proxy tunnel, preventing DNS leak detection.

### Timezone Spoofing
Overrides JavaScript `Date` and `Intl.DateTimeFormat` APIs in web pages to match your browser's apparent timezone to your proxy server's geographic location.

### Device Identity
Overrides browser fingerprint signals (user agent string, screen resolution, touch support, device memory, hardware concurrency, plugins, media queries, and Client Hints headers) to present a consistent device identity matching your selected profile (Windows, Mac, iPhone, or Android).

### Canvas, WebGL & AudioContext Fingerprint Protection
Injects imperceptible noise into Canvas, WebGL, and AudioContext API outputs to prevent cross-site browser fingerprinting. Each session generates unique noise values.

### Geolocation & Language Matching
Overrides `navigator.language`, `navigator.languages`, and geolocation APIs to match your proxy's country of origin.

**All of these features execute locally within your browser. No data from these features is transmitted anywhere.**

---

## Third-Party Services

### Proxy Servers
When you activate a proxy profile, your web traffic is routed through the proxy server **you configure**. ProxySwitcher does not operate or control any proxy servers. Your choice of proxy provider and their privacy practices are your responsibility.

### ProxyScrape (Optional)
If you use the "Fetch Free Proxies" feature, the Extension makes a request to the ProxyScrape public API (`api.proxyscrape.com`) to retrieve a list of free proxy servers. No personal data is sent in this request.

### Speed Test (Optional)
When you run a speed test, the Extension downloads a small file (~1MB) from Cloudflare's public CDN (`speed.cloudflare.com`) to measure download speed through your proxy. No personal data is sent.

### IP Reputation Check (Optional)
When you check a proxy's IP reputation, the Extension queries public IP reputation APIs. Only the proxy server's IP address is sent — never your real IP.

### License Validation
When you activate a premium license key, the Extension sends the license key to a self-hosted validation server. No personal data, browsing history, or proxy configurations are included in this request.

---

## Permissions Justification

The Extension requests the following Chrome permissions:

| Permission | Justification |
|---|---|
| `proxy` | Required to configure Chrome's proxy settings when you activate a profile. This is the core functionality. |
| `storage` | Stores proxy profiles, preferences, and statistics locally using Chrome's secure storage API. |
| `privacy` | Configures WebRTC leak protection and DNS leak prevention settings. |
| `scripting` | Injects privacy protection scripts (timezone, fingerprint, identity) into web pages. |
| `webRequest` | Monitors proxy connection events for logging, error reporting, and traffic analytics. |
| `webRequestAuthProvider` | Provides proxy authentication credentials automatically so you don't see repeated login prompts. |
| `tabs` | Reads tab URLs to apply per-URL proxy routing rules and inject privacy scripts. |
| `webNavigation` | Detects page navigations to inject privacy scripts into new pages as they load. |
| `notifications` | Notifies you when proxies connect/disconnect, errors occur, or auto-rotation switches profiles. |
| `contextMenus` | Adds a right-click menu for quick profile switching. |
| `alarms` | Provides reliable timers for auto-rotation and periodic health checks. |
| `declarativeNetRequest` | Modifies outgoing HTTP headers (User-Agent, Client Hints) for device identity features. |
| `<all_urls>` | Required by Chrome's proxy API to route traffic from any website through your proxy. Also needed for privacy script injection across all domains. |

---

## Data Sharing

**We do not share your data with any third parties.**

- ❌ Data is NOT sold to third parties, data brokers, or information resellers
- ❌ Data is NOT used or transferred for purposes unrelated to the Extension's core functionality
- ❌ Data is NOT used or transferred for determining creditworthiness or for lending purposes
- ❌ Data is NOT used for advertising, marketing, or user profiling
- ❌ Data is NOT shared with analytics providers

---

## Data Security

- All data is stored locally using Chrome's built-in `chrome.storage.local` API, which is sandboxed to the Extension
- Proxy authentication credentials are stored in Chrome's secure local storage and are only used to authenticate with proxy servers you configure
- No data is stored on external servers (except license key validation status)
- The Extension does not create accounts or require registration

---

## Data Retention & Deletion

- **Proxy profiles**: Retained until you manually delete them
- **Traffic statistics**: Rolling 30-day window; older data is automatically purged
- **Health monitoring data**: Retained until you clear it or uninstall the Extension
- **Connection logs**: Rolling buffer of the last 200 events
- **All data**: Completely deleted when you uninstall the Extension from Chrome

You can also clear all Extension data at any time by going to `chrome://extensions`, clicking "Details" on ProxySwitcher, and selecting "Clear data."

---

## Children's Privacy

ProxySwitcher is not directed at children under the age of 13. We do not knowingly collect personal information from children.

---

## Changes to This Policy

We may update this Privacy Policy from time to time. Changes will be posted to this page with an updated "Last Updated" date. Continued use of the Extension after changes constitutes acceptance of the updated policy.

---

## Your Rights

Since ProxySwitcher stores all data locally on your device and does not collect personal data on any server, there is no personal data for us to access, modify, or delete on your behalf. You have full control over all data stored by the Extension through Chrome's built-in extension management.

---

## Contact

If you have questions about this Privacy Policy or the Extension's data practices:

- **Email:** al68998e@gmail.com
- **GitHub Issues:** [https://github.com/Dwayne353/proxyswitcher-privacy/issues](https://github.com/Dwayne353/proxyswitcher-privacy/issues)

---

© 2026 Dwayne353. All rights reserved.
