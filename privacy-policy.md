# DeSpark — Privacy Policy

**Effective date:** June 25, 2026

This policy explains what data DeSpark collects, why, and the choices you have. It is written in plain English on purpose — you should be able to read it in a few minutes.

---

## The short version

DeSpark removes unwanted objects and distractions from your photos, and the image editing happens **entirely on your device**. **Your photos are never uploaded** — not to us, not to anyone.

To keep the app free and to improve it, DeSpark works with a few other companies: it sends a small amount of **anonymous diagnostic data** to Google Firebase (which features you use and crash reports — never your images), and the **free version shows ads** from Google AdMob, which — only with your permission — may use a device advertising identifier to show and measure ads. An optional **Pro** purchase removes all ads. Your photos are never part of any of this and never leave your device.

---

## 1. Who we are

DeSpark is an app that removes unwanted objects and distractions from photos. It is developed and operated by **Abdullah Al Hadi** ("we", "us"). For the purposes of the EU / UK / EEA General Data Protection Regulation (GDPR) and the California Consumer Privacy Act (CCPA/CPRA), Abdullah Al Hadi is the **data controller** for personal data collected through the app. For any privacy question, contact us at **mukashi.dev@gmail.com**.

This policy covers the DeSpark app on **iOS, iPadOS, Android, and macOS**, including the iOS Share Extension ("Share → DeSpark"). The ads described in §4 are shown on iOS, iPadOS, and Android; the macOS build does not display ads.

---

## 2. Data that stays on your device — never sent anywhere

The following lives only on your device, in the app's private storage. We have no server that stores it and no way to read it.

- **The images you clean** — the picture you pick, paste, or share into the app, and the cleaned result. These are processed on-device and are never uploaded.
- **Your in-app gallery** — the before/after pairs the app keeps so you can reopen them later, stored in the app's private container.
- **App state** — small flags such as whether you've seen the onboarding and how many results you've kept (used to decide when to offer a review prompt) and your local preferences.

You can delete the gallery at any time (**Settings → Clear gallery**, or delete an individual result). Uninstalling the app removes all of it.

If you have iCloud Backup (iOS) or device backup (Android/macOS) enabled, your operating system may include the app's local data in a backup you control in system settings. Those backups are between you and Apple/Google; we have no access to them.

---

## 3. Data sent to Firebase (Google)

We use two Firebase services from Google: **Analytics** and **Crashlytics**. Both are configured with the minimum data surface needed for product decisions and crash fixing — Firebase itself uses **no advertising identifiers** and does no cross-app tracking. (The separate, permission-gated advertising identifier used to show ads is described in §4.)

### Firebase Analytics collects:

- App-scoped identifiers only (Apple's IDFV / a Firebase installation ID). These cannot identify you across other apps.
- Device type, OS version, app version, language, and country (derived from IP).
- Which screens you view in the app.
- Aggregate feature usage, so we can decide what to keep, fix, or improve. For example:
  - How an image entered the app — *gallery*, *paste*, or *share* (and whether a paste found no image) — never the image itself.
  - The result of automatic cleanup — *detected*, *low confidence*, *not detected*, or *manual* — whether something was removed, and the output format (*jpg* or *png*).
  - Whether processing failed, with a generic reason (e.g. *too large*, *decode failed*).
  - Use of the manual brush (opened, an erase applied, kept) and the "try auto-clean anyway" action.
  - Saving and sharing a result, and which screen it came from.
  - Gallery actions — opening, deleting, or clearing kept results (counts only).
  - Onboarding completion, tab navigation, review prompts, and which Settings support rows you tap.

Each event carries at most a few categorical labels (like `source: paste`). **No free-form text and no image content is ever included.**

Firebase Analytics is configured **not** to collect your advertising identifier (IDFA/AAID); it cannot link you across other apps or websites.

### Firebase Crashlytics collects data only when the app crashes:

- Stack traces from the crash.
- A snapshot of device state at the time of the crash (OS version, device model, memory/disk, locale).
- A non-fatal error we report if the image-processing step fails unexpectedly — we send only the error's **type**, never the image or any text derived from it.

Crashlytics is **disabled in our development builds** (`setCrashlyticsCollectionEnabled(!kDebugMode)`); it is active in the release build you install from a store.

**What we never send to Firebase:** the image you are cleaning, the cleaned result, any image bytes, pixels, file names, file paths, or photo metadata (EXIF). All editing happens on your device; the picture itself does not leave it.

**Legal basis (EEA / UK / Switzerland).** Where the GDPR or UK GDPR applies, we process this anonymous analytics and crash-diagnostic data under our **legitimate interests** (Art. 6(1)(f)) — understanding how the app is used and keeping it stable — balanced against your privacy. You can object at any time (see §12).

---

## 4. Ads (Google AdMob)

The free version of DeSpark is supported by ads from **Google AdMob** — a banner on the home screen and an occasional full-screen ad between actions. Buying **Pro** (see §5) removes all ads. Ads appear on iOS, iPadOS, and Android; the macOS build shows no ads.

To request and measure ads, Google's Mobile Ads SDK collects and shares with Google:

- a **device advertising identifier** (Apple's IDFA on iOS, the Advertising ID on Android) — used only if you grant permission (see consent below);
- your **IP address** and the **coarse location/region** derived from it;
- **device and app information** (model, OS version, app version, language); and
- **ad interactions** — which ads were shown, and whether you tapped one.

Google uses this to serve ads, cap how often you see the same ad, detect invalid activity, and measure performance — and, where you have granted permission, to show **personalized** (more relevant) ads. Google acts as an independent controller for the ad data it receives; see the [Google Privacy Policy](https://policies.google.com/privacy) and [how Google uses information from apps that use its services](https://policies.google.com/technologies/partner-sites).

**Your consent and choices.** Before any ad loads, on first launch:

- **iOS — App Tracking Transparency.** The system asks permission to use your device's advertising identifier (IDFA). If you choose **"Ask App Not to Track,"** your IDFA is not used and ads are **non-personalized**. You can change this any time in **Settings → Privacy & Security → Tracking**.
- **EEA, UK, and Switzerland.** Google's **User Messaging Platform (UMP)** shows a consent form; your choice there determines whether ads are personalized or non-personalized.
- If permission or consent isn't granted, the app shows **non-personalized** ads — or, if the ad system can't initialize, simply runs without ads.

**SKAdNetwork (iOS).** DeSpark includes Apple's SKAdNetwork identifiers so advertising can be attributed and measured in a privacy-preserving way that does not identify you.

**Your photos are never used for advertising** and are never shared with the ad network.

---

## 5. Purchases & subscriptions (RevenueCat, Apple, Google)

DeSpark is free to use. You can optionally upgrade to **Pro** — a weekly subscription or a one-time lifetime purchase — which **removes all ads**. Purchasing is entirely optional.

- **Payment** is handled by **Apple (App Store)** or **Google (Google Play)**. We never see or store your card number, billing address, or other payment details — the store processes the payment under its own privacy policy.
- We use **RevenueCat** to check and restore what you've purchased. RevenueCat receives a **randomly generated, app-specific user ID** (not your name or email), your **purchase and transaction history** and store **receipt**, and basic **device, platform, and country** information, so the app can tell whether Pro is active and restore it on a new device. RevenueCat is our service provider and uses this data only to deliver and support your purchase; see the [RevenueCat Privacy Policy](https://www.revenuecat.com/privacy/).
- This purchase data is **not** linked to the images you edit or to your photo library.

---

## 6. The "Report a bug" email path

If an image doesn't clean correctly, the app offers **"Report this image"** (and Settings → **Report a bug**). These open a pre-filled email **in your own mail app**. A bug report pre-fills your app version, platform, OS version, and device model, and — only if you choose to attach it — the image that failed.

Nothing is sent until you press Send in your mail app. The image, and anything else in the email, reaches us **only by your explicit action**, via your email provider to **mukashi.dev@gmail.com**. This is the only way an image would ever leave your device, and only because you chose to send it to help us reproduce a bug.

---

## 7. Permissions the app asks for

- **Photo library** — on iOS, iPadOS, and Android, to pick the image you want to clean and to save the cleaned result back to your library. On macOS we open images through a standard file picker and request only add-to-Photos access to save results. We read only the image(s) you explicitly select, and save only when you tap Save. Your photos are not uploaded.
- **Clipboard** — read only when you tap "Paste image", to bring in an image you copied.
- **App Tracking Transparency (iOS)** — a one-time prompt asking whether DeSpark may use your device's advertising identifier for ads (see §4). Saying no still lets the app work, with non-personalized ads.
- **Network** — used by the Firebase SDKs (§3) to send diagnostic data, by Google AdMob (§4) to request and measure ads in the free version, by the purchase system (§5) to validate and restore Pro, and (on iOS and Android) by the in-app browser that shows this policy. On macOS the app is sandboxed and is granted only outbound network (`network.client`) and add-to-photo-library access for saving results.
- DeSpark does **not** use the camera, microphone, precise location, contacts, or calendar.

---

## 8. How on-device editing works

All detection and editing run **on-device**, in the app. DeSpark removes only the visible content you select or that automatic cleanup targets. No image is uploaded for processing.

---

## 9. What we never do

- We never upload, store, or transmit **the images you edit** — image content stays on your device and leaves it only via a bug-report email **you** choose to send (§6).
- We never use your **photos** to target or personalize ads, and we never share your images with the ad network or any other third party.
- We never **sell your personal information for money.**
- We don't link your analytics, ad, or purchase data to your real-world identity — there is no account system and we never ask for your name.

---

## 10. Third parties

- **Firebase** (Google LLC) — Analytics and Crashlytics, processed as our service provider under the [Firebase Data Processing and Security Terms](https://firebase.google.com/terms/data-processing-terms). Google's own practices are covered by the [Google Privacy Policy](https://policies.google.com/privacy). Google primarily processes this data on servers in the **United States**; for EEA/UK/Swiss users, transfers rely on Google's Standard Contractual Clauses and the UK International Data Transfer Addendum.
- **Google AdMob** (Google LLC) — serves the ads in the free version of the app (§4), covered by the [Google Privacy Policy](https://policies.google.com/privacy). Google may use the ad data it receives as an independent controller.
- **RevenueCat, Inc.** — manages subscription and purchase entitlements (§5) as our service provider; see the [RevenueCat Privacy Policy](https://www.revenuecat.com/privacy/).
- **Apple App Store / Google Play** — install, review, and rate prompts, **and processing your purchases**. Governed by Apple's and Google's own privacy policies.
- **Gmail** (Google LLC) — receives a support email only if you choose to send one.
- **GitHub Pages** — hosts this policy page; GitHub may log standard request data (such as your IP address) when you open it.

---

## 11. How long we keep it

- **On-device data** — until you delete it or uninstall the app.
- **Firebase Analytics** — Google retains event-level data per its default window (up to 14 months), after which older events are aggregated or dropped.
- **Firebase Crashlytics** — Google retains crash reports for **90 days**.
- **Advertising data** — retained by Google according to the [Google Privacy Policy](https://policies.google.com/privacy); we keep no ad data ourselves.
- **Purchase data** — RevenueCat and the app stores keep purchase records for as long as needed to provide, restore, and support your purchase and to meet legal, tax, and accounting obligations.
- **Support emails** — kept in our inbox no longer than needed to handle your request and any follow-up.

---

## 12. Your rights and choices

- **Delete your in-app gallery** any time — **Settings → Clear gallery**, or delete an individual result.
- **Control ad personalization** — on **iOS**, change your choice in **Settings → Privacy & Security → Tracking**; on **Android**, reset or delete your Advertising ID in system settings. Opting out switches you to non-personalized ads.
- **Remove ads entirely** — upgrade to **Pro** (in **Settings**), which turns off all ads.
- **Stop all telemetry** — uninstalling the app stops any further analytics and crash reporting from your device and invalidates the Firebase installation ID.
- **Access or erase your data** under GDPR (EEA, UK), CCPA/CPRA (California), Brazil's LGPD, or similar laws — email **mukashi.dev@gmail.com**. Because we don't tie analytics or ad data to a persistent identity, the most reliable erasure is uninstalling the app and resetting your device advertising identifier.
- **Lodge a complaint** — if you're in the EEA, UK, or Switzerland, you may complain to your local data protection authority. We'd appreciate the chance to address your concern first — email **mukashi.dev@gmail.com** and we'll respond within 30 days.

We don't sell your personal information for money. If you allow tracking, your device's advertising identifier may be used to personalize ads — which California law (CCPA/CPRA) treats as **"sharing"** for cross-context behavioral advertising. You can opt out at any time by denying tracking (iOS) or resetting your Advertising ID (Android), declining the consent form where it's shown, or upgrading to **Pro**.

---

## 13. Children's privacy

DeSpark is a general-audience app and is not directed at children under 13 (or the equivalent age in your region). We don't knowingly collect personal data from children. If you believe a child has used the app and want associated diagnostic data removed, email **mukashi.dev@gmail.com**.

---

## 14. Security

- On-device data is stored in the app's private sandbox. Data sent to Firebase, the ad network, and the purchase system travels over HTTPS (TLS).
- We operate no server that holds your content, so there is no central store of your images to breach.
- No method of transmission or storage is 100% secure. If we become aware of a breach affecting your data, we will notify you as required by applicable law.

---

## 15. Changes to this policy

If we change this policy, the new version replaces this page at **https://hadicuet.github.io/despark-legal/** and the "Effective date" above is updated. Material changes (such as a new third-party service or a new category of data) will be called out in the app's release notes.

---

## 16. Contact us

Questions, requests, or complaints: **mukashi.dev@gmail.com**.

*© Abdullah Al Hadi. Last updated June 25, 2026.*
