# WifiSnap

Releases of **WifiSnap** (와이파이 찰칵), an Android app that connects you to Wi-Fi from the note on a café wall.
Point your camera at the paper with the network name and password and it joins that network. No QR code needed:
two plain lines are enough, and labeled notes (`ID / PW`, `와이파이 이름 / 비밀번호`) work too. Text is read on your
phone in Korean and English, and the name is matched against the networks around you so OCR mix-ups like `O`/`0`
get fixed. Dark and light follow your phone's setting.

## Download
Open the [latest release](../../releases/latest) and download `WifiSnap-android-<version>.apk`.

## Updates
The app includes an automatic update system.

Every time you open WifiSnap it checks this repository for a new version. On Wi-Fi it downloads it in the
background, verifies its checksum and signature, and then shows an **update** button at the top of the camera
screen. Tap it and then tap "Install" when Android asks.

## Installation
1. Download `WifiSnap-android-<version>.apk` on your phone (Android 8.0 or later, ARM phones)
2. Open it and allow installing from this source once
3. Open WifiSnap and allow the camera. Allowing location is optional but recommended (see Notes)

## Connecting
- **Android 11 and later**: when the note is read clearly, Android asks "Save this network?". Tap **Save** and you are connected.
- **Android 10**: the app copies the password and opens Wi-Fi settings. Pick the network and paste the password.
- **Android 8–9**: the app adds the network and connects by itself.

If a letter was misread, fix it on the result screen or tap the right network from the nearby list, then tap **Connect**.

## Notes
- Location permission is only used because Android requires it to list nearby Wi-Fi names. Your location itself is not used. Without it the app still works, but it asks you to confirm before connecting.
- Photos are never saved. Text recognition runs on the phone (Google ML Kit), and the only other network access is the update check against this repository.
- Enterprise Wi-Fi (sign in with a username, common at offices and schools) has to be joined from Wi-Fi settings.

If you encounter a problem, please report it so it can be fixed in a future update.
