# Zap Pay

GenZ-style UPI payments app prototype. Single-file web app (`www/index.html`) wrapped as an Android app with Capacitor.

Demo data only. No real money moves. Real UPI needs a licensed PSP / bank partner.

## Features
Wallet, quick pay, scan and pay (simulated), amount keypad, UPI PIN step, confetti success, activity chart,
scratch-card rewards, theme (auto/dark/light), 5 accent colours, background presets + custom photo + dim slider,
6 app icons, sound effects, haptics, hide balance, reduce motion.

## Run in a browser
Open `www/index.html`.

## Build the APK (needs Node 18+, JDK 17, Android SDK)
```
npm install
npx cap add android
npx cap sync android
cd android && ./gradlew assembleDebug
```
APK: `android/app/build/outputs/apk/debug/app-debug.apk`

## Build the APK with no setup (GitHub)
Push this folder to a GitHub repo. Open Actions > Build APK > Run workflow.
Download `zap-pay-debug-apk` from the run's Artifacts. Unzip, then install the APK on your phone.

## Real launcher icon switching
The in-app icon picker changes the in-app logo and tab icon. To switch the real launcher icon on Android,
add `<activity-alias>` entries in AndroidManifest.xml and enable one at a time with PackageManager
(via a small Capacitor plugin).
