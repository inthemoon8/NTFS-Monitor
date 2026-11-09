**[Download NTFS Monitor for Windows (x64)](https://github.com/inthemoon8/NTFS-Monitor/releases/latest/download/NTFS-Monitor-Setup.exe)**

# NTFS Monitor

NTFS Monitor is a Windows desktop utility that shows file creation, modification, and deletion on selected NTFS volumes in real time. It reads the NTFS USN Journal and groups related changes into a lightweight, chat-style overlay.

## Installation

1. Download `NTFS-Monitor-Setup.exe` from the repository's **Releases** page.
2. Run Setup. The default installation folder is `C:\Program Files\NTFS Monitor`. When upgrading, choose your existing installation folder if you want to keep using it.
3. Open **NTFS Monitor** from the Start menu and approve the administrator prompt. Administrator access is required to read the USN Journal.

NTFS Monitor requires Windows 10 or 11 x64 and at least one NTFS volume. Setup includes the .NET Desktop Runtime.

## Using the overlay

On first launch, select the volumes to monitor and the display to use, then click **Apply** (`적용`). You can reopen settings from the notification area icon.

- New entries appear at the bottom and push older entries upward. Each entry fades over 10 seconds by default. An update restarts the fade for that entry.
- Changes of the same type under the same grouping path update an existing entry. The default grouping window closes after 60 seconds of inactivity.
- The overlay normally lets mouse clicks pass through. Hold **Ctrl + Alt** and hover over an entry to highlight it. Click it while holding the keys to open the file or folder in File Explorer. For a deleted file, the app tries to open its last known parent folder.
- The display settings let you choose a monitor, position, text opacity, fade duration, and interaction shortcut. The overlay can appear above other windows or on the desktop only.
- The monitoring settings let you select multiple NTFS volumes and start the app automatically at Windows sign-in using your saved settings.

## Filters and logging

Hide entries by ancestor folder name, filename pattern, extension, or path. The default filters include `Cache`, `Temp`, `*.log`, and `*.tmp`.

Disk logging is off by default. Enable it in the monitoring settings and choose a destination folder to save raw events while recording is enabled. Events hidden by display filters are still included in the log.

## Exiting and uninstalling

To stop monitoring, choose **Exit** (`종료`) from the notification area icon. To uninstall, open **Windows Settings → Apps → Installed apps**, find **NTFS Monitor**, and select **Uninstall**. Uninstalling keeps your saved settings and logs.
