# LifestylePass

LifestylePass is a mobile-first platform for discovering local venues, activities, and managing verified check-ins using QR codes.

## Public vs Private Repo Strategy

This public repository is intended as a **portfolio / demo version**. Please contact me for source code or details.

https://github.com/user-attachments/assets/b0c02fcd-eaab-4949-b019-db87d820b703

Built with:
- Expo + React Native (mobile app)
- Laravel + Sanctum (API backend)
- MySQL (database)

The app allows users to:
- Browse venues on a map
- Filter venues by city and activity category
- View upcoming activities

- Check in at venues using QR codes
- View and re-verify recent check-ins
- Manage their profile and subscription plan

---

## Features

- 📍 Interactive venue map with filters
- 🏃 Activities by category and date
- 📱 QR-based venue check-ins
- ✅ Check-in confirmation & proof screen
- 🕒 Recent check-in status (time-limited)
- 👤 User profiles & plans
- 🔐 Secure authentication with Sanctum

---

## Tech Stack

### Mobile App
- Expo (React Native)
- expo-router
- expo-camera
- AsyncStorage
- React Native Maps

### Backend
- Laravel
- Laravel Sanctum
- MySQL
- REST API

---

## Getting Started

### Backend (Laravel)

1. Install dependencies:
    composer install

2. Configure environment:
    cp .env.example .env
    php artisan key:generate

3. Update `.env` with your database credentials.

4. Run migrations and seeders:
    php artisan migrate --seed

5. Start the server:
    php artisan serve

The API will run at:
    http://127.0.0.1:8000/api

---

### Mobile App (Expo)

1. Install dependencies:
    npm install

2. Set API base URL:
    Update `API_BASE_URL` in `mobile/config/api.ts`

3. Start Expo:
    npx expo start

4. Open the app using:
    - Expo Go (iOS / Android)
    - Android emulator
    - iOS simulator

Note:
QR scanning requires a real device.

---

## Check-in Flow

1. User scans a venue QR code
2. App sends a POST request to `/checkins`
3. Backend creates a check-in record
4. App displays a confirmation screen
5. Last check-in is stored locally for re-verification
6. Check-in proof expires after a short time window (configurable)

---

## Roadmap Ideas

- Venue admin dashboard
- Time-limited QR codes
- Offline check-in verification
- Apple Wallet / Google Wallet check-in passes
- Paid subscriptions
- Push notifications

---

## License

This project is provided for demonstration and portfolio purposes.
All rights reserved.
