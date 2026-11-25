<img width="1206" height="2622" alt="Simulator Screenshot - iPhone 17 - 2026-11-25 at 19 15 57" src="https://github.com/user-attachments/assets/5b6023a4-2f6e-4ead-a020-e47ad8adf8ca" />
<img width="1206" height="2622" alt="Simulator Screenshot - iPhone 17 - 2026-11-25 at 19 15 40" src="https://github.com/user-attachments/assets/d6f0066c-c1b6-4ade-b246-1bd204240feb" />

A clean, modern iOS app that tracks your walks and runs.
Press **Start**, move around, and watch your route being drawn live on the map while distance and time update in real time. Press **Stop**, and the walk is saved to your history so you can open it again anytime.

Built entirely with Apple's latest frameworks: **SwiftUI**, the async **Core Location** API, **MapKit for SwiftUI**, and **SwiftData**. No third-party dependencies.

## ✨ Features

- **Live GPS tracking** using the modern `CLLocationUpdate.liveUpdates()` async stream
- **Route drawn in real time** on the map, with a start marker
- **Live stats**: distance (auto-formatted in m / km) and a ticking timer
- **Automatic permission handling**: iOS asks for location access the moment tracking starts
- **Persistent history**: every walk is saved locally and survives app restarts
- **Swipe to delete** walks from the history
- **Route detail screen** that auto-frames the whole route with start and end markers
- **Friendly empty state** when no walks have been recorded yet

## 🛠 Built with

| Technology | Used for |
|---|---|
| **SwiftUI** | The full UI: tabs, navigation, lists, panels |
| **Core Location** | `CLLocationUpdate.liveUpdates(.fitness)` to stream GPS positions with `async/await` |
| **MapKit for SwiftUI** | `Map`, `MapPolyline`, `Marker`, `UserAnnotation`, `MapCameraPosition`, map controls |
| **SwiftData** | `@Model`, `ModelContainer`, `ModelContext` and `@Query` to save and display walks |
| **Swift Concurrency** | A cancellable `Task` that drives the location stream |
| **Foundation formatters** | `Measurement` and `Duration` for locale-aware distance and time |

## 🚀 Getting started

### Requirements
- Xcode 16 or later
- iOS 18.0+ (simulator or device)

### Run it
1. Clone the repo:
   ```bash
   git clone https://github.com/Amine-mdidech/GPSTrackingApp.git
   ```
2. Open `GPSTrackingApp.xcodeproj` in Xcode.
3. Select an iPhone simulator or your own device.
4. Press **Run** (⌘R).

### Simulating a walk in the simulator
The simulator has no real GPS, so you need to give it a route:
- **Built-in:** in the simulator menu, choose **Features → Location → City Run**.
- **Custom GPX route:** add a `.gpx` file to the project, then choose it in **Product → Scheme → Edit Scheme → Run → Options → Default Location**.

On a real iPhone, the app uses your actual GPS. Just go for a walk.

## 👤 Author

**Amine Benchekroun**, iOS developer

- GitHub: [@Amine-mdidech](https://github.com/Amine-mdidech)
- LinkedIn: [amine-benchekroun-](https://www.linkedin.com/in/amine-benchekroun-)

If you find this project useful or interesting, feel free to ⭐ the repo!
