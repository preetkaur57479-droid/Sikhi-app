# Gurbani & Sikhi — Android starter project (updated)

This project is an original Android app starter with a warm, dark-and-gold interface inspired by common Sikh spiritual reading apps. It does not copy ChetHari's proprietary assets or exact screens.

## Improvements in this version
- Reader screen with previous/next Bani navigation.
- Gurmukhi search normalization using Unicode NFC, case normalization, whitespace cleanup, and removal of invisible formatting marks.
- Persistent local favourites for Bani entries and demo search records.
- Adjustable reader font size, saved locally.
- Local Paath progress and Naam Simran count.
- Android back button returns through the app's screens before exiting.
- WebView settings tightened for a bundled, offline-first app; external HTTPS links open outside the app.
- A content schema is provided for future verified Bani data.

## Important content status
This build intentionally does **not** claim to contain complete Nitnem, Sri Guru Granth Sahib Ji, translations, audio, or live Hukamnama. The Bani list is navigation only. Search results are a tiny demo index and are labelled as demo content. The reader clearly states when verified text is unavailable.

Before adding religious content, verify it against an authoritative source, record the source and ang/section reference, confirm licensing/permission for the text and any audio, and review Gurmukhi spelling and formatting. Do not publish unverified text as Gurbani.

## Build an APK
1. Install the current stable Android Studio on a computer.
2. Extract this ZIP.
3. Open the `Gurbani_Sikhi_Android` folder in Android Studio.
4. Allow Gradle sync. Install Android SDK Platform 35 if Android Studio asks.
5. Select **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
6. Find the APK at `app/build/outputs/apk/debug/app-debug.apk`.
7. Transfer it to your Android phone and install it. Android may ask you to allow installation from that file manager.

## Technical details
- Java Android Activity with a local WebView UI.
- Minimum Android version: API 23 (Android 6.0).
- Application ID: `com.gurbanisikhi.app`.
- No account, analytics, or backend is used.
- App data is stored locally in WebView local storage.

## Still to do
- Add a verified, licensed Gurbani content pack and full-text indexed search.
- Implement reader page/ang navigation against the chosen dataset.
- Connect an authorized Hukamnama source with freshness indicators.
- Add licensed audio playback and offline downloads.
- Test on physical Android devices and different screen sizes.
- Generate and sign a release APK.


## Version 3: scripture and audio discovery foundations
- Added separate library entries for Sri Dasam Granth Sahib, Sri Sarbloh Granth and Sri Gur Pratap Suraj Granth.
- Added source/edition reference panels with direct external links and explicit source-quality/rights notes.
- Added an audio search interface with Kirtan, Katha and Bani filters. The catalogue is intentionally empty until permitted audio is indexed.
- Added a structured source register and import guides for separately attributed meanings/teekas and audio metadata.
- No complete scripture texts, translations, audio tracks or machine-generated meanings were copied into the project.

## Build an APK from a phone using GitHub Actions

This project includes a cloud build workflow at `.github/workflows/build-apk.yml`.

1. Create a GitHub account and create a **public or private repository**.
2. Upload the contents of this project folder to the repository (keep the `.github/workflows` folder).
3. Open the repository's **Actions** tab.
4. Select **Build Gurbani and Sikhi APK**, then tap **Run workflow**. (A push to the `main` branch also starts a build.)
5. When the run finishes successfully, open that run and download the `Gurbani-Sikhi-debug-apk` artifact.
6. Extract the downloaded artifact to get the debug APK. Android may ask you to allow installation from the browser or file manager before installing it.

This workflow builds a **debug APK**, not a Play Store release APK. A release build needs a securely managed signing key. The app's scripture, translations, and audio content remain subject to the source and permission limitations described elsewhere in this README and the content guides.
