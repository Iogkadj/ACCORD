# Boeing 737 Coordinate Viewer - Android App Setup
    
    ## Quick Setup Guide
    
    ### Prerequisites
    1. **Node.js** (v14 or higher) - Download from https://nodejs.org/
    2. **Android Studio** - Download from https://developer.android.com/studio
    3. **JDK 11 or higher** - Usually comes with Android Studio
    
    ### Step 1: Install Dependencies
    Open terminal/command prompt in this folder and run:
    ```bash
    npm install
    ```
    
    ### Step 2: Install Capacitor CLI Globally
    ```bash
    npm install -g @capacitor/cli
    ```
    
    ### Step 3: Initialize Capacitor
    ```bash
    npx cap init "Boeing 737 Viewer" "com.supercool.boeing737viewer" --web-dir=www
    ```
    
    ### Step 4: Add Android Platform
    ```bash
    npx cap add android
    ```
    
    ### Step 5: Sync Files
    ```bash
    npx cap sync
    ```
    
    ### Step 6: Open in Android Studio
    ```bash
    npx cap open android
    ```
    
    This will open Android Studio with your project.
    
    ### Step 7: Build and Run
    1. In Android Studio, connect your Android phone via USB (enable USB Debugging in Developer Options)
    2. OR use an Android emulator (create one in Android Studio's AVD Manager)
    3. Click the green "Run" button (or press Shift+F10)
    4. Select your device and the app will install and launch!
    
    ---
    
    ## Alternative: Generate APK Directly (Without Android Studio)
    
    If you want to generate an APK file to share or install directly:
    
    ### Method 1: Using Android Studio
    1. Follow steps 1-6 above
    2. In Android Studio: Build > Build Bundle(s) / APK(s) > Build APK(s)
    3. APK will be in: `android/app/build/outputs/apk/debug/app-debug.apk`
    4. Transfer this APK to your phone and install it
    
    ### Method 2: Using Gradle Command Line
    ```bash
    cd android
    ./gradlew assembleDebug
    ```
    APK location: `android/app/build/outputs/apk/debug/app-debug.apk`
    
    ---
    
    ## Troubleshooting
    
    **Issue: "capacitor: command not found"**
    - Solution: Run `npm install -g @capacitor/cli`
    
    **Issue: Android Studio can't find SDK**
    - Solution: In Android Studio, go to Tools > SDK Manager and install Android SDK
    
    **Issue: App crashes on phone**
    - Solution: Check that your phone's Android version is 5.1 (API 22) or higher
    - Enable "Install from Unknown Sources" in phone settings
    
    **Issue: 3D model doesn't load**
    - Solution: This is normal - the 3D model URL is external. The coordinate visualization will still work perfectly!
    
    ---
    
    ## File Structure
    ```
    boeing-737-app/
    ├── www/
    │   └── index.html          # Your web app
    ├── android/                # Generated Android project (after npx cap add android)
    ├── package.json           # Node dependencies
    ├── capacitor.config.json  # Capacitor configuration
    ├── AndroidManifest.xml    # Android app manifest template
    ├── build.gradle          # Android build configuration template
    └── SETUP_INSTRUCTIONS.md # This file
    ```
    
    ---
    
    ## Quick Commands Reference
    - `npm install` - Install dependencies
    - `npx cap add android` - Add Android platform
    - `npx cap sync` - Sync web files to Android
    - `npx cap open android` - Open in Android Studio
    - `npx cap run android` - Build and run on connected device
    
    ---
    
    ## Testing on Your Phone
    1. Enable Developer Options on your Android phone:
       - Go to Settings > About Phone
       - Tap "Build Number" 7 times
    2. Enable USB Debugging:
       - Settings > Developer Options > USB Debugging
    3. Connect phone to computer via USB
    4. Run `npx cap run android`
    
    The app will install and launch automatically!
    