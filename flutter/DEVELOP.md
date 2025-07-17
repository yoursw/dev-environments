# Flutter Development

## Prerequisites

* Latest JDK
* Android Emulator
* Flutter

## Setup

### Android Emulator

1. Install Command Line Tools
  a. https://developer.android.com/studio#command-line-tools-only
  b. Extract to `/usr/lib/Android/cmdline-tools/latest/`

  ```bash
    sudo mkdir -p /usr/lib/Android/cmdline-tools
    sudo unzip -d /usr/lib/Android/cmdline-tools/latest cmdline-tools.*.zip
    sudo chown -R $USER:$USER /usr/lib/Android
  ```

2. Setup Emulator
  * https://developer.android.com/tools/releases/platforms

  a. Download latest android

  ```bash
    sdkmanager "system-images;android-36;google_apis;x86_64"
    sdkmanager "platforms;android-36"
    sdkmanager "platform-tools"
    # sdkmanager "patcher;v4"
    sdkmanager "emulator"
    sdkmanager "build-tools;35.0.0"
  ```

  b. Configure emulated device

  ```bash
    avdmanager -s create avd -n pixel -k "system-images;android-36;google_apis;x86_64"
  ```
  c. Check config

  ```bash
    avdmanager list
    flutter doctor -v
  ```

  d. Accept licenses

  ```bash
    sdkmanager --licenses
  ```

  e. Run Emulator

  ```bash
    flutter emulator --launch pixel
  ```

  REF: https://dev.to/jay_js/setting-up-flutter-without-android-studio-olo

### Flutter

Refer to [install docs](https://docs.flutter.dev/get-started/install)

### IDE

#### VSCode

Install from https://code.visualstudio.com

#### IntelliJ

TODO

#### NeoViM

TODO

