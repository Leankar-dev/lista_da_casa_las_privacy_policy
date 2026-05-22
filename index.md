---
layout: default
title: Privacy Policy — Lista da Casa
description: Privacy Policy for the Lista da Casa app (Android/iOS). Last updated May 22, 2026 .
lang: en
---

# Privacy Policy

**Lista da Casa** — Gestão de Compras Domésticas  
**Developer:** Leankar.dev  
**Contact:** leankar.dev@gmail.com  
**Website:** [https://leankar.dev](https://leankar.dev)  
**Last updated:** May 22, 2026

---

## 1. Introduction

This Privacy Policy describes how **Lista da Casa** ("the App", "we", "our") handles information when you use our mobile application available on Google Play.

The App is designed with a **local-first** architecture: all user-generated data (shopping lists, items, markets, and preferences) is stored exclusively on your device and is never transmitted to our servers. However, the App displays advertisements through **Google AdMob**, a third-party advertising service provided by Google LLC. As a result, certain device and usage information is collected and processed by Google for advertising purposes, as described in this policy.

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

### 2.2 Information Collected by Google AdMob

The App uses **Google AdMob** to display banner advertisements. When ads are loaded, Google may automatically collect:

| Data | Purpose |
|------|---------|
| Advertising ID (GAID on Android, IDFA on iOS) | Ad targeting and measurement |
| IP address | Geographic targeting and fraud prevention |
| Device model, OS version, screen size | Ad rendering and compatibility |
| App version and ad interaction data | Performance measurement and fraud detection |
| Coarse location (derived from IP) | Regional ad targeting |

This data is collected and processed by **Google LLC** under its own privacy policy. We do not receive, store, or process this data ourselves.

**Personalized vs. Non-Personalized Ads:** Depending on the consent you provide through the in-app consent dialog (powered by the Google UMP SDK), ads may be personalized (using your advertising ID for targeting) or non-personalized (contextual only, using no behavioral data).

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

The App displays banner advertisements provided by Google AdMob. The purpose of advertising is to sustain the App's ongoing development while keeping it free for users. Google uses the data described in Section 2.2 to select and display relevant advertisements.

We do not use your locally stored app data (shopping lists, items, markets) for advertising purposes.

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

### 5.2 Advertising Data (Google AdMob)

The App integrates **Google AdMob**, which collects and processes the data described in Section 2.2. This constitutes a sharing of technical and usage data with a third party for advertising purposes. Google acts as an independent data controller for this data.

- **Google's Privacy Policy:** [https://policies.google.com/privacy](https://policies.google.com/privacy)
- **Google's Advertising Policy:** [https://policies.google.com/technologies/ads](https://policies.google.com/technologies/ads)
- **Opt-out of personalized ads (Google):** [https://adssettings.google.com](https://adssettings.google.com)

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
| **google\_mobile\_ads** | **Banner advertising (Google AdMob + UMP SDK)** | **See Section 2.2 and Section 7** |

> **Note on Google Fonts:** The `google_fonts` package may request font files from Google's servers on first use if fonts are not yet cached on the device. No personal data is included in these requests.

---

## 7. Advertising, Consent, and Regional Privacy Rights

### 7.1 In-App Consent Dialog (UMP SDK)

The App uses the **Google User Messaging Platform (UMP SDK)** to manage advertising consent. Depending on your location:

- **European Union / European Economic Area (EEA):** You will be presented with a consent dialog before any personalized ads are shown. You may choose to accept personalized ads, accept only non-personalized ads, or reject ads entirely. You can change your choice at any time through your device settings.
- **United Kingdom:** Same consent flow as EEA users applies.
- **Other regions:** Non-personalized or contextual ads may be displayed without a consent prompt, subject to applicable local law.

### 7.2 European Union — GDPR

For users located in the EU/EEA, the following applies under the **General Data Protection Regulation (GDPR)**:

- **Data Controller for app data:** You are the sole data controller for all data stored locally in the App. We (Leankar.dev) do not process your personal data.
- **Data Controller for advertising data:** Google LLC, 1600 Amphitheatre Parkway, Mountain View, CA 94043, USA.
- **Lawful basis for advertising:** Consent (Article 6(1)(a) GDPR). Advertising data is only processed for personalization if you explicitly consent through the UMP dialog.
- **Data transfers outside the EU:** Google may transfer advertising data to servers in the United States and other countries. Google relies on Standard Contractual Clauses (SCCs) for such transfers.
- **Your rights:** You have the right to access, rectify, erase, restrict processing of, and port your data, as well as the right to object to profiling based on advertising data. Exercise these rights directly with Google via [myaccount.google.com](https://myaccount.google.com) or by contacting us at leankar.dev@gmail.com.
- **Right to withdraw consent:** You may withdraw advertising consent at any time. This does not affect the lawfulness of processing based on consent before its withdrawal.
- **Lodge a complaint:** You have the right to lodge a complaint with your local Data Protection Authority (DPA).

### 7.3 Brazil — LGPD

For users located in Brazil, the following applies under the **Lei Geral de Proteção de Dados (LGPD — Lei nº 13.709/2018)**:

- **Controller for app data:** You are the sole controller for all data stored locally in the App. We (Leankar.dev) process no personal data on our end.
- **Operator for advertising data:** Google LLC acts as an operator (operador) processing advertising data as described in Section 2.2.
- **Legal basis for advertising:** Legitimate interest (interest legítimo) for non-personalized advertising; consent (consentimento) for personalized advertising. You may be presented with a consent dialog depending on your region settings.
- **Your rights under LGPD:** Confirmation of processing, access, correction, anonymization or deletion of unnecessary data, portability, information about third parties with whom data is shared, right to revoke consent, and right to file a complaint with the ANPD (Autoridade Nacional de Proteção de Dados).
- **Data Processing Report (RIPD):** If required, you may request information about our data processing activities by contacting leankar.dev@gmail.com.
- **DPO Contact:** leankar.dev@gmail.com

### 7.4 United States — CCPA / US State Privacy Laws

For users located in California and other US states with applicable privacy laws:

- **Personal Information collected by AdMob:** The advertising data described in Section 2.2 (advertising ID, IP address, device information, interaction data) is collected by Google and may constitute "personal information" under the California Consumer Privacy Act (CCPA) / California Privacy Rights Act (CPRA).
- **Sharing for cross-context behavioral advertising:** The integration of Google AdMob may be considered "sharing" personal information for cross-context behavioral advertising under CCPA. You have the right to opt out of this sharing.
- **Opt-out options:**
  - Reset or limit your Advertising ID: *Android:* Settings → Privacy → Ads → Delete advertising ID (Android 12+) or Opt out of Ads Personalization. *iOS:* Settings → Privacy & Security → Tracking → disable tracking.
  - Opt out via Google: [https://adssettings.google.com](https://adssettings.google.com)
- **Your CCPA rights:** Right to know what personal information is collected, right to delete, right to opt out of sale/sharing, right to non-discrimination.
- **Do Not Sell or Share My Personal Information:** We do not sell personal information. To opt out of sharing with Google for advertising, use the controls listed above.
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
| **Ad Preferences** | Manage via Google Ad Settings at [adssettings.google.com](https://adssettings.google.com) |
| **Advertising ID** | Reset or delete via device settings (see Section 7.4) |

For rights requests related to advertising data collected by Google, contact Google directly or use the controls described in Section 7.

---

## 9. Children's Privacy

The App does not knowingly collect personal information from children under the age of 13 (or the applicable minimum age in your jurisdiction). The App contains no social features, no accounts linked to real identities, and no online communication.

The advertising displayed through Google AdMob is configured for a **general audience**. If you believe a child is using the App, we recommend using parental control features available on your device to limit ad-related data collection.

If you are a parent or guardian and have concerns, please contact us at leankar.dev@gmail.com.

---

## 10. Data Retention

### 10.1 Your App Data

Data is stored on your device for as long as the App is installed and you choose to retain it. There is no automated expiration of data. When you uninstall the App, the operating system removes all application data, including the SQLite database and all secure storage entries.

### 10.2 Advertising Data (Google)

Advertising data collected by Google is retained according to Google's data retention policies. For details, see [Google's data retention information](https://policies.google.com/technologies/retention).

---

## 11. Internet and Device Permissions

The App requests the following permissions:

| Permission | Required For |
|-----------|-------------|
| `INTERNET` | Loading and displaying advertisements via Google AdMob |
| `ACCESS_NETWORK_STATE` (optional) | Checking connectivity for improved ad performance |

The App does **not** request access to:

- Location (GPS or network-based)
- Camera or microphone
- Contacts or calendar
- External storage
- Device identifiers beyond those accessed by AdMob

All user data is accessed only within the App's own sandboxed application directory on the device.

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
