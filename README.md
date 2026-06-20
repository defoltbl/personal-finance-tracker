# Task-Money-Help-Manager

![Platform](https://img.shields.io/badge/platform-Android-3DDC84?logo=android&logoColor=white)
![Language](https://img.shields.io/badge/language-Kotlin-7F52FF?logo=kotlin&logoColor=white)
![Backend](https://img.shields.io/badge/backend-Firebase-FFCA28?logo=firebase&logoColor=white)
![Min SDK](https://img.shields.io/badge/min%20SDK-Android%208.0-blue)

A personal finance management app for Android that helps you track income and expenses, visualize spending trends, and stay on top of your budget — all from your phone.

[**Download APK**](https://github.com/AndreyMaksimenko/Task-Money-Help-Manager/blob/master/app-debug.apk)

---

## Overview

Task-Money-Help-Manager is a native Android application for everyday personal finance tracking. It lets users log income and expense transactions, review their financial history over any time period, and visualize the balance between money earned and money spent through built-in charts. The app was built with a focus on a clean, intuitive interface so that recording a transaction takes only a few taps.

## Features

**Account & Authentication**
- Registration and login with email and password
- Sign in with Google
- Email-based account confirmation
- Password recovery
- Sign out
- Custom profile picture

**Transaction Management**
- Add new income or expense entries (amount, category, date, description)
- Edit existing entries
- Delete entries you no longer need
- Sort transactions by date, type, or other criteria

**Insights**
- View income and expenses for any selected period
- Visual charts comparing expenses against income received
- Tabbed navigation between the account view and the transactions view

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Kotlin |
| Backend / Database | Firebase (Realtime Database, Authentication, Storage) |
| Authentication | Firebase Auth (email/password, Google OAuth 2.0) |
| Architecture | Android Architecture Components (MVVM — ViewModel, LiveData) |
| Navigation | Bottom chip-style navigation bar |
| Platform | Android, minimum SDK level corresponding to Android 8.0 (Oreo) |

## Architecture

The app follows an **MVVM (Model–View–ViewModel)** approach using Android's official architecture components, which keeps business logic separate from the UI layer and makes the codebase easier to test and maintain.

**Key components:**
- `AccountFragment.kt` — handles account-related UI (registration, login, profile)
- `TransactionFragment.kt` — handles the transaction list (adding, editing entries)
- `MainActivity.kt` — the app's main entry point
- `Login.kt` / `SignUp.kt` — authentication flows, including input validation
- `ForgotPassword.kt` — password recovery flow
- `InsertionActivity.kt` — adding new transactions
- `TransactionDetails.kt` — viewing, editing, and deleting a specific transaction
- `TransactionAdapter.kt` — binds transaction data to list views
- `TransactionModel.kt` — data model for a transaction

Data is persisted and synced through **Firebase**, which also handles user authentication and file storage for profile pictures, removing the need for a custom backend.

## Requirements

**Functional**
- Add, edit, delete, and sort financial transactions
- Sync transaction data to a user account for access across devices
- Add a custom profile picture

**Non-functional**
- Android 8.0 or later
- ARM or x86 compatible processor
- At least 1 GB of RAM recommended for smooth operation
- Active internet connection required for sync, backup, and authentication

## Getting Started

### Prerequisites
- [Android Studio](https://developer.android.com/studio)
- A Firebase project with Authentication and Realtime Database enabled
- Your own `google-services.json` added to the `app/` module

### Installation

```bash
git clone https://github.com/AndreyMaksimenko/Task-Money-Help-Manager.git
```

1. Open the project in Android Studio.
2. Add your `google-services.json` file to the `app/` directory.
3. Sync Gradle and build the project.
4. Run on an emulator or physical device (Android 8.0+).

Alternatively, install the pre-built APK directly: [Download APK](https://github.com/AndreyMaksimenko/Task-Money-Help-Manager/blob/master/app-debug.apk).

## Testing

The application underwent functional testing across its core features (registration, login, transaction CRUD operations, sorting, and synchronization) to verify that actual behavior matched the defined requirements. All test cases passed successfully.

## Developed by

**Maksymenko Andrii**
