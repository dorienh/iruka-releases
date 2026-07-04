# Iruka — Privacy Policy

**Last updated: 4 July 2026**

This policy explains what information Iruka collects and how it is used.

---

## What Iruka collects

Iruka collects the minimum necessary to operate:

| Data | Purpose | Where stored |
|---|---|---|
| License key | Identify your purchase | On your Mac (UserDefaults) |
| License instance ID | Verify this Mac is authorised | On your Mac (Keychain) |
| Update period expiry date | Determine update eligibility | On your Mac (UserDefaults) |
| License tier and machine limit | Display your plan in Settings | On your Mac (UserDefaults) |

None of this data is sent anywhere except to the LemonSqueezy license API at `api.lemonsqueezy.com` to activate or validate your license. No personal information is stored on any server controlled by Dorien Herremans.

## What Iruka does not collect

- No analytics or usage tracking of any kind
- No crash reporting sent anywhere
- No file names, paths, or contents you browse
- No identifiers beyond the license instance ID

## Payments

Purchases are handled by **LemonSqueezy** (Lemon Squeezy, LLC). When you buy a license your payment details (name, email, card) are collected by LemonSqueezy, not by Iruka or Dorien Herremans. LemonSqueezy's privacy policy applies to that data: [lemonsqueezy.com/privacy](https://www.lemonsqueezy.com/privacy)

## Local storage

Iruka stores license information locally on your Mac using standard macOS mechanisms:

- **UserDefaults** — license key, tier, expiry date (not sensitive; readable by you via `defaults read`)
- **Keychain** — license instance ID (protected by macOS Keychain access controls)

Deactivating your license in Settings → License removes all stored data from both locations.

## Sparkle (software updates)

Iruka uses [Sparkle](https://sparkle-project.org) to check for updates. Sparkle contacts the appcast feed at `raw.githubusercontent.com` — a public URL — with no identifying information beyond a standard HTTP request.

## Your rights

You can view or delete all locally stored license data at any time by deactivating your license in **Settings → License**. For questions or requests related to any personal data LemonSqueezy may hold on your behalf, contact LemonSqueezy directly.

## Contact

Questions about this policy: [dorien.herremans@gmail.com](mailto:dorien.herremans@gmail.com)
