# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

ScrollWalker is an iOS app built with SwiftUI targeting iOS 26.1+. The project uses Xcode 26.1.1 and Swift 5.0.

## Project Structure

```
ScrollWalker/
├── ScrollWalker/              # Main app target
│   ├── ScrollWalkerApp.swift  # App entry point (@main)
│   ├── ContentView.swift      # Root view
│   └── Assets.xcassets/       # App assets and icons
└── ScrollWalker.xcodeproj/    # Xcode project file
```

## Building and Running

**Build the project:**
```bash
cd "/Users/tabi/Desktop/coding/iOS ScrollWalker/ScrollWalker"
xcodebuild -project ScrollWalker.xcodeproj -scheme ScrollWalker -configuration Debug
```

**Build for release:**
```bash
xcodebuild -project ScrollWalker.xcodeproj -scheme ScrollWalker -configuration Release
```

**Clean build folder:**
```bash
xcodebuild clean -project ScrollWalker.xcodeproj -scheme ScrollWalker
```

**Run in simulator:**
Open the project in Xcode and use Cmd+R, or use:
```bash
xcodebuild -project ScrollWalker.xcodeproj -scheme ScrollWalker -destination 'platform=iOS Simulator,name=iPhone 16' -configuration Debug
```

## Key Configuration

- **Bundle Identifier:** `tabi.ScrollWalker`
- **Deployment Target:** iOS 26.1
- **Swift Version:** 5.0
- **Supported Devices:** iPhone and iPad (Universal)
- **Orientation Support:** Portrait and Landscape
- **SwiftUI Previews:** Enabled

## Development Notes

- This is a SwiftUI-based app using the modern App lifecycle (`@main` struct conforming to `App`)
- SwiftUI previews are available for all views using `#Preview` macro
- The project uses automatic code signing (development)
- Swift concurrency is enabled with `SWIFT_APPROACHABLE_CONCURRENCY` and `MainActor` isolation

## Architecture

The app follows standard SwiftUI architecture:
- `ScrollWalkerApp.swift` defines the app entry point and initial scene
- `ContentView.swift` is the root view that will contain the main UI
- Future views, models, and business logic should be organized into separate directories (Views/, Models/, ViewModels/, etc.)
