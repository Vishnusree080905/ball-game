# Ball Battle Studio: Android APK project

Needs: Node 18+, JDK 17, and the Android SDK (install Android Studio, which includes it).

## Build a debug APK (installable on any phone)
    npm install
    npx cap add android
    npx capacitor-assets generate --android
    npx cap sync android
    cd android
    ./gradlew assembleDebug        # Windows: gradlew.bat assembleDebug

Your APK: android/app/build/outputs/apk/debug/app-debug.apk
Copy it to your phone, open it, and allow "Install unknown apps" when asked.

## Or use Android Studio
    npx cap open android
then Build > Build Bundle(s) / APK(s) > Build APK(s).
For a Play Store release use Build > Generate Signed Bundle / APK.

## Notes
- The app is in www/index.html. After editing it, run: npx cap sync android
- Save video writes the recording to cache and opens the Android share sheet so you can save it to Files or Drive.
- Fonts load from Google Fonts when online and fall back to the system font offline.
- Icon and splash source images are in resources/.
