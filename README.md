# 🎬 Reel Text Generator

<p align="center">
  <img src="https://img.shields.io/badge/HTML-5-E34F26?style=flat-square&logo=html5&logoColor=white"/>
  <img src="https://img.shields.io/badge/CSS-3-1572B6?style=flat-square&logo=css3&logoColor=white"/>
  <img src="https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/>
  <img src="https://img.shields.io/badge/Export-MP4%20%7C%20WebM-red?style=flat-square"/>
  <img src="https://img.shields.io/badge/No%20Dependencies-✓-brightgreen?style=flat-square"/>
</p>

<p align="center">
  A cinematic text animation generator that exports real <strong>H.264 MP4</strong> videos — runs entirely in the browser, zero server needed.
</p>

---

## ✨ Features

- 🎥 **Real MP4 export** — H.264 via WebCodecs API + mp4-muxer (no FFmpeg, no backend)
- 📦 **WebM fallback** — automatic fallback for Firefox / Safari
- 🌐 **Bilingual** — full Arabic (RTL) + English support, Arabic diacritics supported
- 🌙 **Dark / Light** theme toggle
- ⚙️ **Fully customizable** — text size, speed, line count, glow, scroll direction
- ⚡ **Optimised render loop** — cached fonts, two-pass draw, no redundant GPU state changes
- 📐 **9:16 canvas** — 1080 × 1920 px, perfect for Instagram / TikTok Reels
- 🚫 **Zero dependencies** — single HTML file, works offline

---

## 🚀 Live Demo

👉 **[Try it here](https://hossam-majrashi.github.io/reel-text-generator/)**

---

## 📸 Preview

| Dark Mode | Light Mode |
|-----------|------------|
| ![dark](https://placehold.co/400x220/0a0a0a/ffffff?text=Dark+Mode) | ![light](https://placehold.co/400x220/f4f4f4/111111?text=Light+Mode) |

---

## 🎬 How to Export

| Format | How | Compatibility |
|--------|-----|---------------|
| **MP4 (H.264)** | WebCodecs + mp4-muxer | Chrome / Edge 94+ |
| **WebM (VP9)** | MediaRecorder API | All modern browsers |

> MP4 automatically falls back to WebM if WebCodecs is not available.

---

## 🛠️ Usage

**Option 1 — Direct (no install)**
```
Download index.html → open in Chrome → done
```

**Option 2 — GitHub Pages**
```
Fork this repo → Settings → Pages → Deploy from main → /root
```

**Option 3 — Local server**
```bash
# Python
python -m http.server 8080

# Node
npx serve .
```

---

## ⚙️ Controls

| Control | Description |
|---------|-------------|
| **Text** | The text that scrolls across the reel |
| **Text Size** | Base font size (16–72) |
| **Speed** | Scroll speed (1–12) |
| **Lines** | Number of text rows (4–28) |
| **Glow** | White glow/bloom intensity (0–20) |
| **Direction** | Left ← or Right → scroll |
| **Duration** | Recording length: 5s / 10s / 15s / 20s / 30s / 60s |
| **Format** | MP4 (H.264) or WebM |

---

## 🏗️ Technical Details

### Render Pipeline
```
Text settings
     │
     ▼
OffscreenCanvas (1080×1920)
  ├─ Pass 1: non-blurred words  ← single GPU state change
  └─ Pass 2: blurred words      ← per-word filter
     │
     ▼
Preview Canvas (270×480) ← scaled down via drawImage
```

### MP4 Recording Pipeline
```
Animation Loop (30 fps)
     │
     ▼
VideoFrame(offCanvas)
     │
     ▼
VideoEncoder (H.264 avc1.640029)
     │
     ▼
mp4-muxer → ArrayBuffer → Blob → Download
```

### Performance Optimisations
- **Font caching** — `fontStr` stored on each word object, rebuilt only on reset
- **No `save()/restore()`** — manual state reset, fewer GPU round-trips  
- **Two-pass rendering** — non-blurred words in one batch, blurred words separately
- **`isAR` flag cached** — Arabic detection runs once per word, not per frame
- **30 fps cap** — timestamp-gated `requestAnimationFrame` loop

---

## 📁 Structure

```
reel-text-generator/
├── index.html      # Everything — HTML + CSS + JS, single file
└── README.md
```

---

## 📄 License

MIT © [Hossam Hassan Majrashi](https://github.com/hossam-majrashi)

---

<p align="center">Built with ❤️ using vanilla HTML · CSS · JavaScript</p>
