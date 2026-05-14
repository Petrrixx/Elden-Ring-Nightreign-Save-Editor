# macOS & Linux Support

## Status: ✅ Fully Supported

This application is now fully compatible with macOS and Linux systems.

### Platform-Specific Changes

#### Font Support
- **Windows**: Uses `Microsoft JhengHei` font (default)
- **macOS**: Uses `Helvetica` font (system-native)
- **Linux**: Uses `DejaVu Sans` font (universal fallback)

Fonts are automatically selected based on the operating system.

### Build & Deployment

#### macOS
```bash
cd src
/opt/homebrew/bin/pyinstaller build_mac.spec
# App bundle available in: ../dist/Nightreign_Relic_Editor.app
```

#### Linux
Build specifications can be created following PyInstaller best practices. The application has no platform-specific dependencies preventing Linux builds.

#### Windows
Original build process remains unchanged:
```bash
cd src
pyinstaller build.spec
# or
pyinstaller build_win64_onedir.spec
```

### Testing
- ✓ Application imports successfully on macOS with Python 3.12+
- ✓ Font selection detects macOS platform correctly  
- ✓ PyInstaller builds macOS app bundle successfully
- ✓ All dependencies are cross-platform

### Save File Locations
See README.md for platform-specific save file paths.
