# AI Camera App

Learn from photographers you admire. Get real-time coaching to capture similar shots.

## Quick Start

### 1. Prerequisites
- Mac with Xcode 15+ installed
- Apple Developer account ($99/year for App Store)
- iPhone for testing (iOS 17+)

### 2. Create Xcode Project
```bash
# Open Xcode
# File → New → Project
# Choose: iOS → App
# Product Name: AICamera
# Interface: SwiftUI
# Language: Swift
# Storage: SwiftData
```

### 3. Start Claude Code Session
```bash
cd AICamera  # Your Xcode project folder
claude
```

Then tell Claude:
> "Read the CLAUDE.md and help me build the camera view first with a live preview"

## Features

### MVP (Version 1.0)
- [ ] Camera view with live preview
- [ ] Manual photo capture
- [ ] Basic composition grid overlay
- [ ] Photo library integration

### Version 1.1 - Style Learning
- [ ] Add photographer by Instagram/Twitter handle
- [ ] Fetch and analyze sample photos
- [ ] Extract style characteristics
- [ ] Store style profile locally

### Version 1.2 - Real-time Guidance
- [ ] Composition suggestions overlay
- [ ] "Move camera" directional hints
- [ ] Settings recommendations
- [ ] "Perfect shot" indicator

### Version 1.3 - Advanced Features
- [ ] Multiple style profiles
- [ ] Before/after comparison
- [ ] Export settings to native Camera app
- [ ] Share style profiles

## Architecture
```
┌─────────────────────────────────────────────────┐
│                   SwiftUI Views                 │
├─────────────────────────────────────────────────┤
│  CameraView │ StyleView │ LibraryView │ Settings│
├─────────────────────────────────────────────────┤
│                   Managers                      │
│  CameraManager │ MLModelManager │ CloudKit     │
├─────────────────────────────────────────────────┤
│                   Core ML                       │
│  StyleClassifier │ CompositionAnalyzer         │
├─────────────────────────────────────────────────┤
│                 AVFoundation                    │
│         Camera Capture & Processing             │
└─────────────────────────────────────────────────┘
```

## Key Technologies

| Technology | Purpose |
|------------|---------|
| SwiftUI | User interface |
| AVFoundation | Camera access and control |
| Core ML | On-device ML inference |
| Create ML | Training custom models |
| Vision | Image analysis |
| SwiftData | Local data persistence |
| CloudKit | Cross-device sync |

## Cost Estimate
- Apple Developer Program: $99/year
- Development: Free (Xcode is free)
- Hosting: Free (CloudKit included)
- ML Training: Free (Create ML on Mac)

## Revenue Model Options
1. **Paid app:** $4.99-9.99 one-time
2. **Freemium:** Free with 1 style, $4.99 for unlimited
3. **Subscription:** $2.99/month for pro features

## App Store Optimization Keywords
- AI camera
- Photography coach
- Photo composition
- Camera settings
- Photography learning
- Style transfer
- Photography assistant

## Resources
- [Core ML Documentation](https://developer.apple.com/documentation/coreml)
- [Create ML Documentation](https://developer.apple.com/documentation/createml)
- [AVFoundation Camera Guide](https://developer.apple.com/documentation/avfoundation/capture_setup)
- [SwiftUI Tutorials](https://developer.apple.com/tutorials/swiftui)
