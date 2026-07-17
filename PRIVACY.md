# Iruka — Privacy Policy

**Last updated: 17 July 2026**

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

License data is sent only to the LemonSqueezy license API at `api.lemonsqueezy.com` to activate or validate your license. Update check data (see Sparkle section below) is stored anonymously on servers controlled by Dorien Herremans. No personal information is ever stored.

## What Iruka does not collect

- No crash reporting sent anywhere
- No file names, paths, or contents you browse
- No personal identifiers — the install ID in update checks is a random number, not linked to you, your license, or your hardware
- No advertising IDs or cross-app tracking

## Payments

Purchases are handled by **LemonSqueezy** (Lemon Squeezy, LLC). When you buy a license your payment details (name, email, card) are collected by LemonSqueezy, not by Iruka or Dorien Herremans. LemonSqueezy's privacy policy applies to that data: [lemonsqueezy.com/privacy](https://www.lemonsqueezy.com/privacy)

## Local storage

Iruka stores license information locally on your Mac using standard macOS mechanisms:

- **UserDefaults** — license key, tier, expiry date, anonymous install ID (not sensitive)
- **Keychain** — license instance ID (protected by macOS Keychain access controls)

Deactivating your license in Settings → License removes all stored license data from both locations.

## Sparkle (software updates)

Iruka uses [Sparkle](https://sparkle-project.org) to check for updates. When checking, Sparkle may send anonymous technical details to `iruka.dorienherremans.com`:

- App version and build number
- macOS version
- CPU architecture (Apple Silicon or Intel)
- Mac model identifier (e.g. MacBookPro18,1)
- System language
- RAM amount
- A random anonymous install ID (generated once on first launch, stored on your Mac)

Each install generates a random ID stored only on your Mac and sent with update checks so we can count unique installs. It is not derived from your hardware, license, or any personal data. This data is stored anonymously to understand how many installs are active and which platforms to support.

## Your rights

You can view or delete all locally stored data at any time by deactivating your license in **Settings → License**. For questions or requests related to any personal data LemonSqueezy may hold on your behalf, contact LemonSqueezy directly.

## Contact

Questions about this policy: [dorien.herremans@gmail.com](mailto:dorien.herremans@gmail.com)
