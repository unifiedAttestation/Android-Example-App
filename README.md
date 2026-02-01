# Android-Example-App

## Overview
Demonstrates the end-to-end Unified Attestation flow:
- Builds canonical request string
- Computes requestHash
- Uses Android-SDK to fetch providerSet
- Sends backendIds to Example-App-Server
- Requests integrity token
- Sends token to Example-App-Server for verification

## Build
```bash
cd Android-Example-App
./gradlew assembleDebug
```

## Runtime settings
- Example-App-Server URL: `http://10.0.2.2:4000` (Android emulator localhost)
- Update `MainActivity.java` if running on device or using a different host.
- The Unified Attestation service enforces a privileged bind permission. For demo, install the service as a system app or sign the example app with the same key.
