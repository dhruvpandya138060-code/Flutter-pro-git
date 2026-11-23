# App 5: Quote App

Reconstructed from Udemy course screenshots (not the instructor's original code).
Fetches a random quote as JSON from `https://dummyjson.com/quotes/random`, decodes it into `Quote`, and displays its text and author. The refresh floating button retrieves another quote. Handles loading and network errors. Uses `ChangeNotifier` rather than GetX.

## Run

```powershell
flutter create .
flutter pub get
flutter run -d chrome
```

Internet required. On Android, confirm AndroidManifest contains Internet permission when needed.

## Viva
- REST API: HTTP interface for retrieving resources.
- GET: reads JSON from server.
- `jsonDecode`: parses JSON string into Dart structures.
- `ChangeNotifier`: notifies listeners to redraw the screen.
