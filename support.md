---
layout: page
title: Layer8Focus Support
permalink: /support/
---

# Layer8Focus Support & Documentation

Welcome to the official support hub for **Layer8Focus** — the tactical zero-knowledge focus and interval timer built for Apple devices (iOS, iPadOS, watchOS, macOS, and visionOS) and Android.

**Developer:** PEBCAK Consulting LLC  
**Primary Support Contact:** [layer8focus@pebcakconsulting.com](mailto:layer8focus@pebcakconsulting.com)  
**General Inquiries:** [sonofagl1tch@pebcakconsulting.com](mailto:sonofagl1tch@pebcakconsulting.com)  
**Response Time:** Within 24–48 business hours.

---

## Quick Navigation
- [Getting Started](#getting-started)
- [Apple Watch Companion Setup](#apple-watch-companion-setup)
- [Encrypted Backups & Zero-Knowledge Architecture](#encrypted-backups--zero-knowledge-architecture)
- [Cross-Device Synchronization](#cross-device-synchronization)
- [In-App Purchases & Restoring Purchases](#in-app-purchases--restoring-purchases)
- [Apple Health & Mindful Minutes](#apple-health--mindful-minutes)
- [Frequently Asked Questions (FAQ)](#frequently-asked-questions-faq)
- [Contact Support & Bug Reports](#contact-support--bug-reports)

---

## Getting Started

1. **Launch & Focus:** Open Layer8Focus to immediately view the tactical HUD timer. No account creation or login is required.
2. **Select a Preset:** Use the bottom preset selector to switch between default routines (*Kernel Focus*, *Deep Compilation*, *Chore Routine*, *System Defrag*) or configure your own custom durations.
3. **Start Timer:** Tap **START** / **INITIALIZE** to begin your focus block.
4. **Ambient Audio:** Tap the audio frequency icon to activate procedural soundscapes (Server Room Hum, Mechanical Keystrokes, Terminal Brown/White Noise).
5. **Session Telemetry:** Completed sessions automatically log to the **Logs** tab with daily, weekly, and preset breakdown charts.

---

## Apple Watch Companion Setup

Layer8Focus includes a dedicated companion app for Apple Watch (watchOS 10+):

- **Automatic Mirroring:** Once installed on your paired iPhone, the Apple Watch app automatically mirrors your active timer countdown, cycle count, and phase via WatchConnectivity.
- **Wrist Haptics:** Distinct haptic taps notify you when focus sessions and break intervals conclude, keeping you focused without looking at your phone.
- **Installation Troubleshooting:**
  1. Open the **Watch** app on your paired iPhone.
  2. On the **My Watch** tab, scroll down to **Available Apps**.
  3. Locate **Layer8Focus** and tap **Install** (or verify that *Show App on Apple Watch* is toggled ON).
  4. Ensure both your iPhone and Apple Watch have Bluetooth and Wi-Fi enabled.

---

## Encrypted Backups & Zero-Knowledge Architecture

Layer8Focus operates under strict **Zero-Knowledge** principles:
- **Local-First Encryption:** All session history, presets, and preferences are stored exclusively on your device using hardware-accelerated **AES-256-GCM**.
- **Password-Protected Export (.l8bak):** Navigate to **Settings -> Data Privacy Architecture -> Export Password-Protected Archive**. Enter a passphrase to generate an encrypted backup file.
- **Importing Archives:** You can restore your data onto any device by tapping **Import Archive** and providing your master passphrase.
- **Data Deletion:** To permanently delete all on-device telemetry, navigate to **Settings -> Data Privacy Architecture -> Erase All Data**.

---

## Cross-Device Synchronization

- **Optional Cloud Sync:** You can use Layer8Focus 100% offline in Local Mode. If you wish to sync presets, streak history, and badges across your Apple devices, you can optionally authenticate with **Sign in with Apple** or **Google Account** in **Settings -> Account Identity & Encrypted Sync**.
- **Privacy:** Sync payloads remain end-to-end encrypted; neither PEBCAK Consulting LLC nor third parties have access to your telemetry.

---

## In-App Purchases & Restoring Purchases

Layer8Focus offers an optional one-time **Pro Operator Lifetime License** (unlocks unlimited custom presets, exports audit reports, and permanently removes all sponsor banners):

- **Restoring Purchases:** If you reinstall the app or set up a new Apple device:
  1. Open Layer8Focus on your device.
  2. Go to **Settings** -> tap the **UPGRADE** banner or **Upgrade Operator License**.
  3. Tap **Restore Purchases** at the bottom of the screen.
  4. Sign in with the Apple ID used for the original purchase. StoreKit will restore your Pro Operator status immediately with zero charges.
- **Family Sharing:** In-App Purchases are linked to your Apple ID and follow standard App Store licensing terms.

---

## Apple Health & Mindful Minutes

- **Permission:** When prompted, allow Layer8Focus to write Mindful Sessions to Apple Health.
- **How It Works:** Every completed focus interval automatically logs as Mindful Minutes on your device, contributing to your daily mindfulness goals in Apple Health.
- **Managing Permissions:** You can enable or revoke access anytime in iOS **Settings -> Privacy & Security -> Health -> Layer8Focus**.

---

## Frequently Asked Questions (FAQ)

#### Why does the countdown not drift when the app is in the background?
Layer8Focus utilizes a monotonic hardware clock differential engine. Rather than relying on inaccurate UI tick timers, it calculates exact elapsed time against monotonic system timestamps, ensuring zero drift even if your device enters low-power mode or returns from hours in the background.

#### Does Layer8Focus track my location or sell my data?
**Never.** Layer8Focus does not track your location, does not collect personal identity information, and does not sell or broker telemetry to third parties. Review our complete [Privacy Policy]({{ "/privacy/" | relative_url }}) for details.

#### Which devices and OS versions are supported?
- **iOS:** iOS 17.0 or later (iPhone)
- **iPadOS:** iPadOS 17.0 or later (iPad)
- **watchOS:** watchOS 10.0 or later (Apple Watch)
- **macOS:** macOS 14.0 Sonoma or later (Mac)
- **visionOS:** visionOS 1.0 or later (Apple Vision Pro)

---

## Contact Support & Bug Reports

Need assistance, found a bug, or have a feature suggestion? We are here to help.

- **Email Support:** [layer8focus@pebcakconsulting.com](mailto:layer8focus@pebcakconsulting.com)
- **Developer Inquiries:** [sonofagl1tch@pebcakconsulting.com](mailto:sonofagl1tch@pebcakconsulting.com)
- **When submitting a bug report, please include:**
  1. Device model (e.g., iPhone 16 Pro, Apple Watch Ultra 2, iPad Pro 13").
  2. OS version (e.g., iOS 18.0, watchOS 11.0).
  3. App version and build number (visible at the bottom of Settings).
  4. Steps to reproduce the issue.

---

[Back to Home]({{ "/" | relative_url }}) &bull; [Privacy Policy]({{ "/privacy/" | relative_url }}) &bull; [Terms of Service]({{ "/terms/" | relative_url }})
