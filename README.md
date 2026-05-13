# AItomation

The desktop app for AItomation.

## Download

Get the installer for your operating system from the
[latest release](https://github.com/stanislavmandrik621/aitomation-releases/releases/latest).

- **macOS (Apple Silicon, M1/M2/M3/M4)**: the `.dmg` file ending in `arm64`
- **macOS (Intel)**: the `.dmg` file ending in `x64`
- **Windows 10 / 11 (64-bit)**: the `.exe` file ending in `setup`
- **Linux (64-bit)**: the `.AppImage` file

You can ignore every other file in the release (`*.blockmap`, `*.zip`,
`latest-*.yml`). Those are used by the in-app auto-updater.

---

## Install on macOS

1. Download the `.dmg` that matches your Mac.
   - Apple Silicon (most Macs from 2020 onwards): pick `arm64`.
   - Intel Macs: pick `x64`.
   - Not sure? Click the Apple menu, then **About This Mac**, and
     look at **Chip** or **Processor**.
2. Double-click the downloaded `.dmg` to open it.
3. Drag the **AItomation** icon into the **Applications** folder.
4. Eject the disk image (right-click the AItomation drive on the
   desktop, then **Eject**).
5. Open **Applications** and launch **AItomation**.

### First launch: "AItomation can't be opened" warning

Until the app is notarised with Apple, macOS will show a Gatekeeper
warning the first time you open it. This is expected and only
happens once.

**To open the app:**

1. Open **System Settings**, then **Privacy & Security**.
2. Scroll to the **Security** section.
3. You will see a message like
   *"'AItomation' was blocked to protect your Mac."*
4. Click **Open Anyway**, then confirm with **Open** in the popup.

From then on, AItomation launches normally like any other Mac app.

> Power-user alternative: open Terminal and run
> `xattr -cr /Applications/AItomation.app`, then launch the app.

---

## Install on Windows

1. Download the `.exe` file ending in `setup` (the file name looks like
   `AItomation-0.1.x-setup.exe`).
2. Double-click the installer.
3. Choose where to install (the default location is fine for most
   users) and click **Install**.
4. When the installer finishes, AItomation will start automatically.
   You will also find it in your Start menu.

### First launch: "Windows protected your PC" (SmartScreen)

Until the app is signed with a Microsoft-trusted certificate, Windows
SmartScreen may show a blue warning the first time you run the
installer.

**To open the installer:**

1. Click **More info** in the blue dialog.
2. Click **Run anyway**.

You only need to do this once per installer. The installed app will
launch normally afterwards.

> If your organisation uses managed Windows (Defender for Business or a
> third-party AV), your IT admin may need to allow-list the installer.

---

## Install on Linux

1. Download the `.AppImage` file.
2. Make it executable:
   ```bash
   chmod +x AItomation-0.1.x-x86_64.AppImage
   ```
3. Run it:
   ```bash
   ./AItomation-0.1.x-x86_64.AppImage
   ```

Most distributions will also let you double-click the file from your
file manager once it has the executable bit set.

> Some minimal distributions need FUSE installed:
> `sudo apt install libfuse2` (Debian / Ubuntu) or the equivalent.

---

## Updates

AItomation keeps itself up to date in the background. When a new
version is ready, the app shows a small toast in the bottom-right
corner with two buttons:

- **Install now**: restarts the app and installs the update.
- **Later**: snoozes the prompt for 4 hours.

You don't need to revisit this page to check for new versions. If
you ever want to update manually, just download the latest installer
from the release page and run it on top of your existing install.

---

## Uninstall

- **macOS**: drag **AItomation** from the **Applications** folder to
  the Trash.
- **Windows**: open **Settings**, then **Apps**, then **Installed apps**,
  find **AItomation**, click the **...** menu, then **Uninstall**.
- **Linux**: delete the `.AppImage` file.

Your local data lives in your user profile and is preserved when you
uninstall. If you want to wipe it as well:

- **macOS**: `~/Library/Application Support/AItomation`
- **Windows**: `%APPDATA%\AItomation`
- **Linux**: `~/.config/AItomation`

---

## Support

Use the in-app feedback button, or contact us at
<https://v-aid.ai>.
