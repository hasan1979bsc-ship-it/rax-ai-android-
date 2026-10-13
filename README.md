# RAX AI - Android app

A native Android wrapper (WebView) around your `index.html`. The HTML lives in
`app/src/main/assets/index.html` - replace it any time and rebuild.

## Build option A: Android Studio
1. Install Android Studio (Koala or newer).
2. File > Open > select this folder, wait for Gradle sync.
3. Build > Build APK(s), or press Run with a phone/emulator connected.
   APK: app/build/outputs/apk/debug/app-debug.apk

## Build option B: GitHub (no PC tools needed)
1. Create a new GitHub repo and upload this whole folder (keep the .github folder).
2. Open the Actions tab > "Build APK" and wait ~3 minutes.
3. Download the RAX-AI-apk artifact, unzip it, and install app-debug.apk on your
   phone (allow "Install unknown apps").

## Notes
- Needs Android 10+ (minSdk 29).
- Chats and settings persist (localStorage + IndexedDB).
- Exports and image downloads are saved to the Downloads folder.
- Voice input (Web Speech API) is not supported by Android WebView, so that button won't work.
- localhost endpoints (Ollama / LM Studio) point at the phone itself; use your computer's LAN IP instead.
