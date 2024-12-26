# Installation Guide for Running the Ise View Application


## Notes
- Ensure `set.txt` and `app.ise` are placed in the same directory as the executable.
- For Android, include `set.txt` and `app.ise` as assets in the project.
- Adjust paths in the code as necessary for your platform.
- All files in `asset` folder `except app.c`.
  
## 1. **Linux**

### Prerequisites
Ensure the following dependencies are installed:
- GTK 3+
- WebKit2GTK
- A C compiler like `gcc`

### Installation Steps
1. Install the required dependencies:
   - On Debian/Ubuntu-based systems:
     ```bash
     sudo apt update
     sudo apt install libgtk-3-dev libwebkit2gtk-4.0-dev build-essential
     ```
   - On Arch-based systems:
     ```bash
     sudo pacman -Syu gtk3 webkit2gtk base-devel
     ```
     Or
       ```bash
     sudo pamac install gtk3 webkit2gtk base-devel
     ```
   - On Fedora:
     ```bash
     sudo dnf install gtk3-devel webkit2gtk3-devel gcc
     ```

2. Compile the application:
   ```bash
   gcc app.c -o app $(pkg-config --cflags --libs gtk+-3.0 webkit2gtk-4.0)
   ```

3. Run the application:
   ```bash
   ./app
   ```

---

## 2. **Windows**

### Prerequisites
- Install [MSYS2](https://www.msys2.org/) for a Linux-like development environment.
- GTK and WebKit2GTK libraries for Windows.

### Installation Steps
1. Install MSYS2 and update the package database:
   ```bash
   pacman -Syu
   ```

2. Install GTK and WebKit2GTK:
   ```bash
   pacman -S mingw-w64-x86_64-gtk3 mingw-w64-x86_64-webkit2gtk
   ```

3. Compile the application:
   ```bash
   gcc app.c -o app $(pkg-config --cflags --libs gtk+-3.0 webkit2gtk-4.0)
   ```

4. Run the application:
   ```bash
   ./app.exe
   ```

---

## 3. **Android**

### Prerequisites
- Android NDK
- GTK for Android (Cross-compilation)

### Installation Steps
1. Install the Android NDK from [Android Developers](https://developer.android.com/ndk/downloads).
2. Cross-compile GTK and WebKit2GTK for Android.
   - Follow the instructions on [GTK for Android](https://gitlab.gnome.org/GNOME/gtk/-/wikis/Building-GTK-for-Android).

3. Modify the `Android.mk` and `Application.mk` to include the application and dependencies.

4. Build the application:
   ```bash
   ndk-build
   ```

5. Install the APK on an Android device:
   ```bash
   adb install path/to/your.apk
   ```

6. Run the app from the Android launcher.

---

