# Quote of the Day 💭

A beautiful cross-platform mobile application built with Flutter that curates, displays, and shares memorable and inspirational quotes to motivate and inspire users every day.


[![GitHub stars](https://img.shields.io/github/stars/heenaikramdekhan/Quote_of_Day?style=social)](https://github.com/heenaikramdekhan/Quote_of_Day/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/heenaikramdekhan/Quote_of_Day?style=social)](https://github.com/heenaikramdekhan/Quote_of_Day/network/members)



## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Platform Support](#platform-support)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the App](#running-the-app)
- [Project Structure](#project-structure)
- [Key Features Explained](#key-features-explained)
- [API Integration](#api-integration)
- [State Management](#state-management)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## 🎯 Overview

**Quote of the Day** is a cross-platform mobile application designed to provide users with daily motivation and inspiration through carefully curated quotes. The app delivers wisdom from authors, celebrities, philosophers, and thought leaders, helping users start their day with positive energy and mindful reflection.

### Why This App?

- **Daily Inspiration**: Get a fresh, motivating quote every day
- **Mental Wellness**: Start your day with positive affirmations
- **Easy Sharing**: Share quotes with friends and family
- **Beautiful Design**: Clean, minimalist UI for distraction-free reading
- **Cross-Platform**: Available on Android, iOS, Web, and Desktop

## ✨ Features

### Core Features

- **📅 Daily Quote Delivery**
  - New inspirational quote every day
  - Automatic refresh at midnight
  - Notification reminders (optional)

- **🎨 Beautiful User Interface**
  - Clean and minimalist design
  - Smooth animations and transitions
  - Dark mode support
  - Custom themes

- **📤 Share Functionality**
  - Share quotes to social media
  - Copy to clipboard
  - Save as image
  - WhatsApp, Twitter, Facebook integration

- **⭐ Favorites & Collections**
  - Save favorite quotes
  - Create custom collections
  - Browse quote history
  - Search saved quotes

- **🔍 Quote Categories**
  - Motivational
  - Inspirational
  - Love & Relationships
  - Success & Achievement
  - Wisdom & Philosophy
  - Humor
  - Life & Happiness

- **👤 Author Information**
  - View quotes by specific authors
  - Author biographies
  - Browse author collections

- **🔔 Notifications**
  - Daily quote reminders
  - Customizable notification time
  - Quote of the hour (optional)

- **🌐 Offline Support**
  - Access saved quotes offline
  - Local caching
  - Background sync

## 🛠️ Tech Stack

### Frontend Framework
- **Flutter 3.x** - UI Framework
- **Dart** - Programming Language

### Core Dependencies
- **http** - API calls and network requests
- **shared_preferences** - Local data storage
- **provider** / **riverpod** - State management
- **sqflite** - Local database for quotes
- **share_plus** - Share functionality
- **flutter_local_notifications** - Push notifications
- **cached_network_image** - Image caching
- **url_launcher** - Open external links

### Development Tools
- **Flutter DevTools** - Debugging and profiling
- **Android Studio / VS Code** - IDE
- **Git** - Version control


## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- **Flutter SDK** (3.0.0 or higher)
  - Download from [flutter.dev](https://flutter.dev/docs/get-started/install)
- **Dart SDK** (comes with Flutter)
- **Android Studio** or **Xcode** (for mobile development)
- **Git** for version control

### Verify Flutter Installation

```bash
flutter doctor
```

This command checks your environment and displays a report of the status of your Flutter installation.

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/heenaikramdekhan/Quote_of_Day.git
   ```

2. **Navigate to the project directory**
   ```bash
   cd Quote_of_Day
   ```

3. **Install dependencies**
   ```bash
   flutter pub get
   ```

4. **Check for available devices**
   ```bash
   flutter devices
   ```

### Running the App

#### Run on Android/iOS Emulator or Physical Device

```bash
# Run in debug mode
flutter run

# Run in release mode
flutter run --release

# Run on specific device
flutter run -d <device-id>
```

#### Run on Chrome (Web)

```bash
flutter run -d chrome
```

#### Run on Desktop (Windows/macOS/Linux)

```bash
# Windows
flutter run -d windows

# macOS
flutter run -d macos

# Linux
flutter run -d linux
```

### Building the App

#### Android APK

```bash
flutter build apk --release
```

The APK will be located at: `build/app/outputs/flutter-apk/app-release.apk`

#### iOS App

```bash
flutter build ios --release
```

#### Web App

```bash
flutter build web --release
```

The web build will be in the `build/web` directory.

## 📁 Project Structure

```
Quote_of_Day/
│
├── android/                    # Android-specific code
├── ios/                        # iOS-specific code
├── web/                        # Web-specific code
├── windows/                    # Windows-specific code
├── macos/                      # macOS-specific code
├── linux/                      # Linux-specific code
│
├── lib/                        # Main application code
│   ├── main.dart              # App entry point
│   ├── models/                # Data models
│   │   ├── quote.dart         # Quote model
│   │   └── author.dart        # Author model
│   ├── screens/               # UI screens
│   │   ├── home_screen.dart
│   │   ├── favorites_screen.dart
│   │   ├── categories_screen.dart
│   │   └── settings_screen.dart
│   ├── widgets/               # Reusable widgets
│   │   ├── quote_card.dart
│   │   ├── author_card.dart
│   │   └── loading_widget.dart
│   ├── services/              # Business logic
│   │   ├── api_service.dart   # API calls
│   │   ├── database_service.dart
│   │   └── notification_service.dart
│   ├── providers/             # State management
│   │   └── quote_provider.dart
│   ├── utils/                 # Utility functions
│   │   ├── constants.dart
│   │   └── helpers.dart
│   └── theme/                 # App theming
│       ├── app_theme.dart
│       └── colors.dart
│
├── test/                       # Unit and widget tests
├── assets/                     # Images, fonts, etc.
│   ├── images/
│   └── fonts/
│
├── pubspec.yaml               # Dependencies
├── analysis_options.yaml      # Linting rules
├── .gitignore                 # Git ignore rules
├── .metadata                  # Flutter metadata
└── README.md                  # This file
```

### Key Files Description

- **`lib/main.dart`**: Application entry point, sets up routing and theme
- **`lib/models/`**: Data models representing quotes, authors, and categories
- **`lib/screens/`**: Complete app screens/pages
- **`lib/widgets/`**: Reusable UI components
- **`lib/services/`**: API integration, database, and notifications
- **`lib/providers/`**: State management logic
- **`pubspec.yaml`**: Project configuration and dependencies

## 🔑 Key Features Explained

### 1. Quote Display & Management

The app fetches quotes from an API and displays them in an elegant, readable format:

```dart
// Example Quote Model
class Quote {
  final String id;
  final String text;
  final String author;
  final String category;
  final DateTime date;
  
  Quote({
    required this.id,
    required this.text,
    required this.author,
    required this.category,
    required this.date,
  });
}
```

### 2. State Management

Using Provider/Riverpod for efficient state management:

```dart
class QuoteProvider extends ChangeNotifier {
  Quote? _currentQuote;
  List<Quote> _favorites = [];
  
  Future<void> fetchDailyQuote() async {
    // Fetch from API
    notifyListeners();
  }
  
  void toggleFavorite(Quote quote) {
    // Add/remove from favorites
    notifyListeners();
  }
}
```

### 3. Local Storage

Quotes are cached locally using SQLite for offline access:

- Favorite quotes persistence
- Quote history
- User preferences
- Offline functionality

### 4. Share Functionality

Users can share quotes via multiple channels:

```dart
Future<void> shareQuote(Quote quote) async {
  final shareText = '"${quote.text}" - ${quote.author}';
  await Share.share(shareText);
}
```

## 🌐 API Integration

The app integrates with quote APIs to fetch daily quotes:

### Supported APIs

- **Quotable API** - Free random quotes
- **They Said So API** - Quote of the day
- **ZenQuotes API** - Inspirational quotes
- **Custom Backend** (optional)

### API Service Example

```dart
class ApiService {
  static const String baseUrl = 'https://api.quotable.io';
  
  Future<Quote> getRandomQuote() async {
    final response = await http.get(
      Uri.parse('$baseUrl/random')
    );
    
    if (response.statusCode == 200) {
      return Quote.fromJson(json.decode(response.body));
    }
    throw Exception('Failed to load quote');
  }
}
```

## 🎨 UI/UX Design Principles

- **Minimalist Design**: Focus on content, not clutter
- **Typography**: Large, readable fonts for quote text
- **Color Scheme**: Calming colors that promote positivity
- **Animations**: Smooth transitions and micro-interactions
- **Accessibility**: Support for screen readers and large text

## 🔮 Future Enhancements

### Planned Features

- [ ] **User Authentication**
  - Sign in with Google/Apple
  - Sync favorites across devices
  - Cloud backup

- [ ] **Advanced Features**
  - Quote wallpapers generator
  - Voice reading of quotes
  - Widget for home screen
  - Custom quote creation

- [ ] **Social Features**
  - Like and comment on quotes
  - Follow favorite authors
  - Community quotes sharing
  - User-generated content

- [ ] **Personalization**
  - AI-powered quote recommendations
  - Mood-based quote selection
  - Learning from user preferences
  - Custom categories

- [ ] **Gamification**
  - Daily streak tracking
  - Achievement badges
  - Quote challenges
  - Leaderboards

- [ ] **Multi-language Support**
  - Internationalization (i18n)
  - Quotes in multiple languages
  - Translation feature

- [ ] **Premium Features**
  - Ad-free experience
  - Exclusive quote collections
  - Advanced customization
  - Unlimited favorites

## 🧪 Testing

Run tests with:

```bash
# Run all tests
flutter test

# Run with coverage
flutter test --coverage

# Run integration tests
flutter drive --target=test_driver/app.dart
```

## 📦 Dependencies

Key dependencies from `pubspec.yaml`:

```yaml
dependencies:
  flutter:
    sdk: flutter
  http: ^1.1.0
  provider: ^6.0.5
  shared_preferences: ^2.2.2
  sqflite: ^2.3.0
  share_plus: ^7.2.1
  flutter_local_notifications: ^16.3.0
  cached_network_image: ^3.3.0
  url_launcher: ^6.2.2
```



## 📚 Resources

### Flutter Learning Resources

- [Flutter Documentation](https://flutter.dev/docs)
- [Dart Language Tour](https://dart.dev/guides/language/language-tour)
- [Flutter Cookbook](https://flutter.dev/docs/cookbook)
- [Flutter YouTube Channel](https://www.youtube.com/c/flutterdev)

### Quote APIs

- [Quotable API](https://github.com/lukePeavey/quotable)
- [ZenQuotes API](https://zenquotes.io/)
- [They Said So API](https://theysaidso.com/api/)

### State Management

- [Provider Documentation](https://pub.dev/packages/provider)
- [Riverpod Guide](https://riverpod.dev/)

## 📈 Project Roadmap

- [x] Basic quote display
- [x] Favorites functionality
- [x] Share feature
- [x] Offline support
- [ ] User authentication
- [ ] Cloud sync
- [ ] Widget support
- [ ] Voice reading
- [ ] Multi-language support

---

**Made with ❤️ and Flutter**

*Start each day with inspiration!*

---

**Disclaimer**: Quotes are sourced from public APIs and are attributed to their respective authors. This app is for educational and inspirational purposes.
