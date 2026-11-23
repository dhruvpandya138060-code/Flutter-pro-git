# App 2 — Random Colors

Flutter practice app based on the **Managing State with setState** lesson from *Mastering Flutter: From Basics to Advanced by Building Apps*.

## What it does
- Starts with a blue screen and centered instruction text.
- Tapping the color-lens button generates a new random RGB background color.
- `setState()` rebuilds the page to display the updated background.
- Automatically picks white or black text for readable contrast.

## Run in VS Code / terminal

First ensure Flutter is installed, then open this folder in the terminal:

```powershell
flutter create .
flutter pub get
flutter run -d chrome
```

`flutter create .` generates the Android, iOS, web and desktop platform folders not included in this lightweight ZIP. It keeps the existing source files.

## Test

```powershell
flutter test
```

## Viva talking points
- `StatelessWidget` builds the app wrapper; `StatefulWidget` is used for the changing color screen.
- `_backgroundColor` is the variable storing the current color.
- `Random().nextInt(256)` creates values from 0 through 255 for each RGB channel.
- Calling `setState()` notifies Flutter to rebuild with the new color.
- `ThemeData.estimateBrightnessForColor()` chooses white or black text for contrast.

Note: Based on the visible Udemy screenshot, not a verbatim copy of the instructor's entire source code.
