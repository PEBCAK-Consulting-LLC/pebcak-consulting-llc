---
layout: page
title: Privacy Policy
permalink: /privacy/
---

# PEBCAK Consulting LLC - Privacy Policy

**Effective Date:** October 1, 2026  
**Last Updated:** October 1, 2026  
**Applications Covered:** Layer8Focus (Android, Wear OS, iOS, watchOS, macOS, visionOS)  
**Publisher:** PEBCAK Consulting LLC  
**Contact Email:** [layer8focus@pebcakconsulting.com](mailto:layer8focus@pebcakconsulting.com) | [sonofagl1tch@pebcakconsulting.com](mailto:sonofagl1tch@pebcakconsulting.com)  

---

## 1. Executive Summary & Zero-Knowledge Architecture

PEBCAK Consulting LLC ("we", "us", or "our") is dedicated to protecting your fundamental right to digital privacy. As cybersecurity professionals, we design software based on the principle of **Zero-Knowledge Architecture** and **Local-First Processing**:

- **No Remote Account Required:** You can use all core interval timer features without creating an account or providing any personal information.
- **Hardware-Backed Encryption at Rest:** All timer logs, intervals, streaks, and preferences are stored exclusively on your local device and encrypted using hardware-accelerated **AES-256-GCM**.
- **No Data Brokering or Selling:** We do not sell, rent, monetize, or disclose your personal information or productivity telemetry to third parties or data brokers.
- **Zero-Knowledge Cloud Backups:** If you choose to back up your data to Google Drive or iCloud, your data is encrypted locally on your device with your master passphrase using **AES-256-GCM** and **PBKDF2** (100,000 hashing rounds) *before* transmission. Neither PEBCAK Consulting LLC nor cloud storage providers possess the key to decrypt your vaults.

---

## 2. Information We Process and How We Use It

### A. Focus Session Telemetry (Local Only)
- **Data Points:** Interval durations, completed work and break sessions, custom routine configurations, streaks, and achievement badges.
- **Storage:** Stored locally in an encrypted database (Room with Android Keystore on Android; SwiftData/UserDefaults with Keychain on Apple platforms).
- **Access:** This telemetry remains exclusively on your device.

### B. Google Drive Cloud Vault Backup (Optional - Android)
- **Data Points:** Encrypted application state archive (`.l8bak`).
- **Google API Scopes:** Layer8Focus utilizes restricted app data scopes (`drive.appdata` / `drive.file`) to read and write backup archives created strictly by the application.
- **Security:** Files are encrypted with user-defined passphrases via AES-256-GCM. Unencrypted data is never transmitted.
- **Google API Limited Use Disclosure:** Layer8Focus's use and transfer to any other app of information received from Google APIs will adhere to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements.

### C. Health & Wellness Data Integration (Optional)
- **Platforms:** Android Health Connect and Apple HealthKit.
- **Data Points:** Completed focus and meditation blocks written as **Mindful Sessions** (`WRITE_MINDFULNESS`) and **Exercise Sessions** (`WRITE_EXERCISE`).
- **Policy Compliance:** 
  - Access requires your explicit runtime system authorization.
  - Health data is written exclusively to your personal on-device health store to consolidate wellness metrics.
  - We **never** read your unrelated medical records or third-party health metrics.
  - We **never** transfer, share, or sell health data to advertising platforms, data brokers, or information resellers.

### D. Wear OS & Apple Watch Synchronization
- **Data Points:** Active countdown status, remaining seconds, interval phase, and current routine presets.
- **Transport:** Exchanged directly between your phone and paired watch via local Bluetooth / Wi-Fi peer connections using the official Google Play Services Wearable Data Layer (`Wearable.DataClient`) or Apple WatchConnectivity framework.
- **Security:** Data is ephemeral and stays within your personal device ecosystem.

### E. Advertising & Rewarded Access Passes (Android)
- **Partner:** Google AdMob / Google Play Services.
- **Usage:** Layer8Focus includes optional rewarded video advertisements (e.g. watch an optional 15-30 second transmission to earn 1 hour or 6 hours of ad-free deep work).
- **Data Collected by AdMob:** Device advertising identifier (Google Advertising ID / GAID), coarse location based on IP address, and standard interaction telemetry to serve and measure non-personalized or personalized advertisements.
- **User Control:** You may reset your advertising ID or opt out of personalized ads at any time via **Android Settings -> Google -> Ads**. You can also permanently disable all advertisements with the optional Pro Operator upgrade.

### F. Application Diagnostics and Crash Telemetry
- **Tool:** Firebase Crashlytics.
- **Data Collected:** Anonymous stack traces, operating system versions, device hardware models, and failure timestamps.
- **Privacy Assurance:** Crash reports never contain user session notes, passphrases, or health metrics.

---

## 3. Data Retention and Deletion Rights

You have complete sovereignty over your data:

- **Local Data Erasure:** You can purge all application state, presets, and streak history instantly by navigating to **Settings -> Data Privacy -> Erase All Data**, or by clearing application cache and storage in your device settings.
- **Cloud Backup Removal:** You can delete your encrypted backup archives at any time directly through the Layer8Focus Cloud Vault manager or by removing the application data from your Google Drive / iCloud Drive settings.
- **Account Disconnection:** You can revoke Google Sign-In authorizations granted to Layer8Focus at any time via your [Google Account Security Permissions](https://myaccount.google.com/permissions).

---

## 4. Security Architecture

As security practitioners, we enforce multi-layered defense mechanisms:
- **AES-256-GCM** hardware-backed encryption keys generated and retained inside the secure hardware enclave / Android Keystore.
- **PBKDF2-HMAC-SHA256** with 100,000 hashing rounds and unique cryptographically secure salts for passphrase-based cloud vaults.
- **Strict HTTPS / TLS 1.3** transport security for all external network endpoints.
- **Cleartext Traffic Disabled:** Cleartext HTTP traffic is blocked via network security configurations (`android:usesCleartextTraffic="false"`).

---

## 5. Children's Privacy

Layer8Focus is designed for general audiences, professionals, and students. We do not knowingly collect personal identifiable information from children under 13 years of age (or under 16 in certain jurisdictions). If you become aware that a child has provided us with personal information, please notify us and we will promptly delete it.

---

## 6. International Compliance (GDPR & CCPA/CPRA)

If you reside in the European Economic Area (EEA), United Kingdom, or California:
- **Right to Access & Portability:** You can export all your session data and presets into portable JSON or password-protected archives (`.l8bak`) directly on your device.
- **Right to Erasure:** You can execute complete local and cloud deletion without requiring developer intervention.
- **No Sale of Personal Data:** We do not sell your personal data.

---

## 7. Updates to This Policy

We may update this Privacy Policy from time to time to reflect operational, legal, or regulatory updates. Any changes will be posted to this page with an updated "Last Updated" timestamp.

---

## 8. Contact Information

If you have questions, inquiries, or regulatory requests concerning this policy or our data security architecture, please contact:

**PEBCAK Consulting LLC**  
Attn: Privacy & Security Operations  
Email: [layer8focus@pebcakconsulting.com](mailto:layer8focus@pebcakconsulting.com)  
Website: [https://pebcakconsulting.com](https://pebcakconsulting.com)  
