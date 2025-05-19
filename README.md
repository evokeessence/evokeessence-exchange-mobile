# CryptoEvokeExchange Mobile App

A mobile application version of the CryptoEvokeExchange cryptocurrency trading platform for EvokeEssence s.r.o, connecting to the existing server infrastructure.

## Overview

This repository contains the mobile app codebase (React Native) for the CryptoEvokeExchange cryptocurrency platform. The mobile app connects to the existing backend server via a set of API endpoints and WebSocket connections for real-time data.

## Features

- **Secure Authentication**: Multi-factor authentication with mobile-specific session handling
- **Real-time Price Data**: WebSocket connections for live cryptocurrency price updates
- **Push Notifications**: Transaction alerts, price alerts, and security notifications 
- **Wallet Management**: View and manage cryptocurrency balances
- **Trading Interface**: Execute trades directly from your mobile device
- **Referral System**: Track referrals and commissions through the mobile interface
- **KYC Integration**: Complete verification processes on mobile

## Project Structure

- `/mobile` - React Native mobile application
  - `/src` - Source code for the mobile app
    - `/api` - API client for interacting with the backend
    - `/components` - Reusable UI components
    - `/screens` - Application screens
    - `/navigation` - Navigation configuration
    - `/services` - Business logic and services
    - `/hooks` - Custom React hooks
    - `/config` - App configuration
    - `/assets` - Images and other static assets (not included in this repository)

- `/docs` - Documentation for mobile app integration
  - `ios-app-integration-guide.md` - Guide for integrating iOS apps
  - `ios-push-notification-guide.md` - Guide for setting up push notifications

## Getting Started

### Prerequisites

- Node.js 18+ and npm
- React Native development environment
- iOS: XCode 13+
- Android: Android Studio, JDK 11+

### Installation

1. Clone this repository
   ```
   git clone https://github.com/yourusername/evokeessence-exchange-mobile.git
   cd evokeessence-exchange-mobile
   ```

2. Install dependencies
   ```
   cd mobile
   npm install
   ```

3. Create a `.env` file with the following environment variables:
   ```
   API_BASE_URL=https://api.evokeexchange.com
   WS_URL=wss://api.evokeexchange.com/ws
   ```

4. Install pods (iOS)
   ```
   cd ios && pod install && cd ..
   ```

5. Run the app
   ```
   # For iOS
   npx react-native run-ios
   
   # For Android
   npx react-native run-android
   ```

## API Integration

The mobile app connects to the CryptoEvokeExchange API. See the [iOS App Integration Guide](docs/ios-app-integration-guide.md) for detailed information on how the mobile app integrates with the backend services.

## Push Notifications

The app uses Firebase Cloud Messaging (FCM) for Android and Apple Push Notification service (APNs) for iOS. See the [Push Notification Guide](docs/ios-push-notification-guide.md) for setup instructions.

## Security Features

- **Certificate Pinning**: Prevents man-in-the-middle attacks by validating server certificates
- **Secure Storage**: Sensitive data is stored using encrypted secure storage
- **Biometric Authentication**: Support for fingerprint and face ID authentication
- **Session Management**: Proper handling of authentication tokens and sessions
- **Device Registration**: Secure device registration and verification

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

EvokeEssence s.r.o - contact@evokeessence.com