# iManager - Sports Team Management App

<div align="center">
  <img src="assets/logo.png" alt="iManager Logo" width="200" height="200">
  
  [![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev/)
  [![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev/)
  [![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)](https://firebase.google.com/)
  [![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
  
  **A comprehensive mobile application for sports team management, communication, and organization**
</div>

## 📱 Screenshots

<div align="center">
  <img src="docs/screenshots/dashboard.png" alt="Dashboard" width="200">
  <img src="docs/screenshots/chat.png" alt="Chat" width="200">
  <img src="docs/screenshots/events.png" alt="Events" width="200">
  <img src="docs/screenshots/reports.png" alt="Reports" width="200">
  <img src="docs/screenshots/tactics.png" alt="Tactics Board" width="200">
</div>

## 🎯 Overview

iManager is a comprehensive mobile application designed to streamline sports team management, communication, and organization. It serves as an all-in-one platform for coaches, staff, and players to collaborate effectively and stay organized.

### 🌟 Key Features

- **💬 Real-time Communication**: One-to-one and group chat with voice notes and media sharing
- **📅 Event Management**: Create, schedule, and manage team events with approval workflows
- **📢 Notices & Announcements**: Share updates with specific teams or roles with acknowledgment tracking
- **📊 Daily Logs**: Track wellness metrics including sleep, stress, and health indicators
- **📋 Reports System**: Comprehensive diet plans and medical reports with interactive body mapping
- **⚽ Tactics Board**: Interactive drawing tool for creating and replaying tactical plays
- **🏆 Match Management**: Browse leagues, teams, and player statistics
- **🔔 Push Notifications**: Real-time notifications to keep everyone informed
- **📞 Audio/Video Calls**: Integrated calling system with call history
- **👥 Role-based Access**: Support for coaches, players, managers, and support staff

## 🏗️ Architecture

<div align="center">
  <img src="docs/architecture/app_architecture.png" alt="App Architecture" width="600">
</div>

### Frontend (Flutter)
- **Framework**: Flutter 3.x with Dart
- **State Management**: Provider pattern
- **UI Components**: Custom widgets with Material Design
- **Real-time Communication**: Socket.IO integration
- **Media Handling**: Image/video upload and caching
- **Maps Integration**: Google Maps for location services

### Backend (Node.js)
- **Runtime**: Node.js with TypeScript
- **Database**: MongoDB with Mongoose ODM
- **Real-time**: Socket.IO for live communication
- **Authentication**: JWT with Firebase Admin SDK
- **File Storage**: Firebase Storage
- **Caching**: Redis for session management

## 🚀 Getting Started

### Prerequisites

- Flutter SDK (3.0 or higher)
- Dart SDK (3.0 or higher)
- Node.js (18.x or higher)
- MongoDB instance
- Redis server
- Firebase project setup

### Installation

#### Frontend Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/rchhabra13/imanager_app.git
   cd imanager_app
   ```

2. **Install Flutter dependencies**
   ```bash
   flutter pub get
   ```

3. **Configure Firebase**
   - Add your `google-services.json` (Android) and `GoogleService-Info.plist` (iOS)
   - Update Firebase configuration in `lib/firebase_options.dart`

4. **Update API endpoints**
   - Modify `lib/NetworkApi/Const.dart` with your backend URL

5. **Run the application**
   ```bash
   flutter run
   ```

#### Backend Setup

1. **Navigate to backend directory**
   ```bash
   cd imanager_backend
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

4. **Start the development server**
   ```bash
   npm run dev
   ```

## 📁 Project Structure

```
imanager_app/
├── lib/
│   ├── Models/                 # Data models
│   ├── NetworkApi/            # API communication layer
│   ├── Providers/             # State management
│   ├── Screens/               # UI screens
│   │   ├── Authentication/    # Login/Register screens
│   │   ├── Chat/             # Chat functionality
│   │   ├── Events/           # Event management
│   │   ├── Reports/          # Medical & diet reports
│   │   ├── Settings/         # App settings
│   │   └── TacticBoard/      # Tactics board
│   └── utilities/            # Helper functions & widgets
├── assets/                   # Images, fonts, icons
├── android/                  # Android-specific files
├── ios/                      # iOS-specific files
└── imanager_backend/         # Backend API server
    ├── src/
    │   ├── modules/          # Feature modules
    │   ├── middlewares/      # Express middlewares
    │   ├── services/         # Business logic
    │   └── types/           # TypeScript types
    └── dist/                # Compiled JavaScript
```

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the backend directory:

```env
# Server Configuration
PORT=8080
NODE_ENV=development

# Database
MONGO_URI=mongodb://localhost:27017/imanager

# Authentication
JWT_SECRET=your_jwt_secret_here

# Firebase
FIREBASE_PROJECT_ID=your_project_id
FIREBASE_PRIVATE_KEY=your_private_key
FIREBASE_CLIENT_EMAIL=your_client_email

# Storage
STORAGE_BUCKET=gs://your-bucket.appspot.com

# External Services
NUTRITIONIX_APP_ID=your_app_id
NUTRITIONIX_API_KEY=your_api_key
```

### Firebase Setup

1. Create a Firebase project
2. Enable Authentication, Firestore, and Storage
3. Download configuration files
4. Update the app with your Firebase credentials

## 🎨 UI/UX Features

<div align="center">
  <img src="docs/ui/design_system.png" alt="Design System" width="400">
</div>

- **Modern Material Design**: Clean, intuitive interface
- **Dark/Light Theme**: Adaptive theming support
- **Responsive Layout**: Optimized for various screen sizes
- **Accessibility**: WCAG compliant components
- **Custom Animations**: Smooth transitions and micro-interactions

## 🔐 Security Features

- **JWT Authentication**: Secure token-based authentication
- **Role-based Access Control**: Granular permissions system
- **Data Encryption**: End-to-end encryption for sensitive data
- **Input Validation**: Comprehensive input sanitization
- **Rate Limiting**: API rate limiting to prevent abuse

## 📊 Performance Optimizations

- **Image Caching**: Efficient image loading and caching
- **Lazy Loading**: On-demand content loading
- **State Management**: Optimized state updates
- **Memory Management**: Proper resource cleanup
- **Network Optimization**: Request deduplication and caching

## 🧪 Testing

```bash
# Run Flutter tests
flutter test

# Run backend tests
cd imanager_backend
npm test

# Run integration tests
flutter drive --target=test_driver/app.dart
```

## 📱 Supported Platforms

- **Android**: API level 21+ (Android 5.0+)
- **iOS**: iOS 11.0+
- **Web**: Chrome, Firefox, Safari (limited features)

## 🚀 Deployment

### Frontend Deployment

#### Android
```bash
flutter build apk --release
# or
flutter build appbundle --release
```

#### iOS
```bash
flutter build ios --release
```

### Backend Deployment

```bash
# Build the project
npm run build

# Start production server
npm start
```

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines

- Follow Flutter/Dart style guidelines
- Write comprehensive tests
- Update documentation
- Ensure all tests pass
- Follow semantic versioning

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Team

<div align="center">
  <img src="docs/team/team_photo.png" alt="Development Team" width="400">
</div>

- **Lead Developer**: Rishi Chhabra
- **UI/UX Design**: [Design Team]
- **Backend Development**: [Backend Team]
- **QA Testing**: [QA Team]

## 📞 Support & Contact

For support, questions, or feature requests:

- **Email**: [Rishi.chhabra@outlook.com](mailto:Rishi.chhabra@outlook.com)
- **Issues**: [GitHub Issues](https://github.com/rchhabra13/imanager_app/issues)
- **Documentation**: [Wiki](https://github.com/rchhabra13/imanager_app/wiki)

## 🙏 Acknowledgments

- Flutter team for the amazing framework
- Firebase for backend services
- Open source community for various packages
- Beta testers and early adopters

## 📈 Roadmap

### Upcoming Features
- [ ] Advanced analytics dashboard
- [ ] Video call recording
- [ ] Offline mode support
- [ ] Multi-language support
- [ ] Advanced reporting tools
- [ ] Integration with wearable devices

### Version History
- **v1.0.0** - Initial release with core features
- **v1.1.0** - Enhanced chat and notifications
- **v1.2.0** - Improved reports and body mapping
- **v2.0.0** - Major UI overhaul and performance improvements

---

<div align="center">
  <p>Made with ❤️ for sports teams worldwide</p>
  <p>⭐ Star this repository if you find it helpful!</p>
</div>