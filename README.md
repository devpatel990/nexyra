<div align="center">

# Nexyra 🎵

![Nexyra Logo](https://raw.githubusercontent.com/devpatel990/nexyra/main/favicon.svg)

### Premium Music Streaming Experience

A beautiful, production-ready music web application featuring glassmorphism UI, real song previews, YouTube Music integration, and GDPR-compliant consent system.

[![License](https://img.shields.io/badge/license-MIT-purple.svg)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/devpatel990/nexyra)](https://github.com/devpatel990/nexyra/stargazers)
[![Deployed](https://img.shields.io/badge/deployed-GitHub%20Pages-blue)](https://devpatel990.github.io/nexyra)

---

## ✨ Features

### 🎵 Real Music Integration
- **Deezer API** — Stream 30-second previews of real songs
- **YouTube Music** — Click to play full songs on YouTube Music
- **Correct Metadata** — Real album art, artist names, and song titles
- **Unique Audio** — Each song plays its own unique preview

### 🎨 Premium UI/UX
- **Glassmorphism Design** — Modern translucent interface with blur effects
- **Animated Background** — Dynamic gradient mesh with floating particles
- **GSAP Animations** — Smooth transitions and micro-interactions
- **Dark Theme** — Deep void black with vibrant purple gradient accents
- **Consistent Branding** — Same logo across header, footer, and favicon

### ⚖️ Legal Compliance (GDPR Ready)
- **Terms of Service** — Full-screen modal with complete T&C
- **Privacy Policy** — Detailed data collection disclosure
- **Cookie Consent** — Bottom banner with accept option
- **Persistent Consent** — Saves user preferences in localStorage
- **Decline Option** — Users can reject and exit app

### 🔍 Smart Search
- Real-time search with 300ms debounce
- Combined results from Spotify (artists) and Deezer (tracks)
- Instant playback from search results

### 🎛️ Full-Featured Music Player
- **Mini Player** — Bottom bar with full controls
- **Full Screen Player** — Expandable immersive player view
- **Playback Controls** — Play/Pause/Next/Previous
- **Seekable Progress** — Click to jump to any position
- **Volume Control** — With localStorage persistence
- **Keyboard Shortcuts** — Space to play/pause
- **YouTube Integration** — Direct link to full song

### 📱 Responsive Design
- Mobile-first architecture
- Optimized for all screen sizes
- Touch-friendly interactions
- Footer with contact info

---

## 🚀 Live Demo

**https://devpatel990.github.io/nexyra/**

---

## 🎯 How It Works

1. **Accept Terms** — First-time users see consent modal
2. **Browse Music** — Explore trending artists and tracks
3. **Play Preview** — Click any song for 30-sec preview
4. **Full Song** — Click YouTube button for complete track
5. **Stay Tuned** — Preferences saved automatically

---

## 🛠️ Technology Stack

| Technology | Purpose |
|------------|---------|
| HTML5 | Structure |
| CSS3 | Styling, Glassmorphism, Animations |
| JavaScript (ES6+) | Functionality |
| GSAP | Advanced Animations |
| Lucide Icons | Beautiful Icons |
| Spotify API | Artist & Playlist Metadata |
| Deezer API | Real Song Previews |
| YouTube Music | Full Song Playback |

---

## 📁 Project Structure

```
nexyra/
├── favicon.svg          # Brand logo (purple play button)
├── index.html           # Complete application
├── songs.json           # Local music database (optional)
├── SPEC.md              # Detailed specifications
├── README.md            # Documentation
└── .github/
    └── workflows/      # GitHub Pages deployment
```

---

## 🔧 Setup & Installation

### Quick Start

1. **Clone the repository**
```bash
git clone https://github.com/devpatel990/nexyra.git
cd nexyra
```

2. **Open in browser**
```bash
# Option 1: Open directly
open index.html

# Option 2: Local server (recommended)
npx serve .
# Then visit http://localhost:3000
```

3. **Deploy to GitHub Pages**
- Push to GitHub
- Enable GitHub Pages in repository settings
- Your app goes live automatically!

---

## 📊 API Usage

### Deezer API (Audio Previews)
- **Search:** `https://api.deezer.com/search?q={query}`
- **Chart:** `https://api.deezer.com/chart/0/tracks`
- **No Authentication Required**

### Spotify API (Metadata)
- **Client Credentials Flow** for server-to-server auth
- Requires API credentials in code
- Used for: Artists, Albums, Playlists

### YouTube Music (Full Songs)
- External link integration
- Opens in new tab
- No API key needed

---

## 🤝 Support & Contact

**Need help?** We're here for you!

- 📧 **Email:** [devpatel43@gmail.com](mailto:devpatel43@gmail.com)
- 🐛 **Bug Reports:** [GitHub Issues](https://github.com/devpatel990/nexyra/issues)
- 💡 **Feature Requests:** [GitHub Issues](https://github.com/devpatel990/nexyra/issues)

---

## 📄 License

This project is for educational and personal use. All music content is provided by Spotify and Deezer APIs under their respective terms of service.

---

## 🙏 Acknowledgments

- [Spotify](https://www.spotify.com) — Music metadata
- [Deezer](https://www.deezer.com) — Audio streaming
- [YouTube Music](https://music.youtube.com) — Full song playback
- [GSAP](https://greensock.com/gsap/) — Animation library
- [Lucide](https://lucide.dev) — Icon system
- [Google Fonts](https://fonts.google.com) — Typography

---

## ⭐ Show Your Support

If you like Nexyra, give it a star on GitHub!

---

**Nexyra** — *Experience Music Like Never Before* 🎵

Made with ❤️ by [Dev Patel](mailto:devpatel43@gmail.com)

</div>
