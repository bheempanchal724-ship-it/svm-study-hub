# 📚 SVM Study Hub

**An interactive Android application for learning Support Vector Machines (SVM)**

[![Build APK & AAB](https://github.com/bheempanchal724-ship-it/svm-study-hub/actions/workflows/build_apk.yml/badge.svg)](https://github.com/bheempanchal724-ship-it/svm-study-hub/actions/workflows/build_apk.yml)

---

## 🎯 Features

- 📱 Modern Material Design UI
- 🚀 Optimized for Android 5.0+ (API 24)
- 📦 Automated APK/AAB builds via GitHub Actions
- 🔐 Ready for Google Play Store
- ⚡ Fast & lightweight

---

## 🛠️ Quick Start

### Clone & Build
```bash
git clone https://github.com/bheempanchal724-ship-it/svm-study-hub.git
cd svm-study-hub
./gradlew assembleDebug
```

### Run on Device
```bash
adb install app/build/outputs/apk/debug/app-debug.apk
```

---

## 📦 Build Outputs

| Build Type | Location | Use Case |
|-----------|----------|----------|
| **Debug APK** | `app/build/outputs/apk/debug/` | Testing & development |
| **Release APK** | `app/build/outputs/apk/release/` | Direct distribution |
| **AAB Bundle** | `app/build/outputs/bundle/release/` | Google Play Store |

---

## ☁️ GitHub Actions Automation

Builds automatically trigger on:
- ✅ Push to `main` or `develop`
- ✅ Pull requests to `main`
- ✅ Manual trigger via workflow_dispatch

**Download builds:** Actions → Latest Workflow → Artifacts

---

## 📖 Documentation

- [Setup Instructions](SETUP_INSTRUCTIONS.md)
- [Android Developer Docs](https://developer.android.com)
- [Material Design](https://material.io)

---

## 📄 License

Apache License 2.0 — See [LICENSE](LICENSE) file

---

## 👤 Author

**bheempanchal724-ship-it**

---

## 🤝 Contributing

Contributions welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request

---

**Built with ❤️ using Android & Kotlin**
