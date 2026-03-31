# Flutter App (Auth Module Skeleton)

This folder contains the **Flutter migration skeleton** for the native iOS + Android authentication/session/biometric-lock behaviors.

## What’s included (demo)
- Login (`POST /auth/login`)
- Secure persistence of tokens (flutter_secure_storage)
- Session restore on startup (loads refresh token; if present => requires unlock)
- App lock/unlock using biometrics/passcode fallback (local_auth)
- Protected call (`GET /me`) using an access token
- Token refresh on 401 via Dio interceptor (`POST /auth/refresh`)
- Logout:
  - best-effort `POST /auth/logout` (iOS behavior)
  - clears local tokens (both platforms)
  - clears lock without prompting (iOS behavior)

## Run
1) Ensure you have Flutter installed
2) From this folder:
```bash
flutter pub get
flutter run
```

## Backend base URL
Configure `API_BASE_URL` at build time using `--dart-define`:

Example (Android emulator -> host machine):
```bash
flutter run --dart-define=API_BASE_URL=http://10.0.2.2:3001
```

Example (iOS simulator -> host machine):
```bash
flutter run --dart-define=API_BASE_URL=http://localhost:3001
```

If not provided, defaults to `http://localhost:3001`.
