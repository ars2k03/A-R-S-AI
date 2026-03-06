<div align="center">

# 🤖 ARS AI — Intelligent Chatbot App

<img src="images/logo.png" alt="ARS AI Logo" width="120" height="120" style="border-radius: 20px"/>

**A powerful AI-powered chatbot application built with Flutter**

[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![Firebase](https://img.shields.io/badge/Firebase-Enabled-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)](https://firebase.google.com)
[![AI Powered](https://img.shields.io/badge/AI-Powered-blueviolet?style=for-the-badge)]()
[![Dart](https://img.shields.io/badge/Dart-3.x-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev)
[![License](https://img.shields.io/badge/License-Proprietary-red?style=for-the-badge)](./LICENSE)

[![Download APK](https://img.shields.io/badge/⬇️%20Download%20APK-Latest%20Release-brightgreen?style=for-the-badge)]([https://github.com/your-username/ars-ai/releases/latest](https://github.com/ars2k03/A-R-S-AI/releases/tag/v1.0.2303009)

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
| 🌍 | **Language Settings** | Language selection screen |
| 💎 | **Premium Screen** | Premium upgrade page UI |
| 🗑️ | **Delete Account** | Full account and all associated data deletion |
| 🚪 | **Sign Out** | Clean sign-out from both Firebase and Google |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| 📱 **Framework** | Flutter (Dart) |
| 🔥 **Backend / Database** | Firebase Firestore, Firebase Auth, Firebase Storage |
| 🔐 **Authentication** | Google Sign-In + Firebase Auth |
| 🌐 **Networking** | HTTP, EmailJS REST API |
| 📦 **State Management** | Provider |
| 💾 **Local Storage** | SharedPreferences |
| 🎨 **UI / Fonts** | Google Fonts (Inter), Font Awesome Icons |
| 🎬 **Animations** | Lottie Animations |
| 📝 **Markdown** | flutter_markdown_plus, flutter_highlight, flutter_math_fork |
| 🖼️ **Image** | image_picker |
| 📶 **Connectivity** | connectivity_plus |

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

- Theme toggled directly from the side menu
- Preference persisted across app restarts

---

## 🛡️ Privacy & Security

- 🔒 User data stored securely in **Google Firebase** with encrypted connections
- 🚫 No personal data sold to third parties
- 🗑️ Full **account & data deletion** available in-app → Menu → Delete Account
- 🛡️ Input validation & prompt injection protection built-in
- ⏱️ Rate limiting prevents automated abuse

---

## ⬇️ Download

[![Download APK](https://img.shields.io/badge/⬇️%20Download%20APK-Latest%20Release-brightgreen?style=for-the-badge)]([https://github.com/your-username/ars-ai/releases/latest](https://github.com/ars2k03/A-R-S-AI/releases/tag/v1.0.2303009)

> Requires **Android 5.0 (API 21)** or higher.

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
Copyright © 2026 ARS (Arafat Rahman Sohan). All rights reserved.
```

> ⚠️ **This project is proprietary and private.**
>
> - ❌ You may **NOT** copy, clone, or redistribute this application or any part of it
> - ❌ You may **NOT** modify, reverse-engineer, or create derivative works
> - ❌ You may **NOT** use this code for commercial or personal projects
> - ✅ You **MAY** download and use the APK for personal, non-commercial use only
>
> Unauthorized use of this source code, in whole or in part, without the express
> written permission of the owner is strictly prohibited and may result in legal action.
>
> **All rights reserved.**

---

<div align="center">

**Made with ❤️ using Flutter**

⭐ If you like this project, please give it a star!

</div>
