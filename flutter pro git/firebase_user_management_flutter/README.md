# App 7: Firebase Firestore User Management

Reconstructed from the Firebase screenshot. A form creates/updates `users` documents with `name`, `city`, and `salary` in Cloud Firestore. Live list through Firestore snapshots; edit and delete actions included.

**Requires your own Firebase project.** No Firebase credentials/configuration are included in this ZIP, and Firestore will not work until you configure Firebase and proper security rules. This is not an offline demo.

## Set up
1. Extract and open folder in VS Code.
2. Run `flutter create .` and `flutter pub get`.
3. Install the Firebase CLI and FlutterFire CLI if not present; sign in and run `flutterfire configure` inside this project.
4. In `lib/main.dart`, import `firebase_options.dart` and replace `await Firebase.initializeApp();` with `await Firebase.initializeApp(options: DefaultFirebaseOptions.currentPlatform);`.
5. In Firebase Console enable Cloud Firestore and configure development-appropriate rules. Do not publish an open write-access database.
6. Run `flutter run -d chrome`.

## Viva
Firebase = backend cloud platform; Firestore = document-oriented NoSQL database; `snapshots()` = real-time stream; `add`, `update`, `delete` = CRUD writes.
