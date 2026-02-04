# Boeing 737 MAX Coordinate Viewer - Android Installation Guide

## Quick Installation (2 Methods)

### Method 1: Direct APK Installation (Easiest - No Coding Required)
This method requires building the APK once, then you can install it directly on your phone.

#### Prerequisites:
- Android Studio installed on your computer
- USB cable to connect your phone to computer
- Android phone with Developer Mode enabled

#### Step-by-Step Instructions:

**1. Enable Developer Mode on Your Phone:**
   - Go to **Settings** → **About Phone**
   - Tap **Build Number** 7 times until you see "You are now a developer!"
   - Go back to **Settings** → **Developer Options**
   - Enable **USB Debugging**

**2. Install Android Studio:**
   - Download from: https://developer.android.com/studio
   - Install with default settings
   - Open Android Studio and complete the setup wizard

**3. Open the Project:**
   - Launch Android Studio
   - Click **Open** and select the folder containing your app files
   - Wait for Gradle sync to complete (this may take 5-10 minutes the first time)

**4. Connect Your Phone:**
   - Connect your phone to computer via USB
   - On your phone, tap **Allow USB Debugging** when prompted
   - In Android Studio, you should see your device name in the device dropdown (top toolbar)

**5. Build and Install:**
   - Click the green **Play** button (▶) in the top toolbar
   - Android Studio will build the app and install it directly on your phone
   - The app will launch automatically once installed

**6. Use the App:**
   - The app is now installed on your phone!
   - You can disconnect from your computer and use it anytime
   - Find it in your app drawer as "B737 Coordinate Viewer"

---

### Method 2: Build Standalone APK File
If you want to share the app with others or install without USB connection:

**1. Build APK:**
   - In Android Studio, go to **Build** → **Build Bundle(s) / APK(s)** → **Build APK(s)**
   - Wait for build to complete (you'll see a notification)
   - Click **locate** in the notification to find the APK file

**2. Transfer to Phone:**
   - Copy the APK file to your phone (via USB, email, cloud storage, etc.)
   - The APK location is usually: `app/build/outputs/apk/debug/app-debug.apk`

**3. Install on Phone:**
   - On your phone, open your file manager
   - Navigate to the APK file
   - Tap it to install
   - You may need to allow "Install from Unknown Sources" in Settings

---

## Alternative: Use Capacitor CLI (For Developers)

If you're comfortable with command line:

**1. Install Dependencies:**
```bash
cd /path/to/your/project
npm install
```

**2. Add Android Platform:**
```bash
npx cap add android
```

**3. Copy Web Assets:**
```bash
npx cap copy
```

**4. Open in Android Studio:**
```bash
npx cap open android
```

Then follow steps 4-6 from Method 1 above.

---

## Troubleshooting

### "App not installed" error:
- Go to Settings → Security → Enable "Unknown Sources"
- Or Settings → Apps → Special Access → Install Unknown Apps → Enable for your file manager

### USB Debugging not working:
- Try a different USB cable (some cables are charge-only)
- Revoke USB debugging authorizations and try again
- Make sure you're using the correct USB mode (File Transfer/MTP)

### Gradle sync fails:
- Check your internet connection (Gradle needs to download dependencies)
- In Android Studio: File → Invalidate Caches → Restart
- Update Android Studio to the latest version

### App crashes on launch:
- Make sure your phone is running Android 5.0 (Lollipop) or higher
- Check logcat in Android Studio for error messages
- Rebuild the project: Build → Clean Project, then Build → Rebuild Project

### 3D model not loading:
- This is expected in the built APK - the 3D model URL needs to be changed to a local asset
- For now, the coordinate visualization still works even without the 3D model

---

## System Requirements

**Computer:**
- Windows 10/11, macOS 10.14+, or Linux
- 8GB RAM minimum (16GB recommended)
- 10GB free disk space for Android Studio

**Phone:**
- Android 5.0 (Lollipop) or higher
- 50MB free space

---

## What to Expect

Once installed, the app provides:
- ✅ Input fields for Station (STA), Waterline (WL), and Buttock Line (BL) coordinates
- ✅ Model selection for 737-8 MAX and 737-9 MAX
- ✅ Real-time 3D visualization of coordinate position
- ✅ Interactive 3D view (rotate, zoom, pan)
- ✅ Offline functionality (works without internet)

---

## Next Steps After Installation

1. **Test the App:**
   - Enter test coordinates: STA 1000, WL 150, BL 0
   - Verify the point appears in the 3D space
   - Try rotating the view with touch gestures

2. **Customize (Optional):**
   - You can modify the HTML file to add more features
   - Change colors, add measurement tools, etc.
   - Rebuild and reinstall to see changes

---

## Need Help?

If you encounter any issues:
1. Check the Troubleshooting section above
2. Verify all prerequisites are installed
3. Make sure your phone's Android version is compatible
4. Try the alternative installation method

The app should work on most modern Android phones running Android 5.0 or higher!
