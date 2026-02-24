# 📱 Video Sharing Platform

<div align="center">
  <p align="center">
    <b>A video sharing platform built with React Native, Expo, and Appwrite.</b><br />
  </p>
</div>

---

## 🚀 Overview

This is a modern, full-stack video sharing mobile application built with **React Native**, **Expo**, and **Appwrite**. It features a sleek design, seamless video playback, and a robust backend for user authentication and content management.

### ✨ Key Features

- 🔐 **Secure Authentication**: User sign-up, sign-in, and persistence using Appwrite.
- 📺 **Video Feed**: Home screen featuring latest and trending videos.
- 🔍 **Global Search**: Find videos quickly with a dedicated search interface.
- ⬆️ **Video Uploads**: Users can upload their own videos and thumbnails.
- 👤 **User Profiles**: Personal profile pages showing user-specific content.
- 🎨 **Modern UI/UX**: Beautifully designed interface with smooth animations and transitions using NativeWind and React Native Animatable.
- 📱 **Responsive Design**: Consistent experience across different screen sizes.

---

## 🛠️ Tech Stack

- **Frontend**: [React Native](https://reactnative.dev/) (Expo)
- **Styling**: [NativeWind](https://www.nativewind.dev/) (Tailwind CSS for React Native)
- **Backend**: [Appwrite](https://appwrite.io/) (Authentication, Database, Storage)
- **Routing**: [Expo Router](https://docs.expo.dev/router/introduction/) (File-based routing)
- **Animations**: [React Native Animatable](https://github.com/oblador/react-native-animatable)
- **Video Playback**: [Expo AV](https://docs.expo.dev/versions/latest/sdk/av/)
- **Icons/Images**: [Lucide React Native](https://lucide.dev/), Custom Assets

---

## 🏗️ Project Structure

```text
├── app/                  # Main application screens (Expo Router)
│   ├── (auth)/           # Authentication screens (Sign In, Sign Up)
│   ├── (tabs)/           # Main tab navigation (Home, Create, Profile, Bookmark)
│   ├── search/           # Search functionality
│   ├── _layout.jsx       # Root layout configuration
│   └── index.jsx         # Onboarding/Landing screen
├── assets/               # Static assets (images, icons, fonts)
├── components/           # Reusable UI components
│   ├── CustomButton.jsx
│   ├── EmptyState.jsx
│   ├── FormField.jsx
│   └── ...
├── constants/            # Application constants and theme configuration
├── context/              # Global state management (Context API)
├── lib/                  # Backend logic and API integrations (Appwrite)
│   ├── appwrite.js       # Appwrite client and services
│   └── useAppwrite.js    # Custom hook for fetching data
└── tailwind.config.js    # NativeWind/Tailwind CSS configuration

```

---

## ⚙️ Getting Started

### Prerequisites

- **Node.js** (v18 or higher)
- **npm** or **yarn**
- **Expo Go** app on your mobile device (to test on physical hardware)
- **Appwrite Account**: You'll need an Appwrite project set up.

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/zaykhere/rn-vid-share.git
   cd rn-vid-share
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Environment Setup:**
   Create a `.env` file in the root directory and add your Appwrite credentials:
   ```env
   EXPO_PUBLIC_APPWRITE_ENDPOINT="https://cloud.appwrite.io/v1"
   EXPO_PUBLIC_APPWRITE_PROJECT_ID="your_project_id"
   EXPO_PUBLIC_DB_ID="your_database_id"
   EXPO_PUBLIC_AORA_BUCKET="your_storage_bucket_id"
   ```

4. **Run the application:**
   ```bash
   npx expo start
   ```
   Scan the QR code with **Expo Go** (Android) or the **Camera App** (iOS) to run the app.

---

## 🛠️ Appwrite Configuration

Ensure your Appwrite project has the following:
- **Database**: Create a database and two collections:
  - `users`: With attributes `accountId`, `email`, `username`, `avatar`.
  - `videos`: With attributes `title`, `thumbnail`, `video`, `prompt`, `creator` (relationship with `users`).
- **Storage**: Create a bucket for video and image uploads.
- **Platform**: Add a mobile platform with the bundle ID `com.zain.aora`.

---

## 🤝 Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` (if exists) for more information.

---

<p align="center">Made with ❤️ by <a href="https://github.com/zaykhere">Zain</a></p>
