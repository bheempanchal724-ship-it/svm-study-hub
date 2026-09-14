# 🚀 SVM Study Hub - Setup Instructions

## ✅ What's Included

Your repository now has:
- ✅ Complete Android project structure
- ✅ GitHub Actions workflow for automated APK/AAB builds
- ✅ Debug & Release build configurations
- ✅ Material Design theme setup
- ✅ ProGuard code obfuscation for release builds

---

## 📋 Prerequisites

Before you can build, ensure you have:

1. **Android SDK** (API 34)
2. **Java JDK 11+**
3. **Gradle 8.0+**

---

## 🔧 Local Build (On Your Computer)

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/bheempanchal724-ship-it/svm-study-hub.git
cd svm-study-hub
```

### 2️⃣ Build Debug APK
```bash
./gradlew assembleDebug
```
📁 Output: `app/build/outputs/apk/debug/app-debug.apk`

### 3️⃣ Build Release APK (Unsigned)
```bash
./gradlew assembleRelease
```
📁 Output: `app/build/outputs/apk/release/app-release-unsigned.apk`

### 4️⃣ Build Android App Bundle (AAB)
```bash
./gradlew bundleRelease
```
📁 Output: `app/build/outputs/bundle/release/app-release.aab`

---

## ☁️ Automatic Build with GitHub Actions

### How It Works
Every time you:
- 🔄 Push to `main` or `develop` branch
- 📝 Create a Pull Request
- ▶️ Manually trigger workflow

GitHub automatically builds your APK and AAB files!

### 📥 Download Artifacts

1. Go to **Actions** tab in your repository
2. Click on the latest workflow run
3. Scroll to **Artifacts** section
4. Download:
   - `debug-apk` — Test builds
   - `release-apk-unsigned` — Release builds (requires signing)
   - `release-bundle` — Google Play Store submission

---

## 🔐 Sign Release APK (For Distribution)

### Generate Signing Key
```bash
keytool -genkey -v -keystore app.jks -keyalg RSA -keysize 2048 -validity 10000 -alias my-key-alias
```

### Sign Release APK
```bash
jarsigner -verbose -sigalg SHA256withRSA -digestalg SHA-256 \
  -keystore app.jks app-release-unsigned.apk my-key-alias
```

### Align APK
```bash
zipalign -v 4 app-release-unsigned.apk app-release-aligned.apk
mv app-release-aligned.apk app-release.apk
```

---

## 🏪 Google Play Store Publishing

1. **Upload AAB** to Google Play Console
2. Set up signing and version info
3. Submit for review

---

## 📱 Install on Device/Emulator

### Debug APK
```bash
adb install app/build/outputs/apk/debug/app-debug.apk
```

### Release APK (signed)
```bash
adb install app-release.apk
```

---

## 🆘 Troubleshooting

### Gradle Build Fails
```bash
./gradlew clean build --stacktrace
```

### Out of Memory
```bash
export JAVA_OPTS="-Xmx4096m"
./gradlew build
```

### Clear Cache
```bash
./gradlew cleanBuildCache
```

---

## 📚 Next Steps

1. **Add Features** — Modify `app/src/main/java/`
2. **Update UI** — Edit `app/src/main/res/layout/`
3. **Push Code** — Automatic builds trigger on push
4. **Download APK** — Grab from GitHub Actions Artifacts

---

## 🎯 What's Next?

Would you like help with:
- ✨ Adding Material Design screens
- 🔐 Signing configuration for Play Store
- 📊 Adding SVM algorithms/logic
- 🧪 Setting up unit tests
- 📈 Analytics integration

---

**Happy Building! 🚀**

