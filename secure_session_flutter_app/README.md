# Secure Session Flutter App (Preview)

This folder contains a minimal runnable Flutter project intended for preview/runtime.

## Run (web)
From this folder:

```bash
flutter pub get
flutter run -d web-server --web-port=8080 --web-hostname=0.0.0.0
```

## Backend base URL (optional)
If/when the app is extended to call the backend, pass:

```bash
flutter run -d web-server --dart-define=API_BASE_URL=http://localhost:3001
```
