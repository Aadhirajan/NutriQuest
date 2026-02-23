# NutriQuest

NutriQuest is a Flutter-based nutrition and wellness companion app that helps you make healthier choices. It includes barcode scanning for nutrition lookup, food intake/search, scan history, water tracking, body fat % tools, and exercise guidance.

## Features

- **Barcode scanning** to fetch/check nutrition facts (uses `mobile_scanner`)
- **Scan history** to revisit previously scanned items
- **Food intake / search** experience
- **Water tracker**
- **Body Fat % (BFP%)** section
- **Exercise** section (male/female exercise data from JSON)
- **Progress visualization** (charts via `fl_chart`)
- **Local storage** for persistence (via `shared_preferences`)
- **Feedback / Help / About Us** screens

## Tech Stack

- **Flutter / Dart** (SDK constraint in `pubspec.yaml`: `^3.6.0`)
- Key packages:
  - `mobile_scanner` (barcode scanning)
  - `http` (API/network calls)
  - `shared_preferences` (local persistence)
  - `fl_chart` (charts/graphs)
  - `intl` (formatting)
  - `flutter_local_notifications` + `timezone` (notifications)
  - `google_fonts`, `lottie` (UI/animations)

## Project Structure (high level)

- `lib/` – application screens and logic
  - `main.dart` – home page + navigation entry
  - `scan_page.dart` – scanning flow
  - `history_page.dart` – scan history
  - `search_page.dart` – intake/search
  - `water.dart` – water tracking
  - `body_fat_page.dart` – body fat % tools
  - `exercise_page.dart` – exercise UI
  - plus: `product_service.dart`, `storage_helper.dart`, etc.
- `assets/` – images + datasets
  - `products.json` – product/nutrition dataset
  - `male_exercise.json`, `female_exercise.json` – exercise datasets

> Note: assets include many images and JSON files; see the full directory in GitHub:
> https://github.com/Aadhirajan/NutriQuest/tree/main/assets  
> (The API listing I fetched is limited and may not show every asset in one response.)

## Getting Started

### Prerequisites
- Flutter installed and on PATH
- A compatible SDK (per `pubspec.yaml`): **Dart SDK `^3.6.0`**
- Android Studio / Xcode (depending on target platform)

### Run locally

```bash
git clone https://github.com/Aadhirajan/NutriQuest.git
cd NutriQuest
flutter pub get
flutter run
```

### Build

```bash
# Android APK (debug)
flutter build apk

# iOS (requires macOS + Xcode)
flutter build ios

# Web
flutter build web
```

## Assets

This project uses bundled assets configured in `pubspec.yaml`:

- `assets/`
- `assets/products.json`
- `assets/male_exercise.json`
- `assets/female_exercise.json`

If you add new assets, remember to update `pubspec.yaml` and run:

```bash
flutter pub get
```

## Screens / Navigation

The home screen provides quick actions such as:
- **Scan Now**
- **Scan History**
- **Intake**

And additional sections like:
- **Water**
- **BFP%**
- **Exercise**

(See `lib/main.dart`.)

## License

This project is licensed under the terms of the **LICENSE** file in this repository.

---

### Disclaimer

NutriQuest is intended for informational and educational use. It is **not** medical advice. Always consult qualified health professionals for medical guidance.
