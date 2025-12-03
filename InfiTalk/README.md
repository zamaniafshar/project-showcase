# 🎧 Real-Time Voice Translator (Flutter)

A **production Flutter app** that enables **two-way, real-time voice translation** in a chat-style interface.  
Designed for **quick, natural conversations** — press & hold to speak, **auto-transcribe → translate → speak back**, while keeping a **persistent, searchable** chat history.

> ⚠️ This repository contains **screenshots + high-level description** only.  
> **Source code is not included** to respect client confidentiality.

---

## ✨ Features

- 🎙️ **Voice-to-Text Input**
- 🌐 **Instant Translation**
- 🔊 **Text-to-Speech Playback**
- 🔁 **Two-Way Conversation UI**
- 🌍 **Language Switcher Bottom Bar**
- 💾 **Chat History with Persistent Storage**
- 🧠 **Error & Edge Case Handling**
  - Network errors
  - STT “did not understand” feedback
- 📱 **Responsive UI**
  - Scales across phones/tablets with smooth animations

---

## 🛠️ How It Works

1. **Hold Mic** to start recording → release to stop  
2. Speech-to-Text converts voice → text  
3. Text is translated into the target language  
4. Text-to-Speech plays translated speech  
5. Messages are **persisted locally** for offline history  
6. Swap languages anytime via **bottom language switcher**

---

## 🧩 Tech Stack

### Framework
- Flutter (Dart), Material Design
- Responsive layout via `flutter_screenutil`

### State Management & DI
- **GetX** (`get`)
- Dependency injection with `Get.put`
- Reactive UI w/ `Obx` + Rx variables

### Audio
- Recording: `flutter_sound`
- Playback: `just_audio`
- TTS: `flutter_azure_tts` (Azure TTS)

### Data & Storage
- Local persistence: `hive_flutter`
- Repository pattern w/ caching

### Networking & Utilities
- `http`
- `permission_handler`
- `path_provider`
- `intl`
- `logger`
- `url_launcher`
- UI helpers: `flutter_spinkit`, `font_awesome_flutter`, `dash_flags`

### Build & Branding
- `flutter_launcher_icons`
- `flutter_native_splash`

---

## 🧱 Architecture Overview

### 📌 Controllers (GetX)
- `TalkScreenController` — orchestrates talk flow  
- `MessageSenderController` — recording + sending pipeline  
- `LanguageController` — selected languages + UI switches  
- `ChatListController` — chat state + persistence  
- `TalkScreenOverlayController` — UI events (snackbars, errors)

### 📌 Repositories
- `TranslatorRepository`, `SpeechRepository`
- `MessagesDatabaseRepository`, `LanguagesDatabaseRepository`

### 📌 Providers / Services
- **Remote**: Translator, Speech providers  
- **Local**: Hive DBs, Cache manager, Audio recorder/player  

### 📌 UI
- Chat list + message input (text or mic)
- Bottom language switcher
- Animated mic button + state transitions
- Themed speaker sections

---

## 📸 Screenshots

> Place your screenshots in `screenshots/` and reference them here!

Example:

| Talk Screen | Language Switcher | Recording & Processing | History |
|------------|------------------|-----------------------|--------|
| ![](screenshots/talk.png) | ![](screenshots/switch.png) | ![](screenshots/recording.png) | ![](screenshots/history.png) |

---

## 🔐 Notes on Privacy & Security

- API Keys + endpoints **excluded**
- **Source code not included**
- **Portfolio / showcase** purpose only

---

## 🙌 Credits

- Built with **Flutter** & **GetX**
- TTS powered by **Azure** via `flutter_azure_tts`

---

### ⭐ If you like this project…
Give this repo a **star** to support the work!

---

