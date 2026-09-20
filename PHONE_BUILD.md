# Suda — Build APK using only an Android phone

This project is prepared for a phone-only GitHub Actions build. You do NOT need Android Studio or a PC.

## 1. Create a GitHub repository
Create an empty repository named `Suda`.

## 2. Extract this ZIP on your phone
Do NOT upload this ZIP itself.

Extract it and upload the PROJECT ROOT contents to GitHub. The repository root must directly contain:

- `.github/`
- `app/`
- `build.gradle`
- `gradle.properties`
- `settings.gradle`
- `README.md`
- `PHONE_BUILD.md`

Do not upload an extra outer `Suda_Phone_Build_FIXED` folder around these files.

## 3. Run the APK build
Open the repository in GitHub:

Actions → Build Suda APK → Run workflow → Run workflow

Wait for the workflow to finish with a green check.

## 4. Download the APK
Open the completed workflow run.

Scroll to **Artifacts** → tap **Suda-debug-apk**.

Download the artifact ZIP, extract it, and install `app-debug.apk`.

## 5. Test Suda
Install Suda on two Android phones. Grant the requested nearby/Bluetooth permissions. Open Suda on both phones and tap:

"डिवाइस खोजें व कनेक्ट करें"

Then test sending messages.

## Important
This is a debug/test APK. It uses Google Nearby Connections and direct nearby device communication. `P2P_CLUSTER` is not automatically a true multi-hop mesh; a future version would need explicit relay/routing logic for messages to hop through other phones.
