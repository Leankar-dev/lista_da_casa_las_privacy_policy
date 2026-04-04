---
layout: default
title: Privacy Policy — Lista da Casa
description: Privacy Policy for the Lista da Casa app (Android/iOS). Last updated April 4, 2026.
lang: en
---

# Privacy Policy

**Lista da Casa** — Gestão de Compras Domésticas  
**Developer:** Leankar.dev  
**Contact:** leankar.dev@gmail.com  
**Website:** [https://leankar.dev](https://leankar.dev)  
**Last updated:** April 4, 2026

---

## 1. Introduction

This Privacy Policy describes how **Lista da Casa** ("the App", "we", "our") handles information when you use our mobile application available on Google Play.

We are committed to protecting your privacy. The App is designed with a **local-first, offline-only** architecture: **no personal data is ever transmitted to external servers**, and we do not collect, store, or share any information outside your device.

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

### 2.2 Information We Do NOT Collect

We do **not** collect any of the following:

- Real name, email address, phone number, or any identity document
- Location data or GPS coordinates
- Device identifiers (IMEI, advertising ID, IP address)
- Usage analytics or crash reports
- Contacts, photos, camera, or microphone data
- Payment or financial information
- Biometric data
- Browsing or behavioral data of any kind

---

## 3. How We Use Your Information

All data is used **solely within the App** to deliver its features:

- Display and manage your shopping lists
- Track item prices and purchase status
- Present spending history and analytics charts
- Maintain your language preference across sessions

We do not use your data for advertising, profiling, marketing, or any purpose beyond the core App functionality.

---

## 4. Data Storage and Security

### 4.1 Where Data is Stored

| Storage Layer | Contents | Technology |
|---------------|----------|-----------|
| Secure storage | PIN (HMAC-SHA256 hashed with cryptographic salt), username, preferences | Android Keystore / iOS Keychain |
| Local database | Shopping lists, items, markets, history | SQLite (via Drift ORM), file: `lista_da_casa.db` |

**All data resides entirely on your device.** There is no cloud sync, no remote backup, and no network communication of any kind.

### 4.2 Security Measures

- **PIN hashing:** Your PIN is never stored in plain text. It is processed with HMAC-SHA256 using a unique cryptographic salt per device.
- **Secure storage:** Credentials are stored using platform-native secure storage (Android Keystore / iOS Keychain), not in plain files or shared preferences.
- **Brute-force protection:** After repeated failed login attempts, the App enforces progressive lockouts (30 seconds → 5 minutes → 1 hour).
- **Session timeout:** If the App is placed in the background for more than 15 minutes, you will be automatically logged out and must re-authenticate.
- **Timing-attack resistance:** PIN comparison uses constant-time evaluation to prevent information leakage.
- **Screen capture protection:** On Android, the App sets the `FLAG_SECURE` window flag at startup, which prevents screenshots, screen recordings, and App Switcher previews from capturing any App content. This ensures that sensitive data (shopping lists, prices, PINs) cannot be captured by other apps or system-level tools.

### 4.3 Limitations

The local SQLite database itself is not encrypted at the file level. Physical access to a rooted or jailbroken device could expose the database contents. We recommend keeping your device secure and using a strong PIN.

---

## 5. Data Sharing and Disclosure

**We do not share your data with anyone.** Because all data remains on your device:

- No data is transmitted to us or any third party
- No data is sold, rented, or licensed to anyone
- No data is used for advertising or analytics platforms
- No data is shared with government entities (we have no data to provide)

---

## 6. Third-Party SDKs and Libraries

The App uses only open-source libraries for UI rendering, local data persistence, cryptography, and localization. **None of these libraries collect or transmit personal data.**

Key dependencies include:

| Library | Purpose |
|---------|---------|
| Drift / SQLite | Local database |
| flutter\_secure\_storage | Platform-native secure storage |
| crypto | PIN hashing |
| google\_fonts | Font rendering (may cache fonts locally) |
| fl\_chart | Charts and graphs |
| flutter\_riverpod | State management |
| flutter\_neumorphic\_plus | UI design system |

> **Note on Google Fonts:** The `google_fonts` package may request font files from Google's servers on first use if fonts are not yet cached on the device. No personal data is included in these requests. If you are concerned, the App operates normally with system fonts once the initial rendering occurs.

---

## 7. Children's Privacy

The App does not knowingly collect personal information from children under the age of 13 (or the applicable minimum age in your jurisdiction). The App contains no social features, no accounts linked to real identities, and no online communication.

If you are a parent or guardian and believe your child has provided information through the App, please note that all data is local to the device and can be deleted at any time (see Section 8).

---

## 8. Your Rights and Data Control

Because all data is local to your device, you have full and immediate control:

| Right | How to Exercise |
|-------|----------------|
| **Access** | All your data is visible directly within the App |
| **Correction** | Edit any list, item, or market from within the App |
| **Deletion** | Delete individual items, lists, or markets within the App; use "Delete Account" in Settings to erase all data |
| **Portability** | The SQLite database file (`lista_da_casa.db`) can be accessed and exported from the application data directory |
| **Withdraw** | Uninstall the App — all data is permanently deleted from the device |

For GDPR, LGPD (Brazil), or CCPA purposes: since we do not process personal data on our servers, you are the sole data controller for all information within the App.

---

## 9. Data Retention

Data is stored on your device for as long as the App is installed and you choose to retain it. There is no automated expiration of data.

When you uninstall the App, the operating system removes all application data, including the SQLite database and all secure storage entries.

---

## 10. Internet and Device Permissions

The App requests **no sensitive permissions**. It does not request access to:

- Internet / network communication
- Location (GPS or network-based)
- Camera or microphone
- Contacts or calendar
- External storage
- Device identifiers

The App only accesses its own sandboxed application directory on the device.

---

## 11. Changes to This Policy

We may update this Privacy Policy to reflect changes in the App's features or applicable law. When we do:

- The "Last updated" date at the top of this page will be revised
- If the change is material, we will note it in the App's store listing release notes

Continued use of the App after an update constitutes acceptance of the revised policy. We encourage you to review this page periodically.

---

## 12. Contact Us

If you have any questions or concerns about this Privacy Policy or the App's data practices, please contact us:

**Email:** leankar.dev@gmail.com  
**Website:** [https://leankar.dev](https://leankar.dev)  
**App:** Lista da Casa — available on Google Play  

We will respond to all inquiries within 30 days.

---

*© 2026 LeanKar. All rights reserved.*
