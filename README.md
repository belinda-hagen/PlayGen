<p align="center">
  <img src="assets/icon.png" alt="PlayGen Logo" width="120" />
</p>

<h1 align="center">PlayGen</h1>

<p align="center">
  <strong>YouTube music downloader & playlist manager built with Electron</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Electron-28-191970?style=for-the-badge&logo=electron&logoColor=white" alt="Electron" />
  <img src="https://img.shields.io/badge/Node.js-18+-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/Platform-Windows-0078D4?style=for-the-badge&logo=windows&logoColor=white" alt="Platform" />
  <img src="https://img.shields.io/badge/License-MIT-ff2d78?style=for-the-badge" alt="License" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/yt--dlp-powered-a855f7?style=flat-square" alt="yt-dlp" />
  <img src="https://img.shields.io/badge/ffmpeg-required-ff5c9a?style=flat-square" alt="ffmpeg" />
  <img src="https://img.shields.io/badge/Audio-320kbps_MP3-22c55e?style=flat-square" alt="Audio Quality" />
</p>

---

## ✨ Features

- **Download from YouTube** — Paste a link, get high-quality MP3 (320 kbps)
- **Library management** — All your tracks in one place with thumbnails, titles & durations
- **Playlist system** — Create, rename, reorder & delete playlists with drag-and-drop
- **Full music player** — Play/pause, skip, shuffle, repeat (one/all), seek & volume
- **Audio visualizer** — Real-time equalizer bars on the album thumbnail
- **Mini player** — Compact always-on-top player when minimized
- **Search** — Instantly filter songs across your library
- **Session restore** — Picks up right where you left off
- **Settings panel** — Customize behavior (mini player on minimize, etc.)
- **Keyboard shortcuts** — Full keyboard control for power users

## 📋 Prerequisites

| Tool | Install |
|------|---------|
| **Node.js** 18+ | [nodejs.org](https://nodejs.org) |
| **yt-dlp** | `winget install yt-dlp` or [GitHub releases](https://github.com/yt-dlp/yt-dlp/releases) |
| **ffmpeg** | `winget install ffmpeg` or [ffmpeg.org](https://ffmpeg.org/download.html) |

> PlayGen auto-detects yt-dlp and ffmpeg from your PATH or common WinGet install locations.

## 🚀 Quick Start

```bash
# Clone the repo
git clone https://github.com/your-username/PlayGen.git
cd PlayGen

# Install dependencies
npm install

# Run the app
npm start
```

## ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` | Play / Pause |
| `←` / `→` | Seek −5s / +5s |
| `Ctrl+←` / `Ctrl+→` | Previous / Next track |
| `↑` / `↓` | Volume up / down |
| `S` | Toggle shuffle |
| `R` | Cycle repeat (off → all → one) |
| `Ctrl+F` | Focus search |

## 📁 Project Structure

```
PlayGen/
├── main.js              # Electron main process — IPC, downloads, database
├── preload.js           # Secure bridge (contextBridge API)
├── package.json
├── assets/
│   ├── icon.png         # App icon (256×256)
│   └── icon.ico         # Windows icon
├── src/
│   ├── index.html       # App layout & UI structure
│   ├── styles.css       # Velvet Noir theme
│   ├── renderer.js      # App logic, player, visualizer
│   └── mini-player.html # Compact mini player window
└── README.md
```

## ⚙️ How It Works

1. **Download** — Paste a YouTube URL → yt-dlp extracts audio → saved as 320 kbps MP3
2. **Library** — All downloads appear in "All Downloads" with metadata & artwork
3. **Playlists** — Create playlists in the sidebar, drag songs or use the right-click menu
4. **Player** — Click any song to play — controls, visualizer & progress in the bottom bar
5. **Mini Player** — Minimize the window → a compact player stays on top of your screen
6. **Storage** — Song metadata & playlists stored in a JSON database in your app data folder

## 🎨 Theme

PlayGen uses the **Velvet Noir** theme — pure black canvas with hot pink and electric purple accents, Space Grotesk + Inter typography, ambient glow effects, and smooth animations throughout.

## 📄 License

MIT