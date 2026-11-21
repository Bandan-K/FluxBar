# FluxBar

A small macOS menu bar app that keeps an eye on your Mac and remembers what you copy.

Live network speed, temperatures and fan speed sit next to the clock. Clipboard history is one shortcut away. A built-in cleaner clears out developer caches and other disk clutter.

**[Download FluxBar.dmg](FluxBar.dmg)** · macOS 15 (Sequoia) or later

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
- Press **⇧⌘V** anywhere to open the quick picker. Use the arrow keys to move and **Return** to paste the item into the app you were using. Press **P** to pin or unpin it. You can change the shortcut in Settings.
- **Pin** the snippets you reuse. Pinned items stay at the top, are never trimmed and survive *Clear History*.
- Search your history, delete single items or clear everything else.
- Choose how much to keep: 20, 50, 100 or 200 items.

### System Hub
One page for the live picture of your Mac:
- Download, upload, temperature and fan speed
- CPU load, memory, swap, free disk space, disk throughput, battery and GPU temperature
- Per-core thermal sensors for P-cores, E-cores, GPU clusters and the rest of the system, with CPU usage per core

Download, upload and temperature cards include a short trend line, so you can see whether a spike is over.

Readings only update while the window or menu is open, so FluxBar stays light in the background.

### Heat alerts
Turn on **Settings → Alerts** to get a notification when the CPU stays above a temperature you choose (60–105 °C). Short spikes are ignored and you get at most one alert every 10 minutes.

### Cleaner
Scans for space you can safely win back and shows the size of each item before you clean.

- **Developer:** Xcode Derived Data, iOS Device Support, Xcode Archives, Simulator data, Swift Package Manager cache, CocoaPods cache, Carthage cache, Swift Playgrounds, Xcode temp files, iOS device backups
- **System and user:** system cache, user cache, logs, Trash

Nothing is removed until you tick it, press **Clean Now** and confirm in the **Review Cleanup** sheet, which lists every item and its size.

- Regenerable caches are deleted straight away.
- Items that are harder to replace (Xcode Archives, iOS backups, Device Support files, Playgrounds, Carthage builds) are **moved to the Trash**, so you can still put them back. They are marked *Recoverable* and are off by default. Their space is released when you empty the Trash.

## Using the app

| I want to… | Do this |
|---|---|
| See speed and temperature at a glance | Check the menu bar readout |
| Paste something I copied earlier | **⇧⌘V**, or click the menu bar icon and pick from the list |
| Keep a snippet around | Pin it (**P** in the picker, or the pin button in the list) |
| See every sensor and system stat | Menu bar icon → **Open FluxBar** → **System Hub** |
| Free up disk space | **Open FluxBar → Cleaner → Clean Now** |
| Change what the menu bar shows | **Settings → Menu Bar Metrics** |
| Update faster or slower | **Settings → Refresh Rate** (0.5 s to 5 s) |
| Start FluxBar at login | **Settings → General → Launch at login** |
| Change the clipboard shortcut | **Settings → Clipboard → Shortcut** |
| Hide the stats in the dropdown | **Settings →** turn off *Show stats in menu dropdown* |

## Permissions

- **Full Disk Access (Cleaner):** Without it, protected folders such as the Trash may show 0 KB. Use **Grant Access** in the Cleaner, or enable FluxBar under *System Settings → Privacy & Security → Full Disk Access*.
- **Accessibility (Clipboard):** Needed only to paste straight into the front app from the picker. Without it, the chosen item is copied and you press ⌘V yourself. Enable it under *Privacy & Security → Accessibility*, or turn off *Paste into the front app* in Settings.
- **Notifications (Heat alerts):** macOS asks the first time you turn alerts on.

## Good to know

- Fan and temperature data come from the Mac's System Management Controller. If it can't be reached, Settings shows **Hardware Disconnected** with a **Retry Connection** button.
- Fan readings are read-only. Fan speed control is not available yet.
- Clipboard history is stored on your Mac. FluxBar doesn't send anything anywhere.
- The interface is currently in English.

## Feedback

Questions or bugs? Open an issue on this repo, or visit the [portfolio](https://bandan-kumar.vercel.app).

© 2026 Bandan.K
