# Kurikulum Pembelajaran React Native: Dari Basic Hingga Expert

## Timeline Pembelajaran

| Level | Durasi | Modul |
|-------|--------|-------|
| **Pemula** | 4 minggu | Modul 1-4 |
| **Menengah** | 6 minggu | Modul 5-9 |
| **Lanjutan** | 8 minggu | Modul 10-15 |
| **Expert** | 6 minggu | Modul 16-19 |

**Total Program**: 24 minggu (6 bulan)

---

## Modul 1: Pengenalan & Persiapan (1 minggu)
### Topik:
1. **Pengenalan React Native**
   - Apa itu React Native?
   - Sejarah dan perkembangan React Native
   - Keunggulan dan keterbatasan React Native
   - Perbandingan dengan framework mobile lainnya (Flutter, Ionic, Native)

2. **Menyiapkan Lingkungan Pengembangan**
   - Instalasi Node.js dan npm/yarn
   - Menyiapkan Expo CLI vs React Native CLI
   - Konfigurasi Emulator (Android & iOS)
   - Konfigurasi Editor (VSCode + extensions)
   - Debugging tools & teknik dasar

3. **Project Pertama**
   - Membuat aplikasi pertama dengan "Hello World"
   - Memahami struktur project React Native
   - Menjalankan aplikasi di emulator dan device fisik
   - Hot Reloading & Live Reload

### Proyek Minggu 1:
- Membuat aplikasi "Profil Saya" sederhana dengan informasi pribadi dan foto

---

## Modul 2: Fundamental JavaScript & React (1 minggu)
### Topik:
1. **JavaScript Modern untuk React Native**
   - ES6+ syntax (arrow functions, destructuring, spread operator)
   - Array methods (map, filter, reduce)
   - Promises & Async/Await
   - Modules (import/export)

2. **Konsep Dasar React**
   - JSX & Virtual DOM
   - Components & Props
   - State & Lifecycle
   - Event Handling
   - Conditional Rendering
   - Lists & Keys

3. **Functional vs Class Components**
   - Perbandingan syntax dan penggunaan
   - Kelebihan dan kekurangan masing-masing pendekatan
   - Best practices penggunaan component

### Proyek Minggu 2:
- Membuat aplikasi To-Do List sederhana dengan operasi CRUD dasar

---

## Modul 3: Komponen UI Dasar (1 minggu)
### Topik:
1. **Core Components**
   - View, Text, Image
   - TextInput
   - Button, TouchableOpacity, Pressable
   - ScrollView & FlatList
   - SafeAreaView & StatusBar
   - ActivityIndicator

2. **Styling di React Native**
   - StyleSheet API
   - Flexbox layout
   - Responsive design
   - Colors, fonts, dan dimensi
   - Platform-specific styling

3. **Handling User Input**
   - Form components
   - Keyboard handling
   - Validasi input

### Proyek Minggu 3:
- Membuat aplikasi Kalkulator dengan UI yang responsif

---

## Modul 4: Navigasi & Routing (1 minggu)
### Topik:
1. **React Navigation**
   - Instalasi dan setup
   - Stack Navigation
   - Tab Navigation
   - Drawer Navigation
   - Parameter & Navigasi antar screen
   - Header customization

2. **Navigasi Kompleks**
   - Nested navigators
   - Authentication flows
   - Deep linking
   - Animasi transisi

3. **Manajemen Rute Lanjutan**
   - Navigation state
   - Navigation events
   - Screen options
   - Navigasi programatik

### Proyek Minggu 4:
- Aplikasi multi-screen dengan navigasi kompleks (tabs, stack, dan drawer)

---

## Modul 5: State Management (1 minggu)
### Topik:
1. **Local State Management**
   - useState hook
   - useReducer hook
   - Context API
   - Prop drilling

2. **Redux**
   - Konsep dasar (Store, Actions, Reducers)
   - Redux Toolkit
   - Middleware (Thunk, Saga)
   - Redux DevTools

3. **Alternatif State Management**
   - MobX
   - Zustand
   - Recoil
   - Jotai

### Proyek Minggu 5:
- Refactor aplikasi To-Do List dengan Redux/Context API

---

## Modul 6: Networking & API Integration (1 minggu)
### Topik:
1. **HTTP Requests**
   - Fetch API
   - Axios
   - RESTful API concepts
   - Authentication (JWT, OAuth)

2. **GraphQL di React Native**
   - Apollo Client
   - Queries dan Mutations
   - Caching & state management

3. **Handling Network State**
   - Loading states
   - Error handling
   - Offline support
   - Retrying requests

4. **Webhooks & Realtime Data**
   - WebSockets
   - Server-Sent Events
   - Firebase Realtime Database

### Proyek Minggu 6:
- Aplikasi berita yang mengambil data dari API publik

---

## Modul 7: Penyimpanan Data Lokal (1 minggu)
### Topik:
1. **Persistent Storage**
   - AsyncStorage
   - MMKV Storage
   - Realm Database
   - SQLite

2. **File System**
   - Akses penyimpanan device
   - Mengelola file dan direktori
   - Image caching

3. **Secure Storage**
   - Keychain (iOS) & Keystore (Android)
   - Encrypted storage
   - Biometric authentication

### Proyek Minggu 7:
- Aplikasi notes dengan penyimpanan lokal dan sinkronisasi ke cloud

---

## Modul 8: UI/UX Lanjutan (2 minggu)
### Topik:
1. **Animasi**
   - Animated API
   - LayoutAnimation
   - Gesture Responder System
   - Reanimated 2
   - Lottie animations

2. **Custom Components**
   - Membangun komponen reusable
   - Higher-Order Components
   - Component composition
   - Theming

3. **UI Libraries**
   - React Native Paper
   - NativeBase
   - React Native Elements
   - Tailwind for React Native

4. **Design Systems**
   - Menerapkan design system
   - Konsistensi UI/UX
   - Theming & dark mode
   - Accessibility

### Proyek Minggu 8-9:
- Aplikasi e-commerce dengan UI yang menarik, animasi, dan tema yang dapat diubah

---

## Modul 9: Testing & Debugging (1 minggu)
### Topik:
1. **Testing di React Native**
   - Jest basics
   - React Native Testing Library
   - Component testing
   - Snapshot testing
   - E2E testing dengan Detox

2. **Debugging Lanjutan**
   - Chrome DevTools
   - React DevTools
   - Flipper
   - Performance monitoring
   - Crash reporting

3. **Error Handling**
   - Error boundaries
   - Logging
   - Telemetry
   - Monitoring tools

### Proyek Minggu 9:
- Menulis test untuk aplikasi yang sudah ada sebelumnya

---

## Modul 10: Native Modules & Bridges (2 minggu)
### Topik:
1. **Pengenalan Native Modules**
   - Arsitektur bridge React Native
   - JavaScript <-> Native communication
   - Threading model

2. **Native Modules for Android**
   - Java/Kotlin fundamentals
   - Creating Android native modules
   - Callbacks & Promises
   - UI components in Android

3. **Native Modules for iOS**
   - Objective-C/Swift fundamentals
   - Creating iOS native modules
   - Callbacks & Promises
   - UI components in iOS

4. **Turbo Modules & Fabric**
   - New architecture overview
   - Migrating to the new architecture
   - Performance benefits

### Proyek Minggu 10-11:
- Mengembangkan modul native sederhana untuk Android dan iOS

---

## Modul 11: Mengintegrasikan Third-Party SDKs (1 minggu)
### Topik:
1. **Maps & Geolocation**
   - React Native Maps
   - Geolocation API
   - Geocoding & reverse geocoding
   - Map annotations & overlays

2. **Social Media Integration**
   - Authentication via social platforms
   - Sharing ke platform sosial
   - Deep linking ke apps lain

3. **Payment Gateways**
   - Stripe
   - PayPal
   - In-App Purchases
   - Google Pay & Apple Pay

4. **Analytics & Monitoring**
   - Firebase Analytics
   - Crashlytics
   - Performance monitoring
   - User behavior tracking

### Proyek Minggu 12:
- Aplikasi marketplace dengan maps, social sharing, dan integration pembayaran

---

## Modul 12: Fitur Device & APIs (1 minggu)
### Topik:
1. **Kamera & Media**
   - Akses kamera
   - Image picker
   - Audio & video recording
   - Image processing

2. **Sensors & Hardware**
   - Accelerometer & Gyroscope
   - Bluetooth
   - NFC
   - Haptic feedback

3. **Push Notifications**
   - Local notifications
   - Remote notifications
   - Notification channels
   - Background tasks

4. **Permissions**
   - Permission model
   - Requesting permissions
   - Handling denied permissions
   - Deep linking

### Proyek Minggu 13:
- Aplikasi utilitas yang menggunakan berbagai API perangkat (kamera, sensors, notifications)

---

## Modul 13: Performa & Optimisasi (2 minggu)
### Topik:
1. **Performance Profiling**
   - Mengidentifikasi bottlenecks
   - Memory leaks
   - Frame drops
   - Profiling tools

2. **Rendering Optimisasi**
   - Component memoization
   - Pure components
   - List optimization (FlatList, SectionList)
   - Lazy loading & virtualization

3. **Memory Management**
   - Garbage collection
   - Image optimization
   - Asset management
   - Bundle splitting

4. **Bundle Size Optimisasi**
   - Code splitting
   - Tree shaking
   - Dynamic imports
   - Hermes engine

### Proyek Minggu 14-15:
- Audit dan optimisasi aplikasi yang sudah ada untuk meningkatkan kinerja

---

## Modul 14: Aksesibilitas & Internasionalisasi (1 minggu)
### Topik:
1. **Aksesibilitas**
   - Accessibility API
   - Screen readers support
   - Navigasi keyboard
   - Contrast & scaling
   - Testing aksesibilitas

2. **Internasionalisasi & Lokalisasi**
   - i18n libraries
   - RTL support
   - String localization
   - Date, time, & number formatting
   - Multi-language support

3. **Compliance & Standards**
   - WCAG guidelines
   - Mobile accessibility best practices
   - Regional compliance requirements

### Proyek Minggu 16:
- Meningkatkan aksesibilitas dan menambahkan dukungan multi-bahasa ke aplikasi yang sudah ada

---

## Modul 15: Deployment & Publishing (1 minggu)
### Topik:
1. **App Building & Bundling**
   - Release configuration
   - App signing
   - Generating bundles/APKs/IPAs
   - Code Push & OTA updates

2. **App Store Submission**
   - App Store guidelines
   - App Store Connect
   - Submission process
   - TestFlight

3. **Google Play Submission**
   - Google Play Console
   - Play Store guidelines
   - Submission process
   - Internal/Alpha/Beta testing

4. **CI/CD for React Native**
   - GitHub Actions
   - Bitrise
   - Fastlane
   - Automated testing & deployment

### Proyek Minggu 17:
- Menyiapkan pipeline CI/CD dan mempublikasikan aplikasi ke stores (atau simulasi)

---

## Modul 16: Arsitektur Aplikasi (2 minggu)
### Topik:
1. **Arsitektur Patterns**
   - MVC, MVVM, dan MVP patterns
   - Flux architecture
   - Clean Architecture
   - Domain-Driven Design

2. **Project Structure**
   - Feature-based organization
   - Atomic Design
   - Module design
   - Monorepo vs multi-repo

3. **Code Quality**
   - Linting & code formatting
   - Static type checking (TypeScript)
   - Code reviews
   - Documentation

4. **Design Patterns**
   - Compound components
   - Render props
   - Custom hooks
   - Provider pattern

### Proyek Minggu 18-19:
- Refactoring aplikasi menggunakan arsitektur yang lebih baik dan clean code

---

## Modul 17: React Native di Production (2 minggu)
### Topik:
1. **Scaling React Native**
   - Large team organization
   - Modular architecture
   - Feature flagging
   - A/B testing

2. **DevOps for Mobile**
   - Infrastructure as Code
   - Monitoring & alerting
   - Disaster recovery
   - Security best practices

3. **Performance Monitoring**
   - APM tools
   - Analytics integration
   - User feedback collection
   - Production debugging

4. **Maintenance & Updates**
   - Dependency management
   - Upgrading React Native
   - Long-term support
   - Technical debt management

### Proyek Minggu 20-21:
- Menyiapkan infrastruktur monitoring, logging, dan sistem deployment untuk aplikasi production

---

## Modul 18: Advanced Cross-Platform Development (1 minggu)
### Topik:
1. **Code Sharing Strategies**
   - React Native Web
   - React Native Windows/macOS
   - Code sharing dengan web apps
   - Monorepo structure

2. **Cross-Platform Challenges**
   - Platform differences
   - Platform-specific optimizations
   - Shared abstractions
   - Feature parity

3. **Web-to-Mobile Migration**
   - Migrating web React apps to mobile
   - Sharing logic between platforms
   - Creating platform adapters

### Proyek Minggu 22:
- Mengembangkan aplikasi cross-platform yang berjalan di mobile dan web

---

## Modul 19: Proyek Capstone (1 minggu)
### Topik:
1. **Final Project Requirements**
   - Definisi scope proyek
   - Technical requirements
   - Desain arsitektur
   - Timeline & milestones

2. **Implementation**
   - Full-stack integration
   - Advanced UI/UX
   - Multiple native integrations
   - Performance optimization

3. **Presentasi & Review**
   - Code review
   - Performance audit
   - Security audit
   - UX evaluation

### Proyek Minggu 23-24:
- Mengembangkan aplikasi produksi lengkap yang mendemonstrasikan semua keterampilan yang dipelajari

---

## Sumber Belajar Tambahan

### Dokumentasi & Referensi
- [React Native Official Documentation](https://reactnative.dev/docs/getting-started)
- [React Navigation Documentation](https://reactnavigation.org/docs/getting-started)
- [Expo Documentation](https://docs.expo.dev/)

### Kursus Online
- React Native - The Practical Guide (Udemy)
- CS50's Mobile App Development with React Native (Harvard)
- The Complete React Native + Hooks Course (Udemy)

### Buku
- Learning React Native (O'Reilly)
- React Native in Action (Manning)
- Fullstack React Native (Fullstack.io)

### Komunitas & Forum
- React Native Community (GitHub)
- React Native Radio (Podcast)
- Reactiflux Discord Community
- r/reactnative Subreddit

---

## Tips Untuk Sukses Belajar

1. **Konsistensi lebih penting dari intensitas** - Tetapkan jadwal belajar harian dan pertahankan
2. **Learning by doing** - Selalu praktek dengan proyek nyata, bukan hanya tutorial
3. **Bergabung dengan komunitas** - Ajukan pertanyaan, bagikan pengetahuan, dan dapatkan feedback
4. **Lakukan code review** - Bangun kebiasaan mereview kode Anda sendiri dan orang lain
5. **Gunakan sumber terbuka** - Pelajari dari proyek open source React Native yang ada
6. **Dokumentasikan perjalanan Anda** - Menulis blog atau catatan tentang apa yang Anda pelajari
7. **Berkolaborasi** - Cari partner belajar atau bergabung dengan project kolaboratif

---

## Metode Evaluasi

### Untuk setiap modul:
1. **Quiz** - Evaluasi pemahaman konsep dasar
2. **Proyek Praktis** - Menerapkan pengetahuan dalam proyek nyata
3. **Peer Review** - Dapatkan feedback dari sesama peserta
4. **Refleksi Diri** - Dokumentasikan tantangan, solusi, dan pembelajaran

### Evaluasi Akhir:
1. **Proyek Capstone** - Aplikasi produksi lengkap yang menggabungkan semua yang dipelajari
2. **Technical Interview Simulation** - Latihan interview teknis dengan reviewer berpengalaman
3. **Portfolio Review** - Evaluasi komprehensif dari semua proyek yang telah diselesaikan

---

*Kurikulum ini dirancang untuk memberikan jalur pembelajaran komprehensif dari dasar hingga tingkat ahli dalam pengembangan aplikasi dengan React Native. Setiap modul berfokus pada keterampilan spesifik dengan proyek praktis untuk memperkuat pembelajaran.*
