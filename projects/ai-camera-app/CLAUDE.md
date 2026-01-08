# AI Camera App - Claude Code Instructions

## Project Overview
iOS app that learns from photographers' styles and provides real-time guidance to help users take photos in similar styles. Uses on-device ML for privacy and performance.

## Tech Stack
- **Language:** Swift 5.9+
- **UI Framework:** SwiftUI
- **ML Framework:** Core ML, Create ML, Vision
- **Camera:** AVFoundation
- **Storage:** CloudKit (sync), SwiftData (local)
- **Minimum iOS:** 17.0

## Project Structure
```
AICamera/
├── AICamera.xcodeproj
├── AICamera/
│   ├── App/
│   │   ├── AICameraApp.swift
│   │   └── ContentView.swift
│   ├── Features/
│   │   ├── Camera/
│   │   │   ├── CameraView.swift
│   │   │   ├── CameraManager.swift
│   │   │   └── CameraOverlayView.swift
│   │   ├── StyleAnalysis/
│   │   │   ├── StyleAnalyzer.swift
│   │   │   ├── PhotoFetcher.swift
│   │   │   └── StyleModel.swift
│   │   ├── Guidance/
│   │   │   ├── CompositionGuide.swift
│   │   │   ├── SettingsOptimizer.swift
│   │   │   └── CoachingEngine.swift
│   │   └── Library/
│   │       ├── PhotoLibraryView.swift
│   │       └── BeforeAfterView.swift
│   ├── Models/
│   │   ├── PhotographerStyle.swift
│   │   ├── PhotoSettings.swift
│   │   └── GuidanceInstruction.swift
│   ├── Services/
│   │   ├── MLModelManager.swift
│   │   ├── CloudKitManager.swift
│   │   └── PermissionsManager.swift
│   ├── CoreML/
│   │   └── StyleClassifier.mlmodel
│   ├── Resources/
│   │   └── Assets.xcassets
│   └── Utilities/
│       └── Extensions.swift
├── AICameraTests/
├── AICameraUITests/
└── README.md
```

## Coding Standards
- Use SwiftUI for all UI (no UIKit unless absolutely necessary)
- Follow Apple's Human Interface Guidelines
- Use async/await for all asynchronous operations
- Implement proper error handling with Result types
- Use SwiftData for local persistence
- Keep views small and composable

## Core ML Model Requirements
The style classifier model should:
- Run on-device (no cloud inference)
- Analyze composition (rule of thirds, leading lines, symmetry)
- Detect color palette preferences
- Identify lighting patterns (golden hour, high contrast, soft light)
- Process in <100ms for real-time feedback

## Camera Features to Implement
1. **Real-time composition overlay**
   - Grid lines (rule of thirds)
   - Dynamic guides based on learned style

2. **Settings optimization**
   - ISO recommendation
   - Shutter speed suggestion
   - White balance adjustment
   - Focus point suggestion

3. **Coaching feedback**
   - "Move camera slightly left"
   - "Lower your angle"
   - "Wait for better lighting"
   - "Perfect! Take the shot"

## Privacy Requirements
- ALL ML processing on-device
- Never upload photos to external servers
- CloudKit only for user's own data sync
- Clear privacy policy in App Store listing
- Request only necessary permissions

## App Store Requirements
- Support all iPhone sizes (iPhone 12+)
- Dark mode support
- Accessibility labels on all UI elements
- Localization-ready strings
- No crashes in TestFlight before submission

## Performance Targets
- Camera preview: 60fps
- ML inference: <100ms
- App launch: <2 seconds
- Memory usage: <200MB active

## Testing Requirements
- Unit tests for ML model manager
- Unit tests for settings optimizer
- UI tests for camera flow
- Performance tests for ML inference

## Do NOT
- Send photos to external APIs
- Require account creation for basic features
- Use UIKit when SwiftUI works
- Block the main thread with ML inference
- Request unnecessary permissions
- Include analytics without user consent
