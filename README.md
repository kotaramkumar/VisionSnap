# VisionSnap AI

An intelligent image recognition mobile app built with React Native and Expo, powered by Claude Opus (claude-opus-4-6) by Anthropic.

Point your camera at anything and instantly receive rich, educational information about what it sees.

## Features

### 11 Scan Categories

| Category | Icon | What you get |
|----------|------|-------------|
| Leaves | 🍃 | Plant name, leaf type, medicinal uses, ecological importance |
| Trees | 🌳 | Species, scientific name, height, origin, lifespan, uses |
| Vegetables | 🥦 | Nutrition, calories per 100g, health benefits, storage tips |
| Food | 🍔 | Calories, macros (carbs/protein/fats), health benefits, portion size |
| Animals | 🐾 | Species, habitat, diet, lifespan, conservation status, fun facts |
| Cars & Vehicles | 🚗 | Make, model, year, engine type, notable features, fun facts |
| Public Figures | 👤 | Bio, profession, nationality, achievements, career summary |
| Historical Places | 🏛️ | Location, history, architecture, significance, visitor info |
| Country Flags | 🚩 | Country details, capital, population, currency, flag symbolism |
| World Maps | 🗺️ | Region, visible countries, geographic features |
| Objects | 📦 | Description, category, uses, interesting facts |

### App Highlights
- **Camera & Gallery** — scan live or pick from your photo library
- **Scan History** — browse all past scans with thumbnails
- **Offline API key storage** — key stored securely on-device only
- **Dark theme** — easy on the eyes

## Tech Stack

- **Expo SDK 54** + React Native 0.81.5 + React 19.1.0
- **Claude Opus API** (`claude-opus-4-6`) via direct fetch (vision-enabled)
- **expo-image-picker** — camera and gallery capture
- **expo-file-system** — base64 image encoding
- **React Navigation v7** — bottom tabs + native stack
- **AsyncStorage** — persists API key and scan history (up to 50 scans)

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) 18+
- [Expo Go](https://expo.dev/client) app on your iOS or Android device
- An [Anthropic API key](https://console.anthropic.com/)

### Installation

```bash
git clone https://github.com/kotaramkumar/VisionSnap.git
cd VisionSnap
npm install
npx expo start
```

Scan the QR code with Expo Go to launch the app on your device.

### API Key Setup

1. Open the app and go to the **Settings** tab
2. Enter your Anthropic API key (`sk-ant-...`)
3. Tap **Save Key**
4. You're ready to scan

Get an API key at [console.anthropic.com](https://console.anthropic.com/) → API Keys → Create Key.

## Project Structure

```
VisionSnap/
├── App.js                        # Root component
├── app.json                      # Expo config
├── src/
│   ├── context/
│   │   └── AppContext.js         # Global state (API key, scan history)
│   ├── navigation/
│   │   └── index.js              # Bottom tabs + stack navigator
│   ├── screens/
│   │   ├── HomeScreen.js         # Camera/gallery + category chips
│   │   ├── ResultScreen.js       # AI result display
│   │   ├── HistoryScreen.js      # Past scans list
│   │   └── SettingsScreen.js     # API key management
│   ├── services/
│   │   └── claudeService.js      # Anthropic API integration
│   └── utils/
│       └── storage.js            # AsyncStorage helpers
└── assets/                       # Icons and splash screen
```

## Screenshots

| Home | Result | History | Settings |
|------|--------|---------|----------|
| Camera viewfinder with category chips | Rich structured data cards | Thumbnail scan history | API key config + scan types |

## License

MIT
