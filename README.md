# logappa — Private Work & Break Time Tracker

A cross-platform Flutter application for private, personal work and break time tracking with a rich UI, an iconic Apple iPhone-style "logappa" animated launcher greeting, pure white background, signature vibrant orange navigation & buttons, and 100% local device storage (`SharedPreferences`).

---

## Key Features

- 📱 **iPhone "hello" Style Launcher Screen**:
  - Pure white background (`#FFFFFF`) with centered iconic black font animated **`logappa`** greeting.
  - Smooth fade, subtle scale, and letter transition that gracefully moves into the app.

- 🔒 **100% Private to the User (No Admin Overhead)**:
  - Tailored specifically for individual users (engineers, designers, freelancers, professionals).
  - All shift timers, break logs, and settings stay strictly on your local device.
  - Zero company servers, zero remote surveillance.

- 👤 **Easy Personal Details Setup (Onboarding)**:
  - Enter your Name, Job Title, Workspace/Company, Daily Target Hours, and optional Hourly Rate.
  - Edit or update preferences anytime in the Profile tab.

- ⏱️ **Real-Time Work & Break Engine**:
  - Live ticking timer (`HH:MM:SS`) with circular glowing status ring.
  - Real-time break management: **Lunch Break** (45m), **Short Break** (15m), **Coffee Break** (10m), **Wellness Walk** (20m), or **Custom Break**.
  - Automatically pauses working hours during breaks and resumes seamlessly.

- 🎨 **Minimalist Design & Orange Controls**:
  - Clean white canvas (`#FFFFFF`).
  - High-visibility **Orange** navigation and primary action buttons (`#FF5722` / `#F97316`).
  - App icon featuring minimalist black typography on a pure white background.

- 📊 **Private Analytics & CSV Export**:
  - 7-day work vs. break distribution chart powered by `fl_chart`.
  - Productivity metrics: Average daily shift length, break compliance, and overtime tracking.
  - Export personal records to formatted CSV with one-click clipboard copy.

---

## Project Structure

```
lib/
├── main.dart                      # App entry point with MultiProvider & SplashScreen
├── models/
│   ├── user_model.dart            # Private user profile (Name, Title, Workplace, Target hours)
│   ├── break_model.dart           # BreakType enum, durations, and serialization
│   └── shift_model.dart           # ShiftModel with net work & break calculations
├── services/
│   ├── storage_service.dart       # SharedPreferences persistence layer
│   └── mock_data_service.dart     # Sample initial shifts for local history
├── providers/
│   ├── auth_provider.dart         # Private user profile & onboarding state
│   ├── shift_provider.dart        # Real-time shift & break timer engine
│   └── theme_provider.dart        # Light / Dark theme manager
├── theme/
│   └── app_theme.dart             # Pure white background with vibrant orange palette
├── widgets/
│   ├── live_timer_display.dart    # Circular glowing timer card
│   ├── break_dialog.dart          # Break selection modal with note input
│   ├── stat_card.dart             # KPI stat card with icon & badge
│   ├── work_stats_chart.dart      # Weekly bar chart
│   ├── location_badge.dart        # Location selector pill
│   └── pulse_badge.dart           # Animated status indicator
└── screens/
    ├── splash_screen.dart         # iPhone setup-style animated black "logappa" launcher
    ├── onboarding_screen.dart     # Personal details & work goal setup
    ├── main_layout_screen.dart    # Bottom navigation & logappa app bar
    ├── employee_dashboard_screen.dart # Private work time & break tracker
    ├── shift_history_screen.dart  # Personal shift history & CSV export
    ├── statistics_screen.dart     # Productivity & break charts
    └── profile_screen.dart        # Profile & privacy settings
```

---

## How to Run

### Run on macOS (Desktop)
```bash
flutter run -d macos
```

### Run on Chrome (Web)
```bash
flutter run -d chrome
```

### Run Automated Tests
```bash
flutter test
```

### Run Static Analysis
```bash
flutter analyze
```
