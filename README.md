# Animated Responsive Layout

A Flutter application demonstrating an animated responsive layout that adapts seamlessly across different screen sizes. This project showcases a modern email-like interface with smooth transitions, responsive design patterns, and interactive elements.

## Features

- **Responsive Design**: Automatically adapts layout for mobile, tablet, and desktop screens
- **Email Interface**: Modern email-like UI with message list and detailed conversation view
- **Smooth Animations**: Custom transitions and animations for navigation and content changes
- **Interactive Elements**: Star buttons, floating action button, and navigation controls
- **Search Functionality**: Integrated search bar for filtering messages
- **Multi-platform Support**: Runs on web, mobile, and desktop platforms

## Screenshots

### Desktop/Web View
![Application Screenshot](screenshot.png)

The application features a two-column layout with:
- **Left Panel**: Navigation rail, search bar, and message list
- **Right Panel**: Detailed conversation view with message threads
- **Responsive Elements**: Navigation adapts based on screen size

### Mobile View
The app automatically switches to a single-column layout on smaller screens with:
- Bottom navigation bar
- Collapsible navigation rail
- Optimized touch interactions

## Installation

### Prerequisites

- **Flutter SDK**: Version 3.8.1 or higher
- **Dart SDK**: Included with Flutter
- **Platform-specific requirements**:
  - **Web**: Any modern web browser
  - **Android**: Android Studio with Android SDK
  - **iOS**: Xcode (macOS only)
  - **Windows**: Visual Studio with C++ workload
  - **macOS**: Xcode
  - **Linux**: CMake and build essentials

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <repository_url>
   cd animated_responsive_layout
   ```

2. **Install Flutter dependencies**
   ```bash
   flutter pub get
   ```

3. **Download required assets**
   
   The project requires several image assets. Navigate to the assets directory and download them:
   
   ```bash
   cd assets
   ```
   
   **For Windows (PowerShell):**
   ```powershell
   $images = @('avatar_1', 'avatar_2', 'avatar_3', 'avatar_4', 'avatar_5', 'avatar_6', 'avatar_7', 'thumbnail_1')
   foreach($img in $images) { 
       Invoke-WebRequest -Uri "https://raw.githubusercontent.com/flutter/codelabs/main/animated-responsive-layout/step_04/assets/$img.png" -OutFile "$img.png"
       Write-Host "Downloaded $img.png"
   }
   ```
   
   **For macOS/Linux:**
   ```bash
   for name in avatar_1 avatar_2 avatar_3 avatar_4 avatar_5 avatar_6 avatar_7 thumbnail_1; do
       curl -o "$name.png" "https://raw.githubusercontent.com/flutter/codelabs/main/animated-responsive-layout/step_04/assets/$name.png"
   done
   ```
   
   **Alternative (using wget):**
   ```bash
   for name in avatar_1 avatar_2 avatar_3 avatar_4 avatar_5 avatar_6 avatar_7 thumbnail_1; do
       wget "https://raw.githubusercontent.com/flutter/codelabs/main/animated-responsive-layout/step_04/assets/$name.png"
   done
   ```

4. **Return to project root**
   ```bash
   cd ..
   ```

5. **Run the application**
   
   **For Web (Chrome):**
   ```bash
   flutter run -d chrome
   ```
   
   **For Web (Edge):**
   ```bash
   flutter run -d edge
   ```
   
   **For Windows Desktop:**
   ```bash
   flutter run -d windows
   ```
   
   **For Android:**
   ```bash
   flutter run -d android
   ```
   
   **For iOS (macOS only):**
   ```bash
   flutter run -d ios
   ```
   
   **For macOS Desktop:**
   ```bash
   flutter run -d macos
   ```
   
   **For Linux Desktop:**
   ```bash
   flutter run -d linux
   ```

## Project Structure

```
animated_responsive_layout/
├── lib/
│   ├── main.dart                          # Main application entry point
│   ├── animations.dart                    # Custom animation definitions
│   ├── destinations.dart                  # Navigation destinations
│   ├── models/
│   │   ├── data.dart                      # Sample data and mock content
│   │   └── models.dart                    # Data model definitions
│   ├── transitions/
│   │   ├── bottom_bar_transition.dart     # Bottom navigation animations
│   │   ├── list_detail_transition.dart    # List to detail view transitions
│   │   └── nav_rail_transition.dart       # Navigation rail animations
│   └── widgets/
│       ├── animated_floating_action_button.dart
│       ├── disappearing_bottom_navigation_bar.dart
│       ├── disappearing_navigation_rail.dart
│       ├── email_list_view.dart
│       ├── email_widget.dart
│       ├── reply_list_view.dart
│       ├── search_bar.dart
│       └── star_button.dart
├── assets/
│   ├── avatar_1.png through avatar_7.png  # User profile images
│   └── thumbnail_1.png                    # Message attachment thumbnail
├── android/                               # Android platform files
├── ios/                                   # iOS platform files
├── web/                                   # Web platform files
├── windows/                               # Windows platform files
├── macos/                                 # macOS platform files
├── linux/                                 # Linux platform files
├── pubspec.yaml                           # Flutter dependencies and configuration
└── README.md                              # This file
```

## Key Components

### Responsive Layout
- **Navigation Rail**: Collapsible sidebar navigation for larger screens
- **Bottom Navigation**: Mobile-optimized bottom navigation bar
- **Adaptive UI**: Automatically switches between layouts based on screen size

### Animations
- **List-Detail Transition**: Smooth transitions between list and detail views
- **Navigation Animations**: Animated navigation rail and bottom bar
- **Floating Action Button**: Animated FAB with contextual actions

### Data Models
- **Email**: Message structure with sender, recipients, content, and attachments
- **User**: User profile with name, avatar, and activity status
- **Attachment**: File attachment support with image thumbnails

## Development

### Running in Debug Mode
```bash
flutter run --debug
```

### Building for Production

**Web:**
```bash
flutter build web
```

**Android APK:**
```bash
flutter build apk
```

**iOS:**
```bash
flutter build ios
```

**Windows:**
```bash
flutter build windows
```

**macOS:**
```bash
flutter build macos
```

**Linux:**
```bash
flutter build linux
```

### Code Analysis
```bash
flutter analyze
```

### Running Tests
```bash
flutter test
```

## Customization

### Adding New Messages
Edit `lib/models/data.dart` to add new email messages or modify existing ones.

### Styling
The app uses Material Design 3 theming. Modify the theme in `main.dart` or create custom themes.

### Adding New Animations
Add custom animations in `lib/animations.dart` and reference them in your widgets.

## Troubleshooting

### Common Issues

1. **Assets not loading**: Ensure all image files are in the `assets/` directory and properly declared in `pubspec.yaml`

2. **Build errors**: Run `flutter clean` and `flutter pub get` to refresh dependencies

3. **Platform-specific issues**: Check that you have the required platform tools installed

4. **Web-specific issues**: Clear browser cache or try a different browser

### Getting Help

- Check the [Flutter documentation](https://flutter.dev/docs)
- Review [Flutter troubleshooting guide](https://flutter.dev/docs/get-started/install)
- Search [Stack Overflow](https://stackoverflow.com/questions/tagged/flutter) for similar issues

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Based on the Flutter codelab: [Animated Responsive Layout](https://codelabs.developers.google.com/codelabs/flutter-animated-responsive-layout)
- Uses Material Design 3 components and theming
- Inspired by modern email client interfaces

---

**Note**: This project is for educational and demonstration purposes. It showcases Flutter's responsive design capabilities and animation system.