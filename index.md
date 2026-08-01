---
layout: default
title: Privacy Policy — Lista da Casa
description: Privacy Policy for the Lista da Casa app (Android/iOS). Last updated August 2, 2026 .
lang: en
---

# Privacy Policy

**Lista da Casa** — Gestão de Compras Domésticas  
**Developer:** Leankar.dev  
**Contact:** leankar.dev@gmail.com  
**Website:** [https://leankar.dev](https://leankar.dev)  
**Last updated:** August 2, 2026

---

## 1. Introduction

This Privacy Policy describes how **Lista da Casa** ("the App", "we", "our") handles information when you use our mobile application available on Google Play.

The App is designed with a **local-first** architecture: all user-generated data (shopping lists, items, markets, and preferences) is stored exclusively on your device and is never transmitted to our servers. However, the App displays banner and interstitial advertisements through **Start.io** (formerly StartApp), a third-party mobile advertising network operated by Start.io Inc. As a result, certain device and usage information is collected and processed by Start.io for advertising purposes, as described in this policy. The App also uses the **Google Play In-App Update API** to check for and install app updates, which involves communication with Google Play services.

---

## 2. Information We Collect

### 2.1 Information You Provide Directly

All data entered in the App is stored **exclusively on your device**. This includes:

| Data | Purpose | Storage |
|------|---------|---------|
| Username / Display name | Identify the local account | Device secure storage |
| Numeric PIN | Authenticate access to the App | Device secure storage (hashed + salted) |
| Shopping list names | Organize your lists | Local SQLite database |
| Shopping item names, quantities, prices, notes | Manage purchases | Local SQLite database |
| Category selections | Classify items | Local SQLite database |
| Market / store names and addresses | Track where you shop | Local SQLite database |
| Language preference | App localization | Device secure storage |

This data is never transmitted to us or any third party.

### 2.2 Information Collected by Start.io (Advertising SDK)

The App uses the **Start.io (StartApp) SDK** to display banner advertisements (shown on selected screens) and interstitial advertisements (shown occasionally, at most once every 30 minutes, after you complete a purchase in a shopping list). When ads are loaded, Start.io may automatically collect:

| Data | Purpose |
|------|---------|
| Advertising ID (GAID on Android, IDFA/IDFV on iOS) | Ad targeting and measurement |
| IP address | Geographic targeting and fraud prevention |
| Device model, OS version, carrier, and settings | Ad rendering and compatibility |
| App/ad interaction data | Performance measurement and fraud detection |
| Coarse location (derived from IP address) | Regional ad targeting |

The App does **not** request the device's Location permission, so Start.io cannot access GPS/precise location through the App — only the IP-derived approximate location described above. Start.io's SDK may, as part of its normal operation, also collect information about other apps installed on the device for ad-targeting purposes.

This data is collected and processed by **Start.io Inc.** under its own privacy policy. We do not receive, store, or process this data ourselves.

**Personalized vs. Non-Personalized Ads:** The App does not currently implement an in-app consent management dialog. Ad personalization and any related consent choices are governed by Start.io's own compliance mechanisms and by the ad-tracking controls available in your device settings (see Section 7).

### 2.3 Information We Do NOT Collect

We (Leankar.dev) do **not** collect any of the following:

- Real name, email address, phone number, or any identity document
- Location data or GPS coordinates
- Usage analytics or crash reports
- Contacts, photos, camera, or microphone data
- Payment or financial information
- Biometric data

---

## 3. How We Use Your Information

### 3.1 App Functionality

All user-provided data is used **solely within the App** to deliver its features:

- Display and manage your shopping lists
- Track item prices and purchase status
- Present spending history and analytics charts
- Maintain your language preference across sessions

### 3.2 Advertising

The App displays banner and interstitial advertisements provided by Start.io. The purpose of advertising is to sustain the App's ongoing development while keeping it free for users. Start.io uses the data described in Section 2.2 to select and display relevant advertisements.

We do not use your locally stored app data (shopping lists, items, markets) for advertising purposes.

### 3.3 App Updates

The App uses the **Google Play In-App Update API** to check whether a newer version is available and, depending on the update's priority, to prompt a flexible or immediate update. This feature communicates with Google Play services on your device and is governed by Google Play's own terms and privacy practices. No app data (shopping lists, items, markets) is shared through this feature.

---

## 4. Data Storage and Security

### 4.1 Where Your Data is Stored

| Storage Layer | Contents | Technology |
|---------------|----------|-----------|
| Secure storage | PIN (HMAC-SHA256 hashed with cryptographic salt), username, preferences | Android Keystore / iOS Keychain |
| Local database | Shopping lists, items, markets, history | SQLite (via Drift ORM), file: `lista_da_casa.db` |

**All user-provided data resides entirely on your device.** There is no cloud sync, no remote backup, and no server-side storage by us.

### 4.2 Security Measures

- **PIN hashing:** Your PIN is never stored in plain text. It is processed with HMAC-SHA256 using a unique cryptographic salt per device.
- **Secure storage:** Credentials are stored using platform-native secure storage (Android Keystore / iOS Keychain), not in plain files or shared preferences.
- **Brute-force protection:** After repeated failed login attempts, the App enforces progressive lockouts (30 seconds → 5 minutes → 1 hour).
- **Session timeout:** If the App is placed in the background for more than 15 minutes, you will be automatically logged out and must re-authenticate.
- **Timing-attack resistance:** PIN comparison uses constant-time evaluation to prevent information leakage.
- **Screen capture protection:** On Android, the App sets the `FLAG_SECURE` window flag at startup, which prevents screenshots, screen recordings, and App Switcher previews from capturing any App content.

### 4.3 Limitations

The local SQLite database itself is not encrypted at the file level. Physical access to a rooted or jailbroken device could expose the database contents. We recommend keeping your device secure and using a strong PIN.

---

## 5. Data Sharing and Disclosure

### 5.1 Your App Data

We do **not** share your locally stored data (shopping lists, items, markets) with anyone. This data never leaves your device.

### 5.2 Advertising Data (Start.io)

The App integrates the **Start.io** advertising SDK, which collects and processes the data described in Section 2.2. This constitutes a sharing of technical and usage data with a third party for advertising purposes. Start.io Inc. acts as an independent data controller for this data.

- **Start.io's Privacy Policy:** [https://www.start.io/policy/privacy-policy-site/](https://www.start.io/policy/privacy-policy-site/)
- **Start.io's Opt-Out / Right to Opt Out:** [https://www.start.io/optout-right/](https://www.start.io/optout-right/)
- **Start.io privacy requests:** privacy@start.io

### 5.3 App Update Data (Google Play)

The App's in-app update feature (Section 3.3) communicates with Google Play services to determine whether an update is available. This is governed by Google's own privacy policy: [https://policies.google.com/privacy](https://policies.google.com/privacy).

No other data is sold, rented, licensed, or shared with any party.

---

## 6. Third-Party SDKs and Libraries

The App uses the following open-source and third-party libraries:

| Library | Purpose | Data Collection |
|---------|---------|----------------|
| Drift / SQLite | Local database | None — local only |
| flutter\_secure\_storage | Platform-native secure storage | None — local only |
| crypto | PIN hashing | None — local only |
| google\_fonts | Font rendering (may cache fonts locally) | May request font files from Google servers; no personal data sent |
| fl\_chart | Charts and graphs | None |
| flutter\_riverpod | State management | None |
| flutter\_neumorphic\_plus | UI design system | None |
| url\_launcher | Opening external links (e.g. this policy, app store page) in the device's browser | None collected by the App itself |
| **startapp\_sdk** | **Banner and interstitial advertising (Start.io)** | **See Section 2.2 and Section 7** |
| **in\_app\_update** | **Google Play in-app update checks and prompts** | **See Section 3.3 and Section 5.3** |

> **Note on Google Fonts:** The `google_fonts` package may request font files from Google's servers on first use if fonts are not yet cached on the device. No personal data is included in these requests.

---

## 7. Advertising, Consent, and Regional Privacy Rights

### 7.1 Advertising Consent

The App does **not** currently display an in-app consent management dialog before loading ads. Instead:

- Ad-related identifiers (such as your Advertising ID) are subject to the controls your operating system provides — see Section 7.4 for how to reset or limit them.
- You can request Start.io to stop collecting, sharing, or using your data for targeted advertising at any time via their opt-out page ([https://www.start.io/optout-right/](https://www.start.io/optout-right/)) or by emailing privacy@start.io.
- If you are located in the EEA, UK, or another region with similar requirements, you may exercise the rights described in Sections 7.2–7.4 directly with Start.io or through your device's privacy settings.

### 7.2 European Union — GDPR

For users located in the EU/EEA, the following applies under the **General Data Protection Regulation (GDPR)**:

- **Data Controller for app data:** You are the sole data controller for all data stored locally in the App. We (Leankar.dev) do not process your personal data.
- **Data Controller for advertising data:** Start.io Inc., 584 Broadway, New York, NY 10012, USA.
- **Lawful basis for advertising:** Legitimate interest (Article 6(1)(f) GDPR) for ad delivery and measurement, since the App does not currently collect explicit consent through an in-app dialog. If you object, you can restrict processing using the controls in Section 7.1 and 7.4.
- **Data transfers outside the EU:** Start.io may transfer advertising data to servers in the United States and other countries. Refer to Start.io's privacy policy for the safeguards applied to such transfers.
- **Your rights:** You have the right to access, rectify, erase, restrict processing of, and port your data, as well as the right to object to profiling based on advertising data. Exercise these rights directly with Start.io at privacy@start.io or via [https://www.start.io/optout-right/](https://www.start.io/optout-right/), or by contacting us at leankar.dev@gmail.com.
- **Right to object:** You may object to processing based on legitimate interest at any time using the channels above.
- **Lodge a complaint:** You have the right to lodge a complaint with your local Data Protection Authority (DPA).

### 7.3 Brazil — LGPD

For users located in Brazil, the following applies under the **Lei Geral de Proteção de Dados (LGPD — Lei nº 13.709/2018)**:

- **Controller for app data:** You are the sole controller for all data stored locally in the App. We (Leankar.dev) process no personal data on our end.
- **Operator for advertising data:** Start.io Inc. acts as an operator (operador) processing advertising data as described in Section 2.2.
- **Legal basis for advertising:** Legitimate interest (interesse legítimo) for ad delivery, personalization, and fraud prevention. The App does not currently present an in-app consent dialog; you may object or opt out through the channels in Section 7.1.
- **Your rights under LGPD:** Confirmation of processing, access, correction, anonymization or deletion of unnecessary data, portability, information about third parties with whom data is shared, right to revoke consent, and right to file a complaint with the ANPD (Autoridade Nacional de Proteção de Dados).
- **Data Processing Report (RIPD):** If required, you may request information about our data processing activities by contacting leankar.dev@gmail.com.
- **DPO Contact:** leankar.dev@gmail.com

### 7.4 United States — CCPA / US State Privacy Laws

For users located in California and other US states with applicable privacy laws:

- **Personal Information collected by Start.io:** The advertising data described in Section 2.2 (advertising ID, IP address, device information, interaction data) is collected by Start.io and may constitute "personal information" under the California Consumer Privacy Act (CCPA) / California Privacy Rights Act (CPRA).
- **Sharing for cross-context behavioral advertising:** The integration of the Start.io SDK may be considered "sharing" personal information for cross-context behavioral advertising under CCPA. You have the right to opt out of this sharing.
- **Opt-out options:**
  - Reset or limit your Advertising ID: *Android:* Settings → Privacy → Ads → Delete advertising ID (Android 12+) or Opt out of Ads Personalization. *iOS:* Settings → Privacy & Security → Tracking → disable tracking.
  - Opt out directly with Start.io: [https://www.start.io/optout-right/](https://www.start.io/optout-right/) or privacy@start.io
- **Your CCPA rights:** Right to know what personal information is collected, right to delete, right to opt out of sale/sharing, right to non-discrimination.
- **Do Not Sell or Share My Personal Information:** We do not sell personal information. To opt out of sharing with Start.io for advertising, use the controls listed above.
- **Contact:** leankar.dev@gmail.com for any privacy requests.

---

## 8. Your Rights and Data Control

Because all user-provided data is local to your device, you have full and immediate control:

| Right | How to Exercise |
|-------|----------------|
| **Access** | All your data is visible directly within the App |
| **Correction** | Edit any list, item, or market from within the App |
| **Deletion** | Delete individual items, lists, or markets within the App; use "Delete Account" in Settings to erase all data |
| **Portability** | The SQLite database file (`lista_da_casa.db`) can be accessed and exported from the application data directory |
| **Withdraw** | Uninstall the App — all local data is permanently deleted from the device |
| **Ad Preferences** | Opt out directly with Start.io at [start.io/optout-right](https://www.start.io/optout-right/) or privacy@start.io |
| **Advertising ID** | Reset or delete via device settings (see Section 7.4) |

For rights requests related to advertising data collected by Start.io, contact Start.io directly (privacy@start.io) or use the controls described in Section 7.

---

## 9. Children's Privacy

The App does not knowingly collect personal information from children under the age of 13 (or the applicable minimum age in your jurisdiction). The App contains no social features, no accounts linked to real identities, and no online communication.

The advertising displayed through Start.io is configured for a **general audience**. If you believe a child is using the App, we recommend using parental control features available on your device to limit ad-related data collection.

If you are a parent or guardian and have concerns, please contact us at leankar.dev@gmail.com.

---

## 10. Data Retention

### 10.1 Your App Data

Data is stored on your device for as long as the App is installed and you choose to retain it. There is no automated expiration of data. When you uninstall the App, the operating system removes all application data, including the SQLite database and all secure storage entries.

### 10.2 Advertising Data (Start.io)

Advertising data collected by Start.io is retained according to Start.io's own data retention policies. For details, see [Start.io's Privacy Policy](https://www.start.io/policy/privacy-policy-site/).

---

## 11. Internet and Device Permissions

The App requests the following permission:

| Permission | Required For |
|-----------|-------------|
| `INTERNET` | Loading and displaying advertisements (Start.io) and checking for app updates (Google Play In-App Update) |

The App does **not** request access to:

- Location (GPS or network-based)
- Camera or microphone
- Contacts or calendar
- External storage

All user-provided data (lists, items, markets, credentials) is accessed only within the App's own sandboxed application directory on the device. Note that, independent of the permissions listed above, the Start.io advertising SDK may automatically access certain device-level and network-level information (such as the Advertising ID, IP address, and technical device data) as described in Section 2.2, as is standard for mobile advertising SDKs.

---

## 12. Changes to This Policy

We may update this Privacy Policy to reflect changes in the App's features or applicable law. When we do:

- The "Last updated" date at the top of this page will be revised
- If the change is material, we will note it in the App's store listing release notes

Continued use of the App after an update constitutes acceptance of the revised policy. We encourage you to review this page periodically.

---

## 13. Contact Us

If you have any questions or concerns about this Privacy Policy or the App's data practices, please contact us:

**Email:** leankar.dev@gmail.com  
**Website:** [https://leankar.dev](https://leankar.dev)  
**App:** Lista da Casa — available on Google Play  

We will respond to all inquiries within 30 days. For EU/EEA users: we will respond within the timeframes required by GDPR (typically within one month, extendable to three months for complex requests).

---

*© 2026 LeanKar. All rights reserved.*
