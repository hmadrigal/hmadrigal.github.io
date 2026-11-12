---
title: Privacy Policy for PaperVault
date: 2026-11-11 14:00:00 -0600
permalink: /projects/papervault/privacy-policy/
tags:
  - PaperVault
  - Privacy Policy
---

# Privacy Policy for PaperVault

**Effective Date:** November 11, 2026
**Developer:** [[Mad Herb Lab Dev]]
**Contact Email:** [madherblab@gmail.com](mailto:madherblab@gmail.com)

## 1. Overview
[[PaperVault]] ("we," "our," or "us") is built with a strict privacy-first, offline-first architecture. This Privacy Policy explains how [[PaperVault]] handles your scanned documents, local security features (passwords and biometrics), device permissions, and optional third-party integrations.

**We do not operate backend servers, we do not create user accounts, and we do not collect, store, or sell your personal data, passwords, biometric data, or scanned documents.**

---

## 2. Information Collection and Local Processing

### 2.1 Scanned Documents, Images, and OCR Text
- **100% On-Device Processing:** All image capturing, perspective correction, visual filtering, and Optical Character Recognition (OCR) are performed locally on your Android device using on-device libraries (such as OpenCV and Google ML Kit on-device SDKs).
- **Local Storage Only:** Your raw captures, processed images, thumbnails, extracted text, folders, and document tags are stored exclusively within your device's internal storage. We have zero access to your files.

### 2.2 Password Protection & Biometric Authentication
[[PaperVault]] allows you to protect individual documents and folders using a local password and, on supported devices, biometric authentication:
- **Local Password Security:** Passwords and encryption keys used to lock documents or folders are hashed/encrypted and stored strictly on your local device using Android security frameworks (such as the Android Keystore system). Because we do not have servers or accounts, **we cannot view, reset, or recover forgotten passwords.**
- **Biometric Data (`USE_BIOMETRIC`):** When you enable biometric unlock for password-protected folders, [[PaperVault]] relies exclusively on the native Android `BiometricPrompt` system API. **The app never accesses, collects, stores, or transmits your fingerprint, facial geometry, or any raw biometric data.** The Android operating system simply notifies the app whether authentication succeeded or failed.

### 2.3 Device Permissions
To function as a 2D document scanner, [[PaperVault]] requests access to the following device permissions:
- **Camera (`android.permission.CAMERA`):** Used solely to capture images of physical documents when you initiate a scan. Camera frames are never streamed or transmitted externally.
- **Biometric Hardware (`android.permission.USE_BIOMETRIC`):** Used solely to authenticate your identity locally when unlocking password-protected folders or documents.
- **Storage / Media Access:** Used only when you explicitly choose to import existing images from your device gallery or export/share generated PDFs and images to other apps on your device.

### 2.4 Hardware-Backed Credential Storage
If you choose to configure optional third-party API keys (see Section 3), [[PaperVault]] uses the hardware-backed **Android Keystore system (AES-256-GCM encryption)** to encrypt and store your credentials locally on your device. We do not collect hardware identifiers (such as IMEI or Advertising IDs) to track you.

---

## 3. Optional Third-Party AI Services (Bring Your Own Key)

By default, [[PaperVault]] operates completely offline and transmits no data over the internet.

However, [[PaperVault]] includes an optional **Bring-Your-Own-Key (BYOK)** feature that allows you to connect your own personal API keys from third-party AI providers (such as Google Gemini, OpenAI, or Anthropic) for advanced document analysis or summarization:
- **User-Initiated Transmission:** Data (such as extracted OCR text or compressed document images) is transmitted **only** when you manually trigger an AI analysis action and have configured your own API key.
- **Direct Connection:** Requests are sent directly from your device to your chosen AI provider's servers using your personal credentials. We do not intercept, log, or proxy these requests.
- **Third-Party Policies:** When using this optional feature, your data is subject to the privacy policy and data usage terms of your chosen AI provider:
  - [Google AI / Gemini Privacy Policy](https://policies.google.com/privacy)
  - [OpenAI Privacy Policy](https://openai.com/policies/privacy-policy)
  - [Anthropic Privacy Policy](https://www.anthropic.com/privacy)

---

## 4. Data Sharing and International Compliance (GDPR & LGPD)
- **No Commercial Sharing:** We do not sell, rent, trade, or share any user data with data brokers, advertisers, or analytics companies. [[PaperVault]] contains no third-party advertising SDKs.
- **Regional Privacy Rights (EU/UK GDPR & Brazil LGPD):** [[PaperVault]] is available in English, Spanish, Portuguese, French, Italian, and German. Because all core features operate 100% locally on your device without collecting personal data or transferring it to developer-controlled servers, you retain full physical control, access, portability, and deletion rights over your data at all times directly on your device.
- **User-Initiated Sharing:** When you use the "Share" or "Export" features, your device's native Android Share Sheet transfers the selected PDF or image files directly to the external app or recipient you choose.

---

## 5. Data Retention and Deletion
Because all data resides locally on your device:
- **Retention:** Your scanned documents, locked folders, extracted text, and encrypted API keys remain on your device for as long as you keep them in the app.
- **Deletion:** You can delete individual pages, documents, locked folders, or saved API keys within the app at any time. Uninstalling [[PaperVault]] from your Android device permanently deletes all locally stored application data, databases, and cached files (unless backed up by your device's system-level Android Auto Backup settings).

---

## 6. Children's Privacy
[[PaperVault]] is a general-purpose utility application and is not directed at children under the age of 13 (or 16 in applicable European jurisdictions). We do not knowingly collect personal information from children.

---

## 7. Changes to This Privacy Policy
We may update this Privacy Policy from time to time to reflect changes in app functionality or legal requirements. Any updates will be posted on this page with an updated "Effective Date."

---

## 8. Contact Us
If you have any questions, concerns, or requests regarding this Privacy Policy or how [[PaperVault]] handles data, please contact us at:

- **Developer:** [[Mad Herb Lab Dev]]
- **Email:** [madherblab@gmail.com](mailto:madherblab@gmail.com)