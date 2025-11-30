# Signal ECU

Signal ECU is a Flutter-based mobile application designed to help users interact with and monitor ECU-related signals in a modern, user-friendly UI.  
It focuses on providing clear visualization, essential information, and convenient tools for working with ECU data on both Android and iOS.

> This repository is part of my portfolio and is intended to demonstrate my mobile development skills in Flutter (Dart), state management, theming, and app architecture.

---

## ℹ️ Application Information

- **Category**: *[Fill from `categoryDes`, e.g. “Automotive · Utilities · Tools”]*  
- **Supported Platforms**: Android, iOS  
- **Required OS**: *[Fill from `requiredOSDes`, e.g. “Android 8.0+ / iOS 13+”]*  
- **Release Date**: *[Fill from `releaseDateDes`, e.g. “November 2025”]*  
- **Website**: `Constants.appWebsiteUrl`  
- **Version**: Displayed in‑app via the `AppVersionText` widget (follows semantic versioning)

---

## 📝 Description

The in-app About screen describes Signal ECU with two main sections of text:

- **Description (1)** – `descriptionsText1`  
  A high-level overview of what Signal ECU does and who it is for.  
  *Example (replace with your real wording):*  
  “Signal ECU helps technicians and enthusiasts inspect, read and understand ECU signals in a clean and accessible interface.”

- **Description (2)** – `descriptionsText2`  
  A more detailed explanation of usage or typical workflows.  
  *Example (replace with your real wording):*  
  “Use the app to browse available signals, review important parameters, and access related information in a structured way.”

You can update the actual localized strings in your language files; this README is aligned with that About screen structure.

---

## 🧰 Key Features

As shown in the About screen (`keyFeatures` / `keyFeaturesDes`):

- **Key Features Summary**  
  *Example bullets – align them with `keyFeaturesDes` in your localization:*
  - Real-time viewing of ECU-related signal information.
  - Clear, RTL-friendly UI with theming support (light/dark).
  - Organized information cards for app version, category, required OS, and website.
  - Smooth page transitions and animations using `animate_do`.
  - Modern responsive layout using `flutter_screenutil`.

- **Internet Connection Requirement**  
  The About screen highlights: `internerConnectionRequired`  
  *Example wording:*  
  “An active internet connection is required for some features (such as fetching the latest data or remote resources).”

---

## 🧱 Architecture & Tech Stack

- **Framework**: Flutter (Dart)
- **State / Dependency Management**: GetX (`Get.find<ThemeController>()` for theming)
- **Navigation**: `auto_route`
- **Theming & Layout**:
  - Custom `ThemeController` for app-wide theme management
  - `flutter_screenutil` for responsive sizing (`.w`, `.h`, `.sp`, `.r`)
  - Right-to-left (`TextDirection.rtl`) support
- **UI Components**:
  - `AppBaseScreen` for base layout and gradient backgrounds
  - `CustomAppBar` for consistent app bars
  - `AppCustomCard` for feature-specific cards
  - Animated transitions: `SlideInUp`, `FadeIn` from `animate_do`
- **Code Organization**:
  - [lib/views/utility/about_app_screen.dart](cci:7://file:///Users/mac/StudioProjects/signal_ecu/lib/views/utility/about_app_screen.dart:0:0-0:0) for the About screen
  - Common widgets & extensions under `common/widgets` and `common/extensions.dart`
  - Constants in `common/constants/constants.dart`

---

## 📱 Download / References

You can use these badges as reference buttons for Android and iOS once you have the links:

[//]: # "Replace the URLs below with your actual store / download links."

- **Android**  
  [![Android Reference](https://img.shields.io/badge/Android-App-green?logo=android&logoColor=white)](https://your-android-link-here)

- **iOS**  
  [![iOS Reference](https://img.shields.io/badge/iOS-App-black?logo=apple&logoColor=white)](https://your-ios-link-here)

> Once you provide the real links, just replace `https://your-android-link-here` and `https://your-ios-link-here` above.

---

## 🚀 Getting Started (Development)

1. **Clone the repository**

   ```bash
   git clone [https://github.com/your-username/signal_ecu.git](https://github.com/your-username/signal_ecu.git)
   cd signal_ecu