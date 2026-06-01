# Globalize Temu 🌍

A modern and efficient Google Chrome extension that automatically hides "Local" labeled products on Temu, allowing you to focus on global and international items without clutter.

## ✨ Features

*   **Real-time Filtering**: Automatically detects and hides local products as you browse and scroll through Temu, thanks to an efficient `MutationObserver`.
*   **Modern Popup Interface**: A clean, user-friendly popup with smooth animations.
*   **Theme Support**: Built-in Dark and Light modes to match your preference.
*   **Multi-language Support**: Interface available in both English (EN) and Turkish (TR).
*   **Statistics Tracking**: Keeps a running count of the total number of local products hidden by the extension.
*   **Quick Toggle**: Easily enable or disable the extension with a simple switch. Auto-reloads your active Temu tab to apply changes instantly.
*   **Privacy First**: Runs entirely locally in your browser. No data collection or external tracking.

## 🚀 Installation (Developer Mode)

Since this extension is not currently published on the Chrome Web Store, you can install it manually by following these steps:

1. Download or clone this repository to your local machine.
2. Open Google Chrome and navigate to `chrome://extensions/`.
3. Enable **"Developer mode"** by toggling the switch in the top right corner.
4. Click on the **"Load unpacked"** button in the top left corner.
5. Select the `temu_blocker` folder containing the extension files.
6. The "Globalize Temu" extension is now installed and ready to use!

## 🛠️ How it Works

The extension uses Chrome's Manifest V3 architecture.
*   **`content.js`**: Injects into `temu.com` pages. It scans the DOM for specific classes (like `.C9HMW0KN`, `._1O9WmJi_`) and image sources (`local-image`) associated with local products. When found, it hides their parent container (`display: none`).
*   **`popup.js` & `popup.html`**: Handles the user interface, language switching, theme preferences, and displays the blocked item counter using `chrome.storage.local`.

## ⚙️ Requirements
*   Google Chrome browser (or any Chromium-based browser supporting Manifest V3).

---
*Created by [Bohjka](https://github.com/Bohjka)*
