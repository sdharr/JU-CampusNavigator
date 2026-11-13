
# JU Campus Navigator

**An interactive mobile campus-navigation app for the University of Jammu.**

JU Campus Navigator helps students and visitors explore campus locations, find buildings and facilities, and visualize routes across the campus road network.

Built using React Native, Expo, TypeScript, MapLibre, Firebase Firestore, and graph-based routing algorithms.

## Features

- **Interactive Campus Maps:** Explore university buildings, departments, and facilities using MapLibre.
- **Building Search:** Search for campus destinations and view detailed location information.
- **Shortest-Path Navigation:** Uses Dijkstra's algorithm to calculate routes through the campus road network.
- **Alternative Routes:** Explore additional routes between locations when available.
- **GPS Integration:** Uses device location services for current-location tracking.
- **Route Visualization:** Displays navigation paths directly on interactive maps.
- **Firebase Integration:** Retrieves campus locations, road nodes, and road connections from Firestore.
- **Data Caching:** Loads campus data into memory to reduce repeated database requests.

## Tech Stack

| Category | Technologies |
|---|---|
| Mobile Development | React Native, Expo |
| Programming Language | TypeScript |
| Maps | MapLibre, OpenStreetMap, MapTiler |
| Database | Firebase Firestore |
| Navigation | React Navigation |
| Location Services | Expo Location |
| Algorithms | Dijkstra's Algorithm, Graph-Based Routing |
| Version Control | Git, GitHub |

## Demo and Android Build

The Campus Navigator Android development build has been launched successfully using Expo Metro, and interactive map rendering has been tested.

**Development Build:**

[View Campus Navigator on Expo](https://expo.dev/accounts/simrandharr/projects/CampusNavigator/builds/456c368d-c351-40c4-b472-ffa05682396f)

**Standalone Android APK:** Coming soon.

**Screenshots and Demo Video:** Coming soon.

> **Important:** The current Expo link points to a development build that requires a running Metro development server. A standalone APK will be provided after testing. The application uses native MapLibre modules and cannot run inside regular Expo Go.

## Installation and Setup

### Prerequisites

- Node.js and npm
- Android device or Android emulator
- Android development environment or compatible Expo development build
- Firebase Firestore access
- MapTiler API key

### 1. Clone the Repository

```bash
git clone https://github.com/sdharr/JU-CampusNavigator.git
cd JU-CampusNavigator
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the project root.

```env
EXPO_PUBLIC_MAPTILER_KEY=YOUR_MAPTILER_KEY
```

Replace `YOUR_MAPTILER_KEY` with your own MapTiler API key.

> Expo public environment variables are included in the application bundle. Apply appropriate API-key restrictions. Firebase access also depends on Firestore security rules.

### 4. Build the Android Development App

```bash
npx expo run:android
```

Alternatively, install a compatible EAS development build.

### 5. Start the Development Server

```bash
npx expo start --dev-client --lan
```

Connect your computer and Android device to the same Wi-Fi network.

Open the installed Campus Navigator development app and connect to Metro using the displayed QR code.

## How the Navigation System Works

**1. Data Initialization**

The application retrieves campus locations, road nodes, and road connections from Firebase Firestore.

**2. Graph Construction**

The road network is converted into an in-memory graph representing campus locations and their connections.

**3. Location Selection**

Users select a starting point and destination through the application interface.

**4. Shortest-Path Calculation**

Dijkstra's algorithm calculates a shortest path across the campus road graph.

**5. Route Visualization**

The calculated route is displayed on an interactive map using MapLibre.

**6. GPS Navigation**

Device location services support current-location features and location-aware navigation.

## Project Structure

```text
JU-CampusNavigator/
├── App.tsx
├── index.ts
├── src/
│   ├── navigation/
│   ├── context/
│   ├── services/
│   ├── components/
│   ├── data/
│   ├── HomeScreen.tsx
│   ├── MapScreenOSM.tsx
│   ├── LocationPickerScreen.tsx
│   ├── PlaceInfoScreen.tsx
│   └── PlaceDetailScreen.tsx
├── assets/
├── app.json
├── eas.json
├── package.json
├── package-lock.json
└── tsconfig.json
```

## Current Project Status

- React Native application developed with Expo and TypeScript.
- Interactive campus mapping implemented with MapLibre.
- Firebase Firestore integration implemented.
- Graph-based shortest-path and alternative routing logic implemented.
- Android development build successfully launched.
- Map rendering tested on Android.
- Standalone APK and complete end-to-end navigation testing pending.

## Future Improvements

- Publish a standalone Android APK for independent installation.
- Add application screenshots and a demonstration video.
- Improve automated testing and error handling.
- Continue refining navigation accuracy and performance.

## Developer

**Simran Dhar**

GitHub: [github.com/sdharr](https://github.com/sdharr)

Project Repository: [JU-CampusNavigator](https://github.com/sdharr/JU-CampusNavigator)

---

Built as a mobile application project combining React Native development, geographic mapping, graph algorithms, and practical campus navigation.
