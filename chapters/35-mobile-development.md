# Chapter 35: Mobile Development

**Last Updated:** February 5, 2026

---

## Overview

Mobile development creates applications for smartphones and tablets, reaching users on their most personal devices. Whether building native or cross-platform applications, mobile development requires understanding platform-specific patterns and performance optimization.

This chapter covers essential mobile development skills for building high-quality iOS, Android, and cross-platform mobile applications.

### Skills Covered in This Chapter

| Skill | Purpose | Best For |
|-------|---------|----------|
| `@react-native-expert` | React Native | Cross-platform, React developers |
| `@flutter-expert` | Flutter development | Cross-platform, performance focus |
| `@ios-expert` | iOS development | Native iOS, Swift |
| `@android-expert` | Android development | Native Android, Kotlin |

---

## 35.1 React Native Development with @react-native-expert

### Skill Introduction

The `@react-native-expert` skill provides expertise in React Native for cross-platform mobile development. It helps you build iOS and Android apps with a shared JavaScript/TypeScript codebase.

**When to use this skill:**
- Cross-platform mobile apps
- Leveraging React expertise
- Native module integration
- Performance optimization

**Key strengths:**
- Deep React Native knowledge
- Experience with native bridges
- Understanding of mobile patterns

---

### React Native Development Prompts

#### Building React Native Application

**Context:** You're building a cross-platform mobile app with React Native.

```text
@react-native-expert Design a React Native application architecture:

Application:
- E-commerce mobile app
- Product browsing and search
- Cart and checkout
- User authentication
- Push notifications
- Offline capability

Requirements:
- React Native with TypeScript
- Expo or bare workflow (recommend)
- Navigation with React Navigation
- State management approach
- API client with offline sync
- Native modules if needed

Quality requirements:
- 60fps animations
- Small bundle size
- Fast startup time
- Cross-device consistency

Please provide:
1. Project setup recommendation (Expo vs bare)
2. Application structure
3. Navigation architecture
4. State management approach
5. API and offline strategy
6. Native module decisions
7. Testing approach
8. CI/CD for mobile
```

**Expected Output:** React Native application architecture.

---

## 35.2 Flutter Development with @flutter-expert

### Skill Introduction

The `@flutter-expert` skill provides expertise in Flutter for cross-platform development. It helps you build beautiful, high-performance applications for mobile, web, and desktop from a single codebase.

**When to use this skill:**
- Cross-platform with high performance
- Custom UI requirements
- Consistent design across platforms
- Dart programming

**Key strengths:**
- Deep Flutter knowledge
- Experience with widget patterns
- Understanding of rendering

---

### Flutter Development Prompts

#### Building Flutter Application

**Context:** You're building a cross-platform app with Flutter.

```text
@flutter-expert Design a Flutter application architecture:

Application:
- Social fitness app
- Activity tracking
- Social feed with photos
- Chat functionality
- GPS and sensor integration
- Push notifications

Requirements:
- Flutter 3.x with null safety
- Material Design 3
- State management (Riverpod/Bloc)
- API integration with Dio
- Local storage with Hive/Isar
- Platform channel for native

Quality requirements:
- Smooth 60fps performance
- Responsive layout
- Accessibility support
- Dark mode

Please provide:
1. Project structure
2. State management architecture
3. Widget organization
4. Navigation approach
5. API and caching strategy
6. Native integration patterns
7. Testing strategy
8. Build and deployment
```

**Expected Output:** Flutter application architecture.

---

## 35.3 iOS Development with @ios-expert

### Skill Introduction

The `@ios-expert` skill provides expertise in native iOS development with Swift and SwiftUI. It helps you build polished, performant iOS applications that fully leverage Apple's platform.

**When to use this skill:**
- Native iOS applications
- SwiftUI and UIKit
- Apple ecosystem integration
- Performance-critical apps

**Key strengths:**
- Deep iOS and Swift knowledge
- Experience with Apple frameworks
- Understanding of App Store guidelines

---

### iOS Development Prompts

#### Building iOS Application

**Context:** You're building a native iOS app with SwiftUI.

```text
@ios-expert Design a SwiftUI iOS application:

Application:
- Finance tracking app
- Bank account sync (Plaid)
- Transaction categorization
- Budget tracking
- Charts and reports
- Widget for home screen

Requirements:
- SwiftUI for UI
- Combine for reactive programming
- Core Data for persistence
- Swift Concurrency (async/await)
- Widget extension
- Local notifications

Quality requirements:
- iOS design guidelines
- Accessibility (VoiceOver ready)
- Privacy-focused architecture
- Fast app launch

Please provide:
1. Project structure
2. SwiftUI architecture (MVVM/TCA)
3. Data layer design
4. Navigation patterns
5. Network layer with async/await
6. Widget implementation
7. Testing approach
8. App Store submission prep
```

**Expected Output:** iOS application architecture.

---

## 35.4 Android Development with @android-expert

### Skill Introduction

The `@android-expert` skill provides expertise in native Android development with Kotlin and Jetpack. It helps you build robust Android applications following modern best practices.

**When to use this skill:**
- Native Android applications
- Jetpack Compose UI
- Android ecosystem integration
- Background processing

**Key strengths:**
- Deep Android knowledge
- Experience with Jetpack libraries
- Understanding of Android lifecycle

---

### Android Development Prompts

#### Building Android Application

**Context:** You're building a native Android app with Jetpack Compose.

```text
@android-expert Design a Jetpack Compose Android application:

Application:
- Task management app
- Task creation and management
- Due date reminders
- Recurring tasks
- Categories and tags
- Widgets and notifications

Requirements:
- Jetpack Compose for UI
- Kotlin with Coroutines
- Room for database
- Hilt for dependency injection
- WorkManager for background
- Material Design 3

Quality requirements:
- Adaptive layouts (phone/tablet)
- Dark theme support
- Offline-first architecture
- Battery efficient

Please provide:
1. Project structure
2. Clean architecture with Compose
3. State management
4. Navigation with Compose
5. Database and sync strategy
6. Background work patterns
7. Testing strategy
8. Play Store preparation
```

**Expected Output:** Android application architecture.

---

## Best Practices Summary

### Architecture
1. **Clean Architecture:** Separate concerns
2. **Unidirectional Data Flow:** Predictable state
3. **Repository Pattern:** Abstract data sources
4. **Dependency Injection:** Testable code
5. **Navigation:** Clear navigation patterns

### Performance
1. **Lazy Loading:** Load screens on demand
2. **Image Caching:** Efficient memory use
3. **List Optimization:** Recycle views
4. **Startup Time:** Fast initial load
5. **Battery:** Minimize background work

### User Experience
1. **Platform Guidelines:** Follow iOS/Android conventions
2. **Responsive:** Handle all screen sizes
3. **Offline:** Graceful offline handling
4. **Accessibility:** Screen reader support
5. **Deep Linking:** Support app links

---

## Reflection Points

1. **Native vs Cross-Platform:** How do you decide?
2. **Code Sharing:** What level of sharing is optimal?
3. **Platform Features:** When do platform-specific features matter?
4. **Team Skills:** How does team expertise affect the decision?

---

**Next Chapter:** [Chapter 36: Documentation →](chapter-36-documentation.md)
