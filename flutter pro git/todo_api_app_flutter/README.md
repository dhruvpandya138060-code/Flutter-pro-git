# App 6: Todo API (without GetX)

Reconstructed from the Udemy screenshot. Uses regular `StatefulWidget` + `setState`, and `http` with GET/POST/PUT/DELETE to demonstrate CRUD. API: `https://jsonplaceholder.typicode.com/todos`.

**Important:** JSONPlaceholder is a fake testing API: POST, PUT and DELETE return success responses but **changes are not saved on the server**. Changes appear in this app session only and will reset when refreshed. For a persistent CRUD app, replace this endpoint with your own backend.

## Run
```powershell
flutter create .
flutter pub get
flutter run -d chrome
```
Requires internet access.

## Viva
GET = read; POST = create; PUT = update; DELETE = remove. `setState` rebuilds the interface. `Future`/`async`/`await` handle asynchronous HTTP calls.
