# App 3 — Ecom Navigation Demo

A learning project reconstructed from the Udemy course screenshot (not extracted original instructor source).

## Features
- Splash screen that automatically opens Login after 2 seconds
- Login form and registration form
- Named routes (`/`, `/login`, `/register`, `/dashboard`)
- Forward navigation via `Navigator.pushNamed`
- Passing registered name and email back using `Navigator.pop` and a typed result
- Passing username through `/dashboard` route arguments; default name: **Dhruv**
- Dashboard displays **Hi, Dhruv!** for the default login
- Basic form validation
- Password show/hide option on login

**Note:** This project is a navigation and forms demonstration. It has no backend, database, or real authentication; pressing Login navigates directly to the dashboard, without checking credentials against a server. Registration returns a name and email to Login.

## Running
1. Extract the ZIP and open the `ecom_navigation_app` directory in VS Code.
2. Run `flutter create .` to create platform directories.
3. Run `flutter pub get`.
4. Run `flutter run -d chrome` (or select your Android emulator).
5. Run `flutter test` to run widget tests.

## Viva quick notes
- `StatelessWidget` doesn't manage mutable widget state; `StatefulWidget` can update the UI through `setState`.
- `Navigator.pushNamed` opens a registered route; `Navigator.pop` returns to the previous screen and optionally returns a result.
- `pushReplacementNamed` replaces Splash with Login so the back button doesn't return to Splash.
- `TextEditingController` reads form field input; dispose controllers when the state is removed.
- `Form` and `TextFormField.validator` check input before submission.

## Screenshot differences
The course example dashboard reads “Hi, Arzoo!”. This reconstruction defaults to “Hi, Dhruv!” as requested. Registering with another name demonstrates dynamic data passing.

## Viva: how the name reaches Dashboard
`Navigator.pushReplacementNamed(context, '/dashboard', arguments: {'username': _displayName})` sends a `Map<String, String>` to the named route. `onGenerateRoute` receives it through `settings.arguments` and creates `DashboardScreen(username: username)`. `DashboardScreen` displays it with string interpolation.
