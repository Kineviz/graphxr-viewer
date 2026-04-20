# GraphXR Viewer

A standalone viewer application for GraphXR project files (.graphxr).

## About

GraphXR Viewer is a free application that allows you to view and interact with GraphXR project files without requiring a full GraphXR installation. It provides essential visualization and navigation capabilities for exploring graph data.

## Features

- **3D Graph Visualization**: Interactive 3D rendering of nodes and relationships
- **Navigation Tools**: Pan, zoom, rotate, and navigate through graph data
- **Information Panels**: View detailed information about nodes and relationships
- **Legends**: Visual legends for node and relationship types
- **File Association**: Double-click .graphxr files to open them automatically
- **Cross-Platform**: Available for Windows, macOS, Linux, and iPadOS (Development build)

## Installation

### Download
Download the latest version from the [GitHub Releases](https://github.com/Kineviz/graphxr-viewer/releases/latest) page.

### Windows
1. Download `GraphXR Viewer Setup 3.8.0.exe` from the releases page
2. Run the installer and follow the setup wizard
3. The application will be installed and shortcuts created

### Portable Version
1. Download `GraphXR Viewer-3.8.0-win.zip` from the releases page
2. Extract the ZIP file to your desired location
3. Run `GraphXR Viewer.exe`

### macOS
1. Download the appropriate DMG file for your Mac:
   - Intel Macs: `GraphXR Viewer-3.8.0.dmg`
   - Apple Silicon: `GraphXR Viewer-3.8.0-arm64.dmg`
2. Open the DMG file and drag GraphXR Viewer to Applications
3. **If you see "GraphXR Viewer is damaged and can't be opened"**:
   - Open Terminal
   - Run: `xattr -cr "/Applications/GraphXR Viewer.app"`
   - Try launching the app again
   - Alternatively: Right-click the app → Open → Click "Open" in the security dialog
4. Launch from Applications or Launchpad

### Linux
1. Download the appropriate package:
   - AppImage: `GraphXR Viewer-3.8.0-arm64.AppImage`
   - Debian: `graphxr-viewer_3.8.0_arm64.deb`
2. For AppImage: Make executable and run
3. For DEB: Install with `sudo dpkg -i graphxr-viewer_3.8.0_arm64.deb`

### iPadOS (Development build)

The iPad build is distributed as a **Development-signed `.ipa`**
(`GraphXR-Viewer-3.8.0-iPad-Development.ipa`). It is **not on the App Store**
and cannot be installed by tapping on the file in Safari or Files — iPadOS
rejects sideloading of untrusted developer builds. You need a Mac with Xcode
or Apple Configurator 2, and the target iPad must be enrolled in the
Kineviz Apple Developer team's device list. Requires **iPadOS 14 or later**.

#### Method 1: Xcode (recommended for developers)
1. Download `GraphXR-Viewer-3.8.0-iPad-Development.ipa` from the releases page
2. Connect the iPad to your Mac with a USB cable and trust the computer on
   the iPad when prompted
3. Open Xcode → **Window** → **Devices and Simulators**
4. Select the iPad in the left sidebar
5. Under **Installed Apps**, click the **+** button
6. Select the downloaded `.ipa` file
7. Xcode installs the app; it appears on the iPad's home screen
8. On the iPad, go to **Settings** → **General** → **VPN & Device Management**,
   tap the Kineviz developer profile, and tap **Trust**
9. Launch GraphXR Viewer from the home screen

#### Method 2: Apple Configurator 2 (recommended for non-developers)
1. Install **Apple Configurator 2** from the Mac App Store (free)
2. Download `GraphXR-Viewer-3.8.0-iPad-Development.ipa`
3. Connect the iPad to your Mac and open Apple Configurator 2
4. Double-click the iPad in the main window
5. Click **Add** → **Apps…** → **Choose from my Mac…**
6. Select the downloaded `.ipa` file and click **Add**
7. Confirm the installation prompt
8. On the iPad, trust the developer profile under
   **Settings** → **General** → **VPN & Device Management**

#### Notes and limitations
- **Device must be registered**: Development builds only run on iPads whose
  UDID is listed in the team's provisioning profile. If the app refuses to
  launch with a signing error, the device needs to be added to the profile
  and the IPA re-signed.
- **File opening**: Use the **Files** app on the iPad or AirDrop from a Mac
  to send a `.graphxr` file to the iPad, then use the Share sheet to open
  it in GraphXR Viewer.
- **Expiration**: Development-signed apps expire after the provisioning
  profile's validity period (typically 1 year for paid developer accounts,
  7 days for free accounts). When the app stops launching, re-install a
  fresh build.

## Usage

1. **Open Files**: 
   - Drag and drop .graphxr files onto the viewer window
   - Use File → Open... from the menu
   - Double-click .graphxr files (if file association is enabled)

2. **Navigation**:
   - Left mouse: Pan the view
   - Right mouse: Rotate the view (3D mode)
   - Mouse wheel: Zoom in/out
   - Use navigation tools in the bottom-right corner

3. **Information**:
   - Click on nodes or relationships to view details in the info panel
   - Use legends to understand node and relationship types

## System Requirements

- **Operating System**:
  - Windows 10 or later (64-bit)
  - macOS 10.12 or later
  - Linux (64-bit)
  - iPadOS 14 or later (arm64; Development build — see install notes above)
- **Memory**: 4 GB RAM minimum, 8 GB recommended (desktop); any supported iPad for iPadOS
- **Graphics**: DirectX 11 compatible graphics card (Windows) or OpenGL compatible (macOS/Linux); Metal-capable iPad
- **Storage**: 200 MB available space (desktop); ~400 MB on iPad

## Troubleshooting

### macOS: "App is Damaged" Error

If you encounter the "GraphXR Viewer is damaged and can't be opened" error on macOS:

**Method 1: Remove Quarantine Attribute (Recommended)**
1. Open Terminal
2. Run: `xattr -cr "/Applications/GraphXR Viewer.app"`
3. Launch the app again

**Method 2: System Preferences**
1. Go to **System Preferences** → **Security & Privacy** → **General**
2. Click **"Open Anyway"** next to the GraphXR Viewer message

**Method 3: Right-Click Method**
1. Right-click on `GraphXR Viewer.app` in Applications
2. Select **"Open"** from the context menu
3. Click **"Open"** in the security dialog

This error occurs because the app is not code-signed. The app is safe to use - macOS is just being cautious about unsigned applications.

## License

This software is proprietary and owned by Kineviz, Inc. See the LICENSE file for complete terms and conditions.

**Key Points**:
- Free to use for viewing GraphXR files
- No modification or redistribution allowed
- Commercial use requires permission from Kineviz
- No warranty provided

## Support

For technical support or questions:
- Email: support@kineviz.com
- Website: https://www.kineviz.com
- Documentation: https://www.kineviz.com/graphxr

## About Kineviz

Kineviz is the creator of GraphXR, a powerful platform for interactive graph visualization and analysis. Learn more at https://www.kineviz.com.

---

Copyright © 2026 Kineviz, Inc. All rights reserved.
