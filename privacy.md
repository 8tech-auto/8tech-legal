# Privacy Policy — NAIPS Briefing Tool

**Effective date:** 1 May 2026  
**Developer:** 8TECH PTY LTD  
**Contact:** support@8tech.au

---

## 1. Overview

NAIPS Briefing Tool ("the App") is developed and published by 8TECH PTY LTD (ABN to be inserted) ("we", "us", "our"). This Privacy Policy explains how we handle information in connection with your use of the App.

We are committed to protecting your privacy in accordance with the *Privacy Act 1988* (Cth) and the Australian Privacy Principles (APPs).

---

## 2. What information the App collects

### 2.1 NAIPS credentials

The App requires your Airservices Australia NAIPS username and password to retrieve aviation weather briefings on your behalf.

- These credentials are stored **exclusively on your device** using Android's EncryptedSharedPreferences, which applies AES-256-GCM encryption backed by the Android Keystore.
- They are transmitted only to `https://www.airservicesaustralia.com` for the purpose of authenticating with the NAIPS Internet Service and retrieving briefing data.
- They are never transmitted to 8TECH PTY LTD or any other third party.
- They are never written to disk in plaintext, logged, or included in any diagnostic output.

### 2.2 Aviation data

Route configurations, airport alternate minima, NOTAM acknowledgements, weather data, and all other operational data entered into or retrieved by the App are stored **exclusively on your device** in a local SQLite database.

This data is never transmitted to 8TECH PTY LTD or any third party.

### 2.3 Diagnostic logs

The App maintains an in-memory and on-device debug log for the purpose of troubleshooting. This log contains:

- ICAO codes of airports in your routes
- HTTP response codes and timing from NAIPS requests
- Application lifecycle events

This log is stored only on your device. It is never transmitted automatically. You may choose to share it manually via the in-app "Share Log" function when seeking technical support. Sharing is always at your discretion.

In release (production) builds, verbose diagnostic entries are suppressed. Only significant events and errors are retained.

### 2.4 Information we do not collect

The App does not collect, transmit, or process:

- Device identifiers (IMEI, advertising ID, etc.)
- Location data
- Usage analytics or behavioural data
- Crash reports *(see Section 3)*
- Any information from users other than the account holder

---

## 3. Crash reporting

The App uses **Firebase Crashlytics**, a crash reporting service provided by Google LLC, in release builds.

When a crash or significant error occurs, Crashlytics automatically collects and transmits the following to Google's servers:

- Stack trace of the crash or error
- Device model, Android version, and App version
- A randomly generated installation identifier (not linked to your Google account or personal identity)
- Log entries recorded at WARNING or ERROR level by the App's internal logger immediately before the event (these contain ICAO codes and HTTP status codes; they do not contain your NAIPS credentials or personal information)

Crashlytics is **disabled in debug builds** and **enabled only in release builds**. Data collected by Crashlytics is used solely for diagnosing and fixing application defects.

Firebase Crashlytics is subject to Google's Privacy Policy: [policies.google.com/privacy](https://policies.google.com/privacy)

If you do not wish to participate in crash reporting, you may contact us at support@8tech.au to request opt-out guidance.

---

## 4. Third-party services

The App communicates with one external service:

| Service | Provider | Purpose | Privacy Policy |
|---------|----------|---------|----------------|
| NAIPS Internet Service | Airservices Australia | Retrieval of aviation weather briefings, NOTAMs, and ATIS | [airservicesaustralia.com/privacy](https://www.airservicesaustralia.com/privacy) |
| Firebase Crashlytics | Google LLC | Automated crash and error reporting (release builds only) | [policies.google.com/privacy](https://policies.google.com/privacy) |

Your use of NAIPS is subject to Airservices Australia's own terms of service and privacy policy. 8TECH PTY LTD is not affiliated with Airservices Australia.

---

## 5. Data storage and security

All data processed by the App is stored locally on your device and is subject to your device's security controls (screen lock, encryption, etc.).

We apply the following security measures within the App:

- NAIPS credentials encrypted at rest using AES-256-GCM via Android Keystore
- All communication with NAIPS conducted over HTTPS (TLS 1.2 minimum as enforced by Android's network security policy)
- No user data transmitted to our servers

We do not operate servers that store your data. We cannot access your data remotely.

---

## 6. Data retention and deletion

All data stored by the App resides on your device. You can delete all App data at any time by:

- Uninstalling the App (removes all data including the local database and encrypted credentials)
- Using Android's **Settings → Apps → NAIPS Briefing Tool → Storage → Clear Data** function

The App automatically prunes historical briefing records older than 7 days to manage local storage.

We do not retain any copies of your data because we never receive it.

---

## 7. Children

The App is intended for use by licenced aviation professionals and student pilots. It is not directed at children under the age of 18. We do not knowingly collect information from children.

---

## 8. Changes to this policy

We will update this Privacy Policy when material changes are made to how the App handles data. The updated policy will be published at this URL with a revised effective date. Continued use of the App after the effective date of an updated policy constitutes acceptance of the changes.

For significant changes — such as the introduction of crash reporting or analytics — we will provide in-app notice before the change takes effect.

---

## 9. Contact

For privacy-related enquiries or complaints, please contact:

**8TECH PTY LTD**  
Email: support@8tech.au

If you are not satisfied with our response, you may lodge a complaint with the Office of the Australian Information Commissioner (OAIC) at [oaic.gov.au](https://www.oaic.gov.au).

---

## 10. Disclaimer

NAIPS Briefing Tool is an **unofficial companion application** and is not affiliated with, endorsed by, or certified by Airservices Australia, CASA, or any aviation authority. It is not a certified navigation system or safety-critical application. Always obtain official pre-flight briefings through authorised channels before flight.

---

*Last updated: 1 May 2026*
