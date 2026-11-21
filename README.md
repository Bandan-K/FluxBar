# FluxBar

A small macOS menu bar app that keeps an eye on your Mac and remembers what you copy.

Live network speed, temperatures and fan speed sit next to the clock. Clipboard history is one shortcut away. A built-in cleaner clears out developer caches and other disk clutter.

**[Download FluxBar.dmg](FluxBar.dmg)** · macOS 26 or later · Apple Silicon

---

## Install

1. Download [`FluxBar.dmg`](FluxBar.dmg) (use the **Download raw file** button on the file page).
2. Open it and drag **FluxBar** into **Applications**.
3. Launch FluxBar. It lives in the menu bar and has no Dock icon.

If macOS says the app can't be verified, right-click FluxBar in Applications, choose **Open**, then confirm. You only need to do this once.

## Features

### Menu bar readouts
Pick any combination of **download speed**, **upload speed**, **temperature** and **fan RPM** to show next to the clock. Turn each on or off in **Settings → Menu Bar Metrics**.

### Clipboard history
- Keeps text and images you copy, newest first.
- Press **⌘⇧V** anywhere to open the quick picker. Use the arrow keys to move and **Return** to copy the item back.
- Search your history, delete single items or clear everything.
- Choose how much to keep: 20, 50, 100 or 200 items.

### System Hub
One page for the live picture of your Mac:
- Download, upload, temperature and fan speed
- CPU load, memory, swap, free disk space, disk throughput, battery and GPU temperature
- Per-core thermal sensors for P-cores, E-cores, GPU clusters and the rest of the system, with CPU usage per core

Readings only update while the window or menu is open, so FluxBar stays light in the background.

### Cleaner
Scans for space you can safely win back and shows the size of each item before you clean.

- **Developer:** Xcode Derived Data, iOS Device Support, Xcode Archives, Simulator data, Swift Package Manager cache, CocoaPods cache, Carthage cache, Swift Playgrounds, Xcode temp files, iOS device backups
- **System and user:** system cache, user cache, logs, Trash

Nothing is removed until you tick it and press **Clean Now**. Items you probably want to keep, such as iOS backups, are listed but should be selected deliberately.

## Using the app

| I want to… | Do this |
|---|---|
| See speed and temperature at a glance | Check the menu bar readout |
| Paste something I copied earlier | **⌘⇧V**, or click the menu bar icon and pick from the list |
| See every sensor and system stat | Menu bar icon → **Open FluxBar** → **System Hub** |
| Free up disk space | **Open FluxBar → Cleaner → Clean Now** |
| Change what the menu bar shows | **Settings → Menu Bar Metrics** |
| Update faster or slower | **Settings → Refresh Rate** (0.5 s to 5 s) |
| Hide the stats in the dropdown | **Settings →** turn off *Show stats in menu dropdown* |

## Permissions

- **Full Disk Access (Cleaner):** Without it, protected folders such as the Trash may show 0 KB. Use **Grant Access** in the Cleaner, or enable FluxBar under *System Settings → Privacy & Security → Full Disk Access*.
- **Accessibility (Clipboard):** FluxBar checks for it so the global shortcut and picker behave consistently. If prompted, enable it under *Privacy & Security → Accessibility*.

## Good to know

- Fan and temperature data come from the Mac's System Management Controller. If it can't be reached, Settings shows **Hardware Disconnected** with a **Retry Connection** button.
- Fan readings are read-only. Fan speed control is not available yet.
- Clipboard history is stored on your Mac. FluxBar doesn't send anything anywhere.
- The interface is currently in English.

## Feedback

Questions or bugs? Open an issue on this repo, or visit the [portfolio](https://bandan-kumar.vercel.app).

© 2026 Bandan.K
