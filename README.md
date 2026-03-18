<div align="center">

# Nexyra 🎵

![Nexyra Logo](https://raw.githubusercontent.com/devpatel990/nexyra/main/assets/logo.svg)

### Premium Music Streaming Experience

A production-ready music web application featuring glassmorphism UI, dual API integration, and cinematic animations.

[![License](https://img.shields.io/badge/license-MIT-purple.svg)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/devpatel990/nexyra)](https://github.com/devpatel990/nexyra/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/devpatel990/nexyra)](https://github.com/devpatel990/nexyra/network)
[![Deployed](https://img.shields.io/badge/deployed-GitHub%20Pages-blue)](https://devpatel990.github.io/nexyra)

---

## ✨ Features

### 🎧 Dual API Integration
- **Spotify API** — Browse artists, albums, and top tracks with metadata
- **Deezer API** — Stream 30-second audio previews for seamless playback

### 🎨 Premium UI/UX
- **Glassmorphism Design** — Modern translucent interface with subtle blur effects
- **Animated Background** — Dynamic gradient mesh with floating particles
- **Smooth Animations** — GSAP-powered transitions and micro-interactions
- **Dark Theme** — Deep void black aesthetic with vibrant accent colors

### 🔍 Smart Search
- Real-time search with 300ms debounce
- Combined results from Spotify (artists) and Deezer (tracks)
- Instant playback from search results

### 🎛️ Music Player
- Full-featured mini player
- Play/Pause/Next/Previous controls
- Seekable progress bar
- Volume control with localStorage persistence
- Keyboard shortcuts (Space to play/pause)

## ✨ Features

### 🎧 Dual API Integration
- **Spotify API** — Browse artists, albums, and top tracks with metadata
- **Deezer API** — Stream 30-second audio previews for seamless playback

### 🎨 Premium UI/UX
- **Glassmorphism Design** — Modern translucent interface with subtle blur effects
- **Animated Background** — Dynamic gradient mesh with floating particles
- **Smooth Animations** — GSAP-powered transitions and micro-interactions
- **Dark Theme** — Deep void black aesthetic with vibrant accent colors

### 🔍 Smart Search
- Real-time search with 300ms debounce
- Combined results from Spotify (artists) and Deezer (tracks)
- Instant playback from search results

### 🎛️ Music Player
- Full-featured mini player
- Play/Pause/Next/Previous controls
- Seekable progress bar
- Volume control with localStorage persistence
- Keyboard shortcuts (Space to play/pause)

### 📱 Responsive Design
- Mobile-first architecture
- Optimized for all screen sizes
- Touch-friendly interactions

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection for API access

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/devpatel990/nexyra.git
cd nexyra
```

2. **Open in browser**
```bash
# Simply open index.html in your browser
# Or use a local server for best experience
npx serve .
```

3. **Access the app**
Navigate to `http://localhost:3000` in your browser

## 🎯 Usage

### Browsing Content
- **Trending Artists** — Scroll horizontally through popular artists
- **Top Tracks** — Explore trending tracks in the grid layout
- **Featured Playlists** — Discover curated playlists

### Playing Music
1. Click the play button on any track card
2. Use the mini player at the bottom to control playback
3. Click the progress bar to seek to a specific position
4. Adjust volume using the slider

### Searching
1. Type in the search bar at the top
2. Results appear instantly (debounced)
3. Click any track to start playing immediately

## 🛠️ Technology Stack

| Technology | Purpose |
|------------|---------|
| HTML5 | Structure |
| CSS3 | Styling & Animations |
| JavaScript (ES6+) | Functionality |
| GSAP | Advanced Animations |
| Lucide Icons | Icon System |
| Spotify API | Music Metadata |
| Deezer API | Audio Previews |

## 📁 Project Structure

```
nexyra/
├── assets/
│   └── logo.svg  # Nexyra logo
├── index.html    # Complete application
├── SPEC.md       # Detailed specifications
└── README.md     # This file
```

## 🔧 Configuration

### Spotify API
The app uses Spotify's Client Credentials Flow for authentication. The Client ID is configured in the source code.

For production deployment, consider:
- Using a backend proxy for token exchange
- Implementing OAuth 2.0 for user authentication
- Caching tokens to reduce API calls

### Deezer API
Deezer provides free access to search and preview endpoints without authentication. A CORS proxy is used for browser-based requests.

## 🤝 Support & Contact

For questions, feature requests, or bug reports:

- **Email:** devpatel43@gmail.com
- **GitHub Issues:** https://github.com/devpatel990/nexyra/issues

## 📄 License

This project is for educational and personal use. All music content is provided by Spotify and Deezer APIs under their respective terms of service.

## 🙏 Acknowledgments

- [Spotify](https://www.spotify.com) — Music data and metadata
- [Deezer](https://www.deezer.com) — Audio preview streaming
- [GSAP](https://greensock.com/gsap/) — Animation library
- [Lucide](https://lucide.dev) — Beautiful icons
- [Google Fonts](https://fonts.google.com) — Typography

---

**Nexyra** — *Experience Music Like Never Before*

Made with ❤️ by [Dev Patel](mailto:devpatel43@gmail.com)

</div>
