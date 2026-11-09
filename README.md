<div align="center">
  <img src="assets/logo_magdyloops.png" alt="MagdyLoops Logo" width="200" />

  # MagdyLoops
  **A Cozy, Minimalist Row & Round Counter, Pattern Organizer, and Yarn Calculator for Knitting & Crochet**

  [![Platform](https://img.shields.io/badge/Platform-Android%208.0%2B-3DDC84?logo=android&logoColor=white)](#)
  [![Kotlin](https://img.shields.io/badge/Kotlin-2.2-7F52FF?logo=kotlin&logoColor=white)](#)
  [![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack%20Compose%20%2B%20Material%203-4285F4?logo=jetpackcompose&logoColor=white)](#)
  [![Google Play](https://img.shields.io/badge/Google%20Play-Coming%20Soon-CEA8F0?logo=googleplay&logoColor=563078)](#-download--availability)
</div>

---

## 📲 Download & Availability

> **🚧 Coming Soon to Google Play!**  
> **MagdyLoops** is currently preparing for its official release on the **Google Play Store**. Once the store listing is live, the official **Get it on Google Play** button and direct link will be added right here!

---

## 💡 Overview & Inspiration

**MagdyLoops** was designed from the ground up as a distraction-free, tactile companion for knitters and crocheters. When your hands are busy holding needles, a crochet hook, and working yarn, tapping tiny buttons on a cluttered screen breaks your rhythm.

MagdyLoops solves this by combining **warm pastel aesthetics** and **vintage Kraft cardboard hangtags** with an **ultra-minimalist, eyes-free counting experience**.

---

## ✨ Key Features

### 1. Personalized Craft Spaces
- Supports **Knitting**, **Crochet**, or **Both** during onboarding.
- Automatically tailors terminology and tool presets (e.g., **Needles** & **Rows** for Knitting; **Hooks**, **Rounds**, & **Granny Squares / Plushie Pieces** for Crochet).

### 2. Tactile Kraft Cardboard Hangtags
- Each project card is styled after a cozy yarn swatch paired with a **Kraft Cardboard Spec Tag** (`#EADBC8`) featuring a punch-hole eyelet.
- Stores **Needle / Hook Size** (with 1-tap metric & US presets), **Yarn & Colorway**, **Pattern Notes**, **Goal Rows/Rounds**, and a **Multi-Piece Counter** (for tracking motifs, sleeves, or amigurumi limbs right from the dashboard).

### 3. Eyes-Free Minimalist Counter Screen
- **Full-Screen Invisible Split Tap Zones**: Tap anywhere in the upper 62% of the screen to add `+1`, or the lower 38% to subtract `-1`.
- **Hardware Volume Button Support**: Increment (`Volume Up`) and decrement (`Volume Down`) while the phone rests on the couch or table—without triggering the Android system volume slider.
- **Distinct Haptic Vibration Waveforms**:
  - **`+1` (Increment)**: A crisp, firm single-pulse click (`32ms`).
  - **`-1` (Decrement)**: A unmistakable double-pulse (`buzz–buzz`) so you immediately feel if you pressed the wrong button without looking at the screen.
  - **Goal Reached (`e.g. 60 / 60 ✨`)**: A celebratory rising triple-pulse vibration paired with a **60fps physics confetti burst**.
- **Keep Screen Awake Toggle**: Prevents the display from dimming or locking mid-row.

### 4. Pattern Plans & Row-Stamped Progress Photos
- **Pattern Plans**: Attach stitch charts, diagrams, or pattern screenshots to any project and inspect tiny symbols with a **full-screen pinch-to-zoom & double-tap viewer**.
- **Progress Milestones**: Snap or attach work-in-progress photos that are automatically stamped with the exact **Row / Round number** at the moment the photo was saved.
- **Scrapbook Gallery**: Browse all progress photos and pattern plans across every project in one place.

### 5. Built-In 3-in-1 Yarn Calculator
- **Project Estimator**: Estimates total meters, yards, and skeins needed for presets (**Beanie**, **Scarf**, **Socks**, **Amigurumi**, **Top / Tank**, **T-Shirt**, **Baby Blanket**, **Adult Sweater**, **Throw Blanket**) across yarn weights (`Fingering` to `Chunky`), automatically accounting for the ~28% higher yarn usage of crochet vs. knitting.
- **Leftover Skein Calculator**: Weigh a partial yarn ball in grams on a kitchen scale to calculate exactly how many meters and yards remain.
- **Yarn Swap Helper**: Calculates how many skeins you need when substituting a yarn with a different meterage per ball than the pattern specifies.

---

## 🛠️ How It Was Built (Architecture & Technical Highlights)

MagdyLoops is a 100% native Android application built with modern Android engineering practices:

| Layer | Technology & Implementation |
| :--- | :--- |
| **Language** | **Kotlin 2.2** with Coroutines, `StateFlow`, and `SharedFlow` |
| **UI Framework** | **Jetpack Compose** + **Material 3** (Custom Light & Dark palettes with adaptive status/navigation bar insets) |
| **Navigation** | **Jetpack Navigation Compose** with spring & eased horizontal slide/fade transitions |
| **Architecture** | **MVVM** (`MagdyLoopsViewModel` coordinating reactive UI state and hardware key events) |
| **Local Persistence** | **SQLite (`SQLiteOpenHelper` v2)** with two relational tables (`projects` and `project_photos`) + internal file storage for offline images |
| **Custom Graphics** | Frame-synchronized Compose `Canvas` (`withFrameNanos`) driving a 110-particle physics confetti engine with gravity, air sway, and 3D tumble |
| **Hardware Integration** | Custom `KeyEvent` interception in `MainActivity` + `VibratorManager` / `VibrationEffect` waveform synthesis |
| **App Icon** | Android 8.0+ **Adaptive Icon** (`108dp` layered foreground/background) + Android 13+ **Monochrome Themed Icon** |

---

## 🔒 Privacy & Offline-First Design

MagdyLoops operates **100% offline**. It requires no account, contains zero ads or analytics trackers, and uses Android's permissionless **System Photo Picker** (`PickVisualMedia`) so your personal photo library remains private.

📄 Read the full **[Privacy Policy](PRIVACY_POLICY.md)**.
