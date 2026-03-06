<div align="center">

# 🤖 ARS AI — Intelligent Chatbot App

<img src="images/logo.png" alt="ARS AI Logo" width="120" height="120" style="border-radius: 20px"/>

**A powerful AI-powered chatbot application built with Flutter**

[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![Firebase](https://img.shields.io/badge/Firebase-Enabled-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)](https://firebase.google.com)
[![AI Powered](https://img.shields.io/badge/AI-Powered-blueviolet?style=for-the-badge)]()
[![Dart](https://img.shields.io/badge/Dart-3.x-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev)
![License](https://img.shields.io/badge/License-Proprietary-red?style=for-the-badge)

</div>

---

## 📱 Overview

**ARS AI** is a modern, feature-rich AI chatbot application built entirely with **Flutter**. It delivers fast, intelligent conversations with a beautifully crafted UI that adapts seamlessly to both light and dark modes. Backed by **Firebase**, all your chats are saved and synced in real time across sessions — so you never lose a conversation.

> 💡 ARS AI was created by **ARS (Arafat Rahman Sohan)** — a passionate Flutter developer and tech enthusiast who loves building smart mobile applications.

---

## ✨ Features

| # | Feature | Description |
|---|---------|-------------|
| 🔐 | **Google Sign-In** | One-tap secure authentication via Firebase Auth & Google Sign-In |
| 💬 | **AI Chat** | Intelligent, streaming AI-powered conversations with word-by-word response |
| 📷 | **Image Understanding** | Send images and get detailed AI-powered descriptions & analysis |
| 🌙 | **Dark / Light / System Theme** | Fully adaptive theme with persistent preference |
| 🗂️ | **Chat History** | All conversations saved, renamed, and deleted via Firebase Firestore |
| 🌐 | **Multi-language Support** | Auto-detects and replies in the user's own language |
| 🔁 | **Streaming Responses** | Real-time word-by-word reply rendering — ChatGPT style |
| ⚡ | **Smart Response Caching** | Repeated queries are served instantly from local cache |
| 🛡️ | **Rate Limiting** | Built-in per-hour message limit to prevent abuse |
| 🧠 | **Multi-mode AI** | Switches AI model based on context: coding, math, expert, general |
| 📝 | **Markdown Rendering** | Full markdown support with code highlighting, math, and more |
| 📧 | **Contact Support** | In-app support form powered by EmailJS |
| 🔔 | **Notification Settings** | Configurable push, chat, update, sound & vibration preferences |
| ⭐ | **Rate the App** | Built-in star rating & optional feedback submission |
| ❓ | **Help & FAQ** | Searchable FAQ screen with expandable answers |
| 🔏 | **Privacy Policy** | Detailed in-app privacy policy screen |
| 📋 | **Terms & Conditions** | Full terms screen accessible from login and menu |
| 🌍 | **Language Settings** | Language selection screen (extendable) |
| 💎 | **Premium Screen** | Premium upgrade page UI |
| 🗑️ | **Delete Account** | Full account and all associated data deletion |
| 🚪 | **Sign Out** | Clean sign-out from both Firebase and Google |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| 📱 **Framework** | Flutter (Dart) `^3.11.0` |
| 🔥 **Backend / Database** | Firebase Firestore, Firebase Auth, Firebase Storage |
| 🔐 **Authentication** | Google Sign-In + Firebase Auth |
| 🌐 **Networking** | HTTP package, EmailJS REST API |
| 🧠 **AI Service** | Custom AI service with streaming SSE support |
| 📦 **State Management** | Provider |
| 💾 **Local Storage** | SharedPreferences |
| 🎨 **UI / Fonts** | Google Fonts (Inter), Font Awesome Icons |
| 🎬 **Animations** | Lottie Animations |
| 📝 **Markdown** | flutter_markdown_plus, flutter_highlight, flutter_math_fork |
| 🖼️ **Image Picker** | image_picker |
| 🔗 **URL Launcher** | url_launcher |
| 📶 **Connectivity** | connectivity_plus |
| 🔑 **Secrets** | flutter_dotenv (`.env` file) |

---

## 📂 Project Structure

```
ars_ai/
│
├── 📄 main.dart                        # App entry point, theme & Firebase setup
├── 🔥 firebase_options.dart            # Auto-generated Firebase config
├── 🌿 .env                             # API keys (never commit this!)
│
├── 📁 screens/                         # Core navigation screens
│   ├── 🎬 splash_screen.dart           # Lottie animated splash + auth routing
│   ├── 🔐 login_screen.dart            # Google Sign-In UI + Terms & Conditions link
│   ├── 💬 home_screen.dart             # Main chatbot UI (streaming, markdown, image)
│   └── 📋 menu.dart                    # Side drawer: nav, theme toggle, sign-out
│
├── 📁 page/                            # Settings & informational pages
│   ├── 🔔 notifications.dart           # Notification preferences (SharedPreferences)
│   ├── 🌍 language.dart                # Language selection screen
│   ├── 🔏 Privacy.dart                 # Privacy policy screen
│   ├── 📋 Terms.dart                   # Terms & Conditions screen
│   ├── ⭐ Rate_app.dart                 # Star rating & optional feedback
│   ├── ❓ Help_faq.dart                 # Searchable FAQ with expandable answers
│   ├── 📧 Contact_support.dart         # EmailJS-powered in-app support form
│   ├── 💎 premium.dart                 # Premium upgrade screen
│   └── 🗑️ delete_account.dart          # Permanent account & data deletion
│
├── 📁 services/                        # Business logic & API layer
│   ├── 🔐 auth_service.dart            # Firebase Auth + Google Sign-In/Out
│   └── 🤖 mistral_service.dart         # AI service: streaming, cache, rate limit
│
└── 📁 provider/                        # Global state management
    └── 🎨 theme_provider.dart          # Theme mode (light/dark/system) + persistence
```

---

## 🤖 AI Service — How It Works

The AI service is a robust, production-ready implementation with the following pipeline:

```
User Message
    │
    ▼
🛡️ Input Validation ────► Empty / too long / injection pattern check
    │
    ▼
📶 Connectivity Check ──► No internet? → Show friendly error
    │
    ▼
⏱️ Rate Limit Check ────► Max 40 messages / hour enforced
    │
    ▼
⚡ Cache Lookup ─────────► Repeated query? → Serve instantly (word-by-word)
    │
    ▼
🧠 Model Selection ──────► auto / coding / math / expert / info
    │
    ▼
🌐 Streaming API Call ───► SSE stream with up to 3 auto-retries
    │
    ▼
💬 Live UI Update ───────► Word-by-word real-time rendering
    │
    ▼
💾 Save to History + Cache
```

**🧠 AI Modes:**

| Mode | Best For |
|------|----------|
| `auto` | General conversation (default) |
| `coding` | Code generation & debugging |
| `math` | Mathematical problems & equations |
| `expert` | Complex, detailed, long-form queries |
| `info` | Quick factual lookups |

**⚙️ AI Service Highlights:**
- 📜 Token-aware conversation history trimming (max ~28,000 tokens)
- 🔄 Up to **3 automatic retries** on failure
- 💾 LRU-style response cache (max 30 entries)
- ❌ Request cancellation support mid-stream
- 🖼️ Vision support — send image + text together

---

## 🚀 Getting Started

### ✅ Prerequisites

- Flutter SDK `^3.11.0`
- Dart SDK
- Android Studio / VS Code
- A Firebase project
- Valid AI API key

---

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/ars-ai.git
cd ars-ai
```

### 2️⃣ Install Dependencies

```bash
flutter pub get
```

### 3️⃣ Firebase Setup

1. Go to [Firebase Console](https://console.firebase.google.com/) and create a project
2. Enable **Authentication** → Google Sign-In
3. Enable **Cloud Firestore**
4. Enable **Firebase Storage**
5. Download `google-services.json` → place in `android/app/`
6. Download `GoogleService-Info.plist` → place in `ios/Runner/`
7. Run FlutterFire CLI:

```bash
dart pub global activate flutterfire_cli
flutterfire configure
```

### 4️⃣ Environment Variables

Create a `.env` file in the project root:

```env
AI_API_KEY=your_ai_api_key_here
```

> ⚠️ Never commit `.env` to version control. Add it to `.gitignore`.

### 5️⃣ EmailJS Setup (Contact Support)

In `lib/page/Contact_support.dart`, replace with your EmailJS credentials:

```dart
const _kServiceId  = 'YOUR_SERVICE_ID';
const _kTemplateId = 'YOUR_TEMPLATE_ID';
const _kPublicKey  = 'YOUR_PUBLIC_KEY';
```

### 6️⃣ Run the App

```bash
# Debug mode
flutter run

# Release build (Android)
flutter build apk --release

# Release build (iOS)
flutter build ios --release
```

---

## 📸 Screens

| Splash | Login | Chat Interface | AI Modes |
|--------|-------|----------------|----------|
| ![Splash](images/2.jpeg) | ![Login](images/1.jpeg) | ![Chat](images/3.jpeg) | ![Modes](images/4.jpeg) |

---

## 🔒 Authentication Flow

```
App Launch
    │
    ▼
🎬 SplashScreen (3s Lottie Animation)
    │
    ├── ✅ User Already Logged In ──────────► 💬 HomeScreen (Chatbot)
    │
    └── ❌ Not Logged In ──► 🔐 LoginScreen
                                    │
                                    ▼
                            Google Sign-In popup
                                    │
                                    ▼
                            Firebase Auth verify
                                    │
                                    ▼
                            ✅ Welcome Snackbar
                                    │
                                    ▼
                            💬 HomeScreen (Chatbot)
```

---

## 🎨 Theme System

ARS AI supports **three theme modes** with full persistence:

| Mode | Description | Background |
|------|-------------|------------|
| ☀️ **Light** | Clean, minimal white UI | `#FFFFFF` |
| 🌙 **Dark** | Deep dark mode | `#0B141A` |
| ⚙️ **System Default** | Follows device setting | Auto |

- Theme is managed globally via `ThemeProvider` (Provider package)
- Persisted across app restarts via `SharedPreferences`
- Toggled directly from the side menu

---

## 📦 Key Dependencies

```yaml
# 🔥 Firebase
firebase_core: ^4.5.0
firebase_auth: ^6.2.0
cloud_firestore: ^6.1.3
firebase_storage: ^13.1.0

# 🔐 Auth
google_sign_in: ^6.3.0

# 📦 State & Storage
provider: ^6.1.5+1
shared_preferences: ^2.5.4
flutter_dotenv: ^6.0.0

# 🎨 UI & Animations
lottie: ^3.3.2
google_fonts: ^8.0.2
font_awesome_flutter: ^10.12.0

# 📝 Markdown & Code
flutter_markdown_plus: ^1.0.7
flutter_highlight: ^0.7.0
flutter_math_fork: ^0.7.4

# 🌐 Networking
http: ^1.6.0
connectivity_plus: ^7.0.0

# 🔧 Utilities
url_launcher: ^6.3.2
image_picker: ^1.2.1
```

---

## 🛡️ Privacy & Security

- 🔒 User data stored securely in **Google Firebase** with encrypted connections
- 🚫 No personal data sold to third parties
- 🗑️ Full **account & data deletion** available in-app → Menu → Delete Account
- 🔑 API keys stored in `.env` — never hardcoded in source
- 🛡️ Input validation & **prompt injection protection** built into AI service
- ⏱️ Rate limiting prevents automated abuse

---

## 👨‍💻 About the Creator

**ARS (Arafat Rahman Sohan)** is a passionate Flutter developer and tech enthusiast who created ARS AI. He enjoys building smart mobile applications and exploring the world of artificial intelligence.

- 💼 **LinkedIn:** [linkedin.com/in/ars2k03](https://www.linkedin.com/in/ars2k03)
- 📱 **WhatsApp:** +880-1771-259478

---

## 📞 Support

Need help? You can reach out via:

- 📧 **In-App Form:** Menu → Contact Support
- 📱 **WhatsApp:** +880-1771-259478

---

## 📄 License

```
Copyright © 2026 ARS AI. All rights reserved.
```

> ⚠️ **This project is proprietary and private.**
>
> Unauthorized copying, distribution, modification, or use of this source code,
> in whole or in part, is strictly prohibited without the express written
> permission of the owner.
>
> **All rights reserved.**

---

<div align="center">

**Made with ❤️ using Flutter**

⭐ If you like this project, please give it a star!

</div>
