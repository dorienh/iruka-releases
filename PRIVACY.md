# Iruka — Privacy Policy

**Last updated: 7 November 2026**

This policy explains what the Iruka app and the `iruka.sh` website collect, why, and where it goes. Iruka is made by Dorien Herremans.

---

## What the app never sends

- The names, paths or contents of your files and folders
- Crash reports
- Advertising IDs
- Your server, SSH or cloud passwords and keys, which stay in the macOS Keychain on your Mac

## What the app sends

The app makes three kinds of connection on its own:

| Connection | What is sent | Goes to | Why |
|---|---|---|---|
| Update check, once a day | Install ID, app version and build, license status. Sparkle, the update framework, may also send macOS version, CPU type, Mac model, system language and RAM amount. | `iruka.sh` | Offer updates, count installs, decide which systems to support |
| Daily ping | Install ID, app version and build, license status, license tier, and a salted hash of your license key if you have one | `iruka.sh` | Count active installs, detect cracked or refunded licenses |
| License activation and validation | Your license key, and when activating, your Mac's name as set in System Settings | Lemon Squeezy (`api.lemonsqueezy.com`) | Activate your license and confirm it is valid |

You can turn off automatic update checks in Settings. The daily ping can't currently be turned off.

Other connections happen only when you set them up, such as SSH sessions, server and cloud mounts, and git remotes. These go to the servers you choose, not to us.

## The install ID

Each install creates a random ID, stored on your Mac. It isn't derived from your hardware or from personal data.

During a trial, nothing connects this ID to you. Once a license key is entered, the daily ping sends a salted hash of that key together with the install ID. We can match the hash against our purchase records, so **for a licensed install, the install ID and its usage records can be linked to your purchase, including your name and email**. We use this to check that installs reporting a license match a real purchase.

## What we store

These records are kept on servers controlled by Dorien Herremans, using Supabase (database) and Vercel (hosting):

- **Install records:** the update check and daily ping data listed above, with the dates they were received. We don't save your IP address in these records, though Vercel may process it to deliver the request.
- **License and order records:** a copy of what Lemon Squeezy holds about your license and order, updated hourly. This includes your name, email, license key, order amounts, tax, discounts and refund status, and the name of each Mac you activated.

We use license and order records for customer support, to detect misuse, and to re-issue licenses if the Lemon Squeezy account ever became unavailable. There is currently no fixed date when these records are deleted automatically.

## Payments

Purchases are handled by **Lemon Squeezy** (Lemon Squeezy, LLC), which processes your payment. We don't receive your full card number. Lemon Squeezy's privacy policy also applies: [lemonsqueezy.com/privacy](https://www.lemonsqueezy.com/privacy)

## The iruka.sh website

The website uses these analytics and advertising tools:

- **Google Analytics** and **Vercel Analytics** measure visits and how the site is used.
- **Google Ads** records when someone reaches the download page, to measure our ads.
- **OpenAI Ads** records page views and downloads, to measure our ads.
- **X Ads** records site visits. If you continue to our thank-you page after buying, it also receives your order ID and, when the total is in US dollars, the amount.

These services may set cookies or similar identifiers in your browser and handle the data under their own policies. You can block them with your browser's settings or a content blocker, and the site will still work.

Embedded videos use YouTube's privacy-enhanced mode (`youtube-nocookie.com`).

## Affiliate referrals

The website runs Lemon Squeezy's affiliate tracking script. If you arrive through an affiliate link (a URL containing `?aff=`), Lemon Squeezy stores that affiliate's referral code in a cookie in your browser for 60 days and adds it to the checkout links on the site. If you then buy a license, the affiliate who referred you earns a commission. You pay the same price either way. The cookie holds only the affiliate's code, not information about you. You can clear it at any time by deleting cookies for `iruka.sh` in your browser.

## Stored on your Mac

- **UserDefaults:** license key, tier, expiry date, install ID and your settings
- **Application Support** (`~/Library/Application Support/Iruka/`): license instance ID, update period details and trial dates
- **Keychain:** passwords and keys for your saved connections

Deactivating your license in **Settings → License** removes the license key, tier, expiry date and instance ID from your Mac. It keeps your renewal history, install ID and trial dates, and it doesn't delete anything from our servers.

## Your rights

To ask what we hold about you, or to have it corrected or deleted, open a thread in [GitHub Discussions](https://github.com/dorienh/iruka-releases/discussions). Discussions are public, so please don't post your license key or personal details there. We'll arrange a private way to continue. Some order records may need to be kept for tax or legal reasons. For data held by Lemon Squeezy, you can also contact Lemon Squeezy directly.

## Contact

Questions about this policy? Open a thread in [GitHub Discussions](https://github.com/dorienh/iruka-releases/discussions).
