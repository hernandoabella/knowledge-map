# 📱 Mobile

> Building for the pocket computer everyone carries.

---

## 🌐 Cross-Platform

| Tech | What it's for | Trade-offs |
|------|--------------|------------|
| **React Native** | iOS + Android with React — bridge to native APIs | Near-native perf, large community |
| **Flutter** | Dart + Skia rendering engine — compiled to native | Best UI consistency, own render engine |
| **Expo** | React Native toolchain with OTA updates and managed builds | Simplest setup, some native limitations |
| **Ionic** | Web tech in native wrapper — Capacitor for native APIs | Web devs, rapid prototyping |
| **Capacitor** | Native runtime for web apps — successor to Cordova | Better than Cordova, some perf cost |

---

## 🍎 Native iOS

| Tech | What it's for |
|------|--------------|
| **Swift** | Apple's modern language — safe, expressive, interops with ObjC |
| **SwiftUI** | Declarative UI framework for all Apple platforms |
| **UIKit** | Imperative, mature UI framework — more control, larger existing codebases |
| **Combine** | Reactive framework for async event processing on Apple platforms |
| **Swift Concurrency** | async/await + actors — structured concurrency in Swift 5.5+ |
| **Xcode** | IDE, simulator, Instruments profiler, TestFlight, App Store Connect |
| **Core Data** | Apple's ORM/persistence framework |
| **CloudKit** | Apple's iCloud database for syncing across devices |

---

## 🤖 Native Android

| Tech | What it's for |
|------|--------------|
| **Kotlin** | Modern, concise Android language with coroutines |
| **Jetpack Compose** | Declarative UI for Android — modern standard |
| **Android Views** | XML layouts + ViewBinding — legacy but widely deployed |
| **Kotlin Coroutines** | Structured concurrency in Kotlin |
| **Jetpack libraries** | Room (ORM), Navigation, WorkManager, DataStore, ViewModel, LiveData |
| **Android Studio** | IDE with profiler, emulator, APK analyzer |
| **Gradle** | Build system for Android projects |

---

## 📲 Mobile Engineering Concepts

| Concept | What it means |
|---------|--------------|
| **Offline-first** | Local-first storage + sync strategies — graceful degradation on poor connectivity |
| **Push notifications** | FCM (Android), APNs (iOS), Expo Push API |
| **Deep linking** | Open app to specific screen from URL, notification, or widget |
| **Universal links / App links** | Verified domain-to-app link associations |
| **Code push / OTA** | Ship JS bundle updates without app store review (React Native/Expo) |
| **Biometrics** | Face ID, Touch ID, Android BiometricPrompt API |
| **App store review** | Apple/Google guidelines, binary validation, typical review timelines |
| **Performance profiling** | Instruments (iOS), Android Profiler — CPU, memory, network, rendering |
| **Battery optimization** | Background processing limits, Doze mode, background fetch |
| **App signing** | Keystore (Android), provisioning profiles (iOS) — required for distribution |

---

## 🗺️ Suggested Roadmap

```
JavaScript fundamentals
    → React Native + Expo (fastest path to both platforms)
    → Native device APIs (camera, GPS, notifications)
    → Navigation (React Navigation)
    → State management (Zustand or Redux Toolkit)
    → Offline storage (MMKV, SQLite, AsyncStorage)
    → App store deployment
    → Native modules (when JS bridge isn't enough)
    → Optional: native Swift or Kotlin for platform-specific work
```
