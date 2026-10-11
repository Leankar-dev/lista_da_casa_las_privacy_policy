---
layout: default
title: Privacy Policy — Lista da Casa
description: Privacy Policy for the Lista da Casa app (Android). Last updated October 11, 2026.
lang: en
---

# Privacy Policy

**Lista da Casa** — Gestão de Compras Domésticas  
**Developer:** Leankar.dev  
**Contact:** leankar.dev@gmail.com  
**Website:** [https://leankar.dev](https://leankar.dev)  
**Last updated:** October 11, 2026

---

## 1. Introduction

This Privacy Policy describes how **Lista da Casa** ("the App", "we", "our") handles information when you use our mobile application available on Google Play.

The App is designed with a **local-first** architecture and has **no user accounts, no sign-in, and no PIN**: all user-generated data (shopping lists, items, markets, purchase history, and preferences) is stored exclusively on your device and is never transmitted to our servers. However, the App displays banner and interstitial advertisements through **Unity LevelPlay**, a third-party mobile ad mediation platform operated by Unity, which may serve ads from its own demand and from partner advertising networks. As a result, certain device and usage information is collected and processed by LevelPlay and its advertising partners for advertising purposes, as described in this policy. The App also uses the **Google Play In-App Update API** to check for and install app updates, which involves communication with Google Play services.

---

## 2. Information We Collect

### 2.1 Information You Provide Directly

All data entered in the App is stored **exclusively on your device**. This includes:

| Data                                                                           | Purpose                            | Storage               |
| ------------------------------------------------------------------------------ | ---------------------------------- | --------------------- |
| Shopping list names (optional)                                                 | Organize your lists                | Local SQLite database |
| Item names, quantities, prices, categories, observations, and purchased status | Manage purchases                   | Local SQLite database |
| Market / store names and addresses (address optional)                          | Track where you shop               | Local SQLite database |
| Purchase history (finalized lists with date, market, items, and totals)        | Spending history and charts        | Local SQLite database |
| Language preference                                                            | App localization                   | Device secure storage |
| Theme preference (light, dark, or system)                                      | App appearance                     | Device secure storage |
| Ads consent choice (accepted or declined)                                      | Remember your choice (Section 7.1) | Device secure storage |

The App does not ask for your name, email address, password, or any other account information.

This data is never transmitted to us or to any third party by the App. Note that the Android system may include the local database in device backups that you control (see Section 4.1).

### 2.2 Information Collected by Unity LevelPlay (Advertising SDK)

The App uses the **Unity LevelPlay SDK** (a mediation platform that requests ads from LevelPlay's own demand and, when configured, from partner advertising networks) to display banner advertisements (shown on selected screens) and interstitial advertisements (shown occasionally, at most once every 30 minutes, after you complete a purchase in a shopping list). When ads are loaded, the LevelPlay SDK may automatically collect the following data (as disclosed by Unity in LevelPlay's Google Play data safety questionnaire and in Unity's Game Player and App User Privacy Policy):

| Data                                                                    | Purpose                                                                        |
| ----------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| Device or other identifiers, including the Google Advertising ID (GAID) | Analytics; fraud prevention, security and compliance; advertising or marketing |
| IP address and the approximate location derived from it                 | Analytics; fraud prevention, security and compliance; advertising or marketing |
| Ad interaction data (app activity, such as interactions with ads)       | Analytics; fraud prevention, security and compliance; advertising or marketing |
| Diagnostics and performance data                                        | Analytics; fraud prevention, security and compliance; advertising or marketing |
| Device information (such as device type and operating system)           | Ad delivery, measurement, and fraud detection                                  |

According to Unity's disclosure, this collection is required for the SDK to operate (it is not optional or ephemeral), the data is encrypted in transit, and users can request deletion of their data. Device or other identifiers, approximate location, and ad-interaction data may be shared with advertising partners. Unity's disclosure covers data collected by LevelPlay (ironSource) itself: **partner advertising networks** that LevelPlay may call can collect additional data under their own privacy policies. The App currently includes no third-party network adapters.

The App does **not** request the device's Location permission, so LevelPlay cannot access GPS/precise location through the App — only the approximate location derived from the IP address described above.

This data is collected and processed by **Unity (LevelPlay)** and its advertising partners under their own privacy policies (see Section 5.2). We do not receive, store, or process this data ourselves.

**Ads Consent:** On first launch, the App shows an in-app dialog asking whether you agree to see ads. If you decline, the App does not initialize the LevelPlay SDK and does not request any ads, so the App does not trigger the data collection described in this section. If you accept, ads are shown and the data above may be collected by LevelPlay and its advertising partners. You can review or change your choice at any time from Settings → Privacy & Ads. This mechanism does not implement the IAB Transparency & Consent Framework (TCF) or per-vendor granular consent — it is a simple accept/decline choice covering all ad-related data collection by LevelPlay and its partners.

### 2.3 Information We Do NOT Collect

We (Leankar.dev) do **not** collect any of the following:

- Real name, email address, phone number, or any identity document
- Account credentials (the App has no accounts, usernames, passwords, or PIN)
- Location data or GPS coordinates
- Usage analytics or crash reports
- Contacts, photos, camera, or microphone data
- Payment or financial information
- Biometric data

### 2.4 Network Connectivity Check

After you accept ads (Section 7.1), and before the advertising SDK is initialized, the App performs a DNS lookup of a public domain name (`google.com`) to confirm that the device has internet access. The App does not send any app data or identifiers in this lookup; like any DNS lookup, it is visible to your network or DNS provider. This check does not occur if you decline ads.

---

## 3. How We Use Your Information

### 3.1 App Functionality

All user-provided data is used **solely within the App** to deliver its features:

- Display and manage your shopping lists
- Track item prices and purchase status
- Present spending history and analytics charts
- Maintain your language, theme, and ads-consent preferences across sessions

### 3.2 Advertising

The App displays banner and interstitial advertisements provided by Unity LevelPlay and its advertising partners. The purpose of advertising is to sustain the App's ongoing development while keeping it free for users. LevelPlay and its partners use the data described in Section 2.2 to select and display relevant advertisements.

We do not use your locally stored app data (shopping lists, items, markets) for advertising purposes.

### 3.3 App Updates

The App uses the **Google Play In-App Update API** to check whether a newer version is available and, depending on the update's priority, to prompt a flexible or immediate update. This feature communicates with Google Play services on your device and is governed by Google Play's own terms and privacy practices. No app data (shopping lists, items, markets) is shared through this feature.

---

## 4. Data Storage and Security

### 4.1 Where Your Data is Stored

| Storage Layer  | Contents                                                  | Technology                                                                     |
| -------------- | --------------------------------------------------------- | ------------------------------------------------------------------------------ |
| Secure storage | Language preference, theme preference, ads consent choice | Android Keystore-backed encryption (`flutter_secure_storage`)                  |
| Local database | Shopping lists, items, markets, purchase history          | SQLite (via Drift ORM), file: `lista_da_casa.db`, in the App's private storage |

**All user-provided data resides on your device.** We operate no servers, no accounts, and no cloud sync, and we have no access to your data.

**Android device backup:** the App allows Android's automatic backup. If you have Google backup enabled on your device, the local database (`lista_da_casa.db`) may be included in the backup stored in your Google account and in device-to-device transfers. The secure-storage file (preferences and ads-consent choice) is excluded from both. Backups are created and managed by Android and Google, not by us, and you can turn them off or delete them in your device's Settings → Google → Backup.

### 4.2 Security Measures

- **Local-only processing:** the App has no backend. Your lists, items, markets, and history are never sent to us.
- **Secure storage for preferences:** your preferences and ads-consent choice are kept in platform-native secure storage (Android Keystore-backed encryption), not in plain files, and are excluded from Android backups.
- **Screen capture protection:** on Android, the App sets the `FLAG_SECURE` window flag at startup, which prevents screenshots, screen recordings, and App Switcher previews from capturing App content.
- **Third-party traffic is limited to the SDKs described in this policy:** the advertising SDK (only after you accept ads) and Google Play's in-app update service.

### 4.3 Limitations

The local SQLite database itself is not encrypted at the file level, and the App has no PIN or app-level lock. Physical access to an unlocked or rooted device could expose the database contents. We recommend keeping your device protected with a screen lock.

---

## 5. Data Sharing and Disclosure

### 5.1 Your App Data

We do **not** share your locally stored data (shopping lists, items, markets, purchase history) with anyone. The App does not transmit this data; the only copy outside the App is any Android backup that you control (Section 4.1).

### 5.2 Advertising Data (Unity LevelPlay)

The App integrates the **Unity LevelPlay** advertising SDK, which collects and processes the data described in Section 2.2 and may share it with advertising partners. This constitutes a sharing of technical and usage data with third parties for advertising purposes. Unity's Game Player and App User Privacy Policy lists Unity LevelPlay among its mediation products and ironSource among its affiliates, and states that **Unity Technologies S.F.** is the organization responsible for collecting, using, and disclosing this data. Unity's affiliates and third-party advertising partners may receive it.

- **Unity's Game Player and App User Privacy Policy:** [https://unity.com/legal/game-player-and-app-user-privacy-policy](https://unity.com/legal/game-player-and-app-user-privacy-policy)
- **LevelPlay's documentation on US state privacy laws (the "do not sell/share" signal the App sends when you decline ads):** [https://docs.unity.com/en-us/grow/levelplay/platform/legal-resources/ironsource-us-state-privacy-laws](https://docs.unity.com/en-us/grow/levelplay/platform/legal-resources/ironsource-us-state-privacy-laws)
- **Unity's "Do Not Sell or Share My Personal Information" page:** [https://unity.com/legal/do-not-sell-my-personal-information](https://unity.com/legal/do-not-sell-my-personal-information)
- **Privacy requests (Unity's privacy team, the general privacy contact in Unity's policy):** dpo@unity3d.com

Unity's published materials do not describe a separate request process for LevelPlay. Requests about data collected through LevelPlay should therefore be sent to Unity's privacy team at dpo@unity3d.com. The "Do Not Sell or Share My Personal Information" page above describes opt-out controls for Unity Ads and does not name LevelPlay. For users who opt out of sale or sharing under US state privacy laws, LevelPlay states that it uses their personal information only as a service provider and only for permitted purposes such as fraud prevention and frequency capping.

### 5.3 App Update Data (Google Play)

The App's in-app update feature (Section 3.3) communicates with Google Play services to determine whether an update is available. This is governed by Google's own privacy policy: [https://policies.google.com/privacy](https://policies.google.com/privacy).

No other data is sold, rented, licensed, or shared with any party.

---

## 6. Third-Party SDKs and Libraries

The App uses the following open-source and third-party libraries:

| Library                                         | Purpose                                                                                               | Data Collection                                                                              |
| ----------------------------------------------- | ----------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| Drift / sqlite3 / path\_provider                | Local database and its storage location                                                               | None — local only                                                                            |
| flutter\_secure\_storage                        | Platform-native secure storage for preferences and the ads-consent choice                             | None — local only                                                                            |
| google\_fonts                                   | Font rendering. The Poppins font files are bundled with the App and runtime font download is disabled | None — the App makes no font requests                                                        |
| package\_info\_plus                             | Reads the App's own version and build number for display                                              | None — local only                                                                            |
| fl\_chart                                       | Charts and graphs                                                                                     | None                                                                                         |
| flutter\_riverpod, equatable, clock, uuid, intl | State management, value equality, time, local identifiers, and formatting                             | None                                                                                         |
| flutter\_neumorphic\_plus, cupertino\_icons     | UI design system and icons                                                                            | None                                                                                         |
| url\_launcher                                   | Opens the developer's website in the device's browser when you tap it                                 | None collected by the App itself; the website visit is governed by that site's own practices |
| **unity\_levelplay\_mediation**                 | **Banner and interstitial advertising (Unity LevelPlay)**                                             | **See Section 2.2 and Section 7**                                                            |
| **in\_app\_update**                             | **Google Play in-app update checks and prompts (Android)**                                            | **See Section 3.3 and Section 5.3**                                                          |

> **Note on fonts:** the App does not download fonts from Google or any other server; all fonts are packaged inside the App.

---

## 7. Advertising, Consent, and Regional Privacy Rights

### 7.1 Advertising Consent

Before any ad is loaded, the App shows an in-app consent dialog asking you to accept or decline ads. Your choice is stored on your device and used as follows:

- **If you decline:** the App never initializes the LevelPlay SDK on that device and requests no ads, so no banner or interstitial ads are shown and the App does not trigger the data collection described in Section 2.2.
- **If you accept:** ads are shown and LevelPlay and its advertising partners may collect the data described in Section 2.2. The App also informs the SDK of your choice through its privacy settings (GDPR consent and CCPA "do not sell" flags).
- **Changing your choice:** you can review or change your decision at any time from Settings → Privacy & Ads. Declining after previously accepting stops future ad loads and impressions on that device, though data already sent to LevelPlay and its partners while ads were enabled cannot be recalled by the App, and the SDK may keep its previous state until the App is restarted.

This is a binary accept/decline mechanism, not an IAB Transparency & Consent Framework (TCF) implementation with per-vendor granularity. In addition:

- You can ask Unity to stop collecting, sharing, or using your data for targeted advertising at any time through the opt-out options described in Section 5.2.
- If you are located in the EEA, UK, or another region with similar requirements, you may exercise the rights described in Sections 7.2–7.4 directly with Unity (LevelPlay) or through your device's privacy settings.

### 7.2 European Union — GDPR

For users located in the EU/EEA, the following applies under the **General Data Protection Regulation (GDPR)**:

- **Data Controller for app data:** You are the sole data controller for all data stored locally in the App. We (Leankar.dev) do not process your personal data.
- **Data Controller for advertising data:** Unity Technologies S.F., 116 New Montgomery Street, Suite 200, San Francisco, CA 94105, USA (identified in Unity's Game Player and App User Privacy Policy as the organization responsible for the collection), and the advertising partners that receive the data. Data protection contact: dpo@unity3d.com.
- **Lawful basis for advertising:** Consent (Article 6(1)(a) GDPR), collected through the in-app dialog described in Section 7.1. Ads are only shown, and LevelPlay is only initialized, after you accept. Unity states that it relies on consent for personalized advertising and on legitimate interests for contextual advertising and service optimization.
- **Data transfers outside the EU:** Unity states that personal data may be stored and processed in any country where it has facilities (including the United States and Israel) and that it relies on safeguards such as adequacy decisions and Standard Contractual Clauses. Refer to Unity's privacy policy (Section 5.2) for details.
- **Your rights:** You have the right to access, rectify, erase, restrict processing of, and port your data, as well as the right to object to profiling based on advertising data. Exercise these rights directly with Unity (LevelPlay) through its privacy team at dpo@unity3d.com (Section 5.2), or by contacting us at leankar.dev@gmail.com.
- **Right to object:** You may object to processing based on legitimate interest at any time using the channels above.
- **Lodge a complaint:** You have the right to lodge a complaint with your local Data Protection Authority (DPA).

### 7.3 Brazil — LGPD

For users located in Brazil, the following applies under the **Lei Geral de Proteção de Dados (LGPD — Lei nº 13.709/2018)**:

- **Controller for app data:** You are the sole controller for all data stored locally in the App. We (Leankar.dev) process no personal data on our end.
- **Advertising data:** Unity Technologies S.F. is the organization responsible for collecting the advertising data described in Section 2.2 (see Section 5.2); the App's developer does not receive or process this data.
- **Legal basis for advertising:** Consentimento (consent), collected through the in-app dialog described in Section 7.1. Ads are only shown, and LevelPlay is only initialized, after you accept.
- **Your rights under LGPD:** Confirmation of processing, access, correction, anonymization or deletion of unnecessary data, portability, information about third parties with whom data is shared, right to revoke consent, and right to file a complaint with the ANPD (Autoridade Nacional de Proteção de Dados).
- **Data Processing Report (RIPD):** If required, you may request information about our data processing activities by contacting leankar.dev@gmail.com.
- **DPO Contact:** leankar.dev@gmail.com

### 7.4 United States — CCPA / US State Privacy Laws

For users located in California and other US states with applicable privacy laws:

- **Personal Information collected by LevelPlay and its partners:** The advertising data described in Section 2.2 (advertising ID, IP address, device information, interaction data) is collected by LevelPlay and its advertising partners and may constitute "personal information" under the California Consumer Privacy Act (CCPA) / California Privacy Rights Act (CPRA).
- **Sharing for cross-context behavioral advertising:** The integration of the LevelPlay SDK may be considered "sharing" personal information for cross-context behavioral advertising under CCPA. You have the right to opt out of this sharing.
- **Opt-out options:**
  - Reset or limit your Advertising ID: Settings → Privacy → Ads → Delete advertising ID (Android 12+) or Opt out of Ads Personalization.
  - Opt out directly with Unity: [https://unity.com/legal/do-not-sell-my-personal-information](https://unity.com/legal/do-not-sell-my-personal-information) (the page describes opt-out for Unity Ads; for data collected through LevelPlay, send your request to dpo@unity3d.com).
  - In the App: declining ads (Settings → Privacy & Ads) stops ads and sets the SDK's CCPA "do not sell" flag. LevelPlay forwards this signal to the advertising networks that support it, and each network handles it under its own policies.
- **Your CCPA rights:** Right to know what personal information is collected, right to delete, right to opt out of sale/sharing, right to non-discrimination.
- **Do Not Sell or Share My Personal Information:** We do not sell personal information. To opt out of sharing with LevelPlay and its advertising partners, use the controls listed above.
- **Contact:** leankar.dev@gmail.com for any privacy requests.

---

## 8. Your Rights and Data Control

Because all user-provided data is local to your device, you have full and immediate control:

| Right              | How to Exercise                                                                                                                                                                                                     |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Access**         | All your data is visible directly within the App                                                                                                                                                                    |
| **Correction**     | Edit any list, item, or market from within the App                                                                                                                                                                  |
| **Deletion**       | Delete individual items, shopping lists, purchase history entries, and markets within the App; to erase everything, clear the App's data in Android Settings → Apps → Lista da Casa → Storage, or uninstall the App |
| **Portability**    | The App has no export function; your data stays in the App's private storage and, if Android backup is enabled, in your own Google backup (Section 4.1)                                                             |
| **Withdraw**       | Uninstall the App — all local data is permanently deleted from the device                                                                                                                                           |
| **Ad Preferences** | Decline ads in Settings → Privacy & Ads, or opt out directly with Unity (see Section 5.2)                                                                                                                           |
| **Advertising ID** | Reset or delete via device settings (see Section 7.4)                                                                                                                                                               |

<a id="data-deletion"></a>

### 8.1 How to Request Data Deletion

**Lista da Casa**, developed by **Leankar.dev**, stores your data only on your device, so you can delete it yourself:

**1. Delete data inside the App**

Delete individual shopping items, shopping lists, purchase history entries, and markets directly from the corresponding screens of the App.

**2. Clear the App's data (erase everything at once)**

1. Open your device's **Settings**.
2. Go to **Apps → Lista da Casa → Storage**.
3. Tap **Clear data** and confirm.

This immediately and permanently erases, from your device:

- All shopping lists, items, markets, and purchase history (local SQLite database)
- Your language, theme, and ads-consent preferences (secure device storage); the App will ask for your ads consent again the next time it opens

**3. Uninstall the App**

Uninstalling **Lista da Casa** from your device deletes the entire application, including the local database and all secure storage entries, with no data retained on our side — we never had a copy, since everything is local-first (Section 4.1).

**4. Device backups**

If Google backup was enabled on your device, a copy of the local database may exist in your Google account backup (Section 4.1). Deleting data in the App or uninstalling does not remove that backup; you can manage or delete it in your device's Settings → Google → Backup.

**5. Data held by Unity LevelPlay and its advertising partners (advertising SDK)**

If you accepted ads (Section 7.1), the LevelPlay SDK may have already sent your Advertising ID and IP address to LevelPlay's servers (and to partner advertising networks) before you delete the App. None of the options above can recall data already sent to them. To request its deletion, contact Unity's privacy team at dpo@unity3d.com (see its [Game Player and App User Privacy Policy](https://unity.com/legal/game-player-and-app-user-privacy-policy)); Unity's published disclosure states that users can request deletion of data collected by the LevelPlay SDK.

LevelPlay and its partners retain this data according to their own retention policies (see Section 10.2); we do not control or have access to it.

**What is never deleted because it was never collected:** we do not operate any servers or accounts, so there is no copy of your shopping data anywhere outside your device and any Android backup you control.

For rights requests related to advertising data collected by LevelPlay and its partners, contact Unity's privacy team (dpo@unity3d.com) or use the controls described in Section 7.

---

## 9. Children's Privacy

The App does not knowingly collect personal information from children under the age of 13 (or the applicable minimum age in your jurisdiction). The App contains no social features, no accounts linked to real identities, and no online communication.

The advertising displayed through Unity LevelPlay is configured for a **general audience** (the App does not enable child-directed treatment in the SDK). If you believe a child is using the App, we recommend using parental control features available on your device to limit ad-related data collection.

If you are a parent or guardian and have concerns, please contact us at leankar.dev@gmail.com.

---

## 10. Data Retention

### 10.1 Your App Data

Data is stored on your device for as long as the App is installed and you choose to retain it. There is no automated expiration of data. When you uninstall the App, the operating system removes all application data, including the SQLite database and all secure storage entries. Any Android backup stored in your Google account is retained according to Google's backup settings (Section 4.1).

### 10.2 Advertising Data (Unity LevelPlay)

Unity's Game Player and App User Privacy Policy states that Unity retains personal data for as long as is necessary or permitted, without a fixed retention period for advertising data; partner advertising networks apply their own retention policies. For details, see [Unity's Game Player and App User Privacy Policy](https://unity.com/legal/game-player-and-app-user-privacy-policy).

---

## 11. Internet and Device Permissions

The App requests the following permissions:

| Permission                                | Required For                                                                                                     |
| ----------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| `INTERNET`                                | Loading and displaying advertisements (Unity LevelPlay) and checking for app updates (Google Play In-App Update) |
| `ACCESS_NETWORK_STATE`                    | Letting the advertising SDK check whether a network connection is available before loading ads                   |
| `com.google.android.gms.permission.AD_ID` | Allowing the advertising SDK to read the Advertising ID described in Section 2.2 (Android 13+)                   |

The advertising SDK's own manifest additionally declares `ACCESS_ADSERVICES_ATTRIBUTION`, the Android permission required to use the platform's ad-services attribution reporting APIs (Android Privacy Sandbox).

The App does **not** request access to:

- Location (GPS or network-based)
- Camera or microphone
- Contacts or calendar
- External storage

All user-provided data (lists, items, markets, purchase history, preferences) is accessed only within the App's own sandboxed application directory on the device. Android libraries may also declare internal, app-private permissions (for example `<package>.DYNAMIC_RECEIVER_NOT_EXPORTED_PERMISSION`) that are not shared with other apps and do not give access to your data. Note that, independent of the permissions listed above, the Unity LevelPlay advertising SDK and its partners may automatically access certain device-level and network-level information (such as the Advertising ID, IP address, and technical device data) as described in Section 2.2, as is standard for mobile advertising SDKs.

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
