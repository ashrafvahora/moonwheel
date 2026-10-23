# Zodiac Wheel – Android app (transit alerts)

## Get the APK (no Android Studio needed)
1. Create a free GitHub account and a new empty repository.
2. Upload ALL files from this folder (keep the `.github/workflows/build-apk.yml` path).
3. Open the repo → **Actions** → **Build Android APK** → **Run workflow** (it also runs on every push).
4. After ~5 minutes open the finished run → **Artifacts** → download **zodiac-wheel-apk** → unzip → `app-debug.apk`.
5. Copy the APK to your phone, tap it, allow "Install unknown apps" when asked.

## Or build locally
Needs Node 18+, JDK 17, Android Studio.
```
npm install
npx cap add android
(add the 4 permissions from the workflow into android/app/src/main/AndroidManifest.xml)
npx cap sync android
npx cap open android      # Build > Build APK(s)
```

## Using alerts
Open the app → **Transit alerts** card → turn on, choose triggers (sub-lord / nakshatra / sign / bias),
planets, lead minutes and "Market hours only". Allow notifications when Android asks.
Alerts are scheduled on the phone for the next 1–7 days, so open the app every few days to refresh.
If alerts arrive late, set the app's battery usage to "Unrestricted" and allow "Alarms & reminders".
