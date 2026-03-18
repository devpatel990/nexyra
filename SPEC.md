# Nexyra - Premium Music Web Application

## 1. Project Overview

**Project Name:** Nexyra  
**Type:** Music Streaming Web Application  
**Core Functionality:** A premium music discovery platform integrating Spotify Web API with a stunning glassmorphism UI, featuring artist browsing, track search, and audio preview playback.  
**Target Users:** Music enthusiasts seeking an elegant, cinematic music exploration experience.

---

## 2. UI/UX Specification

### Layout Structure

**Page Sections:**
- **Header:** Fixed navigation with logo, search bar, and nav links
- **Hero Section:** Full-width animated gradient background with featured content
- **Trending Artists:** Horizontal scrollable artist cards
- **Top Tracks:** Grid of track cards with play functionality
- **Featured Playlists:** Curated playlist showcase
- **Mini Player:** Fixed bottom bar for audio playback
- **Footer:** Minimal branding footer

**Grid/Layout:**
- CSS Grid for main layout (12-column system)
- Flexbox for component internals
- Max content width: 1400px
- Side padding: 24px (mobile: 16px)

**Responsive Breakpoints:**
- Mobile: 0-767px
- Tablet: 768-1023px
- Desktop: 1024px+

### Visual Design

**Color Palette:**
- Background Primary: `#0a0a0f` (deep void black)
- Background Secondary: `#12121a` (elevated surface)
- Background Tertiary: `#1a1a25` (card surfaces)
- Accent Primary: `#6366f1` (indigo glow)
- Accent Secondary: `#a855f7` (purple pulse)
- Accent Gradient: `linear-gradient(135deg, #6366f1 0%, #a855f7 50%, #ec4899 100%)`
- Text Primary: `#ffffff`
- Text Secondary: `#9ca3af`
- Text Muted: `#6b7280`
- Glass Background: `rgba(255, 255, 255, 0.05)`
- Glass Border: `rgba(255, 255, 255, 0.1)`
- Success: `#10b981`
- Error: `#ef4444`

**Typography:**
- Logo/Brand: `'Clash Display', sans-serif` (700 weight)
- Headings: `'Satoshi', sans-serif` (600-700 weight)
- Body: `'Satoshi', sans-serif` (400-500 weight)
- Font Sizes:
  - Hero Title: 72px (desktop), 40px (mobile)
  - Section Title: 32px (desktop), 24px (mobile)
  - Card Title: 18px
  - Body: 16px
  - Small: 14px
  - Caption: 12px

**Spacing System:**
- Base unit: 4px
- Spacing scale: 4, 8, 12, 16, 24, 32, 48, 64, 96px

**Visual Effects:**
- Glassmorphism: `backdrop-filter: blur(20px)`
- Card shadows: `0 8px 32px rgba(0, 0, 0, 0.4)`
- Glow effects: `box-shadow: 0 0 40px rgba(99, 102, 241, 0.3)`
- Border radius: 8px (small), 16px (medium), 24px (large)

### Components

**1. Header**
- Logo with gradient text effect
- Glassmorphism background (sticky on scroll)
- Navigation links with hover underline animation
- Search bar (expandable on mobile)

**2. Search Bar**
- Pill-shaped input with glass effect
- Search icon with glow on focus
- Live suggestions dropdown
- Loading skeleton during fetch
- Debounced input (300ms)

**3. Artist Card**
- Circular image with gradient border
- Name below with hover glow
- Hover: scale(1.05) with shadow elevation
- Click: ripple effect

**4. Track Card**
- Album art thumbnail (square, rounded)
- Track name (truncated with ellipsis)
- Artist name (muted)
- Duration display
- Play button overlay on hover
- Playing state: animated equalizer icon

**5. Playlist Card**
- Square cover art (4-grid mosaic for multiple tracks)
- Playlist name
- Description (2 lines max)
- Subtle play button reveal

**6. Mini Player**
- Fixed bottom position
- Glassmorphism background
- Album art (small)
- Track info (scrolling marquee if overflow)
- Play/Pause button with pulse animation
- Progress bar (clickable for seek)
- Volume control
- Current time / Duration

**7. Loading Skeleton**
- Shimmer animation effect
- Matches card dimensions

**8. Error State**
- Illustrated error message
- Retry button

---

## 3. Functionality Specification

### Core Features

**Spotify API Integration:**
- Client Credentials Flow authentication
- Token refresh mechanism
- Endpoints:
  - `/v1/browse/featured-playlists` - Featured playlists
  - `/v1/browse/new-releases` - New album releases
  - `/v1/search` - Search artists, tracks, albums
  - `/v1/artists/{id}/top-tracks` - Artist's top tracks
  - `/v1/artists/{id}/albums` - Artist's albums
  - `/v1/artists/top` - Top artists globally

**Search System:**
- Real-time search with 300ms debounce
- Search types: artists, tracks
- Results grouped by type
- Keyboard navigation (arrow keys + enter)
- Clear button when input has value

**Audio Playback:**
- Preview URL from Spotify API (30s clips)
- HTML5 Audio API
- Play/Pause toggle
- Progress tracking
- Volume control (localStorage persistence)
- Track change handling
- Error handling for missing previews

**State Management:**
- React Context for global state (player, search)
- Local state for component-specific data
- Custom hooks for API calls

### User Interactions

1. **Page Load:** Fetch initial data (trending artists, top tracks, featured playlists)
2. **Search:** Type to see live suggestions, press Enter or click to view full results
3. **Play Track:** Click play button → load preview → start playback → update mini player
4. **Pause Track:** Click pause → stop audio → update mini player state
5. **Seek:** Click progress bar → calculate new time → seek audio
6. **Volume:** Drag slider → update volume → persist to localStorage

### Edge Cases

- No preview available: Show "Preview unavailable" tooltip
- API rate limit: Show error with retry option
- Network failure: Show offline state
- Empty search results: Show "No results found" message
- Long track/artist names: Truncate with ellipsis

---

## 4. Technical Architecture

### Project Structure
```
nexyra/
├── src/
│   ├── api/
│   │   ├── spotify.ts        # Spotify API client
│   │   └── types.ts          # TypeScript interfaces
│   ├── components/
│   │   ├── Header/
│   │   ├── Hero/
│   │   ├── SearchBar/
│   │   ├── ArtistCard/
│   │   ├── TrackCard/
│   │   ├── PlaylistCard/
│   │   ├── MiniPlayer/
│   │   ├── Skeleton/
│   │   └── Section/
│   ├── context/
│   │   └── PlayerContext.tsx # Audio playback state
│   ├── hooks/
│   │   ├── useDebounce.ts
│   │   └── useSpotify.ts
│   ├── styles/
│   │   └── global.css        # CSS variables & base styles
│   ├── App.tsx
│   └── main.tsx
├── index.html
├── package.json
├── tsconfig.json
└── vite.config.ts
```

### Dependencies
- React 18+
- TypeScript
- Vite
- GSAP (animations)
- Lucide React (icons)

---

## 5. Animation Specification

**Background Animation:**
- Animated gradient mesh (CSS keyframes)
- Slow color transitions (20s cycle)
- Floating particle effect (CSS + JS)

**Card Animations:**
- Hover: `transform: scale(1.05)` (0.3s ease)
- Entry: Staggered fade-in from bottom (0.5s)
- Click: Subtle press effect

**Page Transitions:**
- Fade in on route change (0.3s)
- Section reveal on scroll (Intersection Observer + GSAP)

**Micro-interactions:**
- Button hover: Glow pulse
- Play button: Scale bounce on click
- Progress bar: Smooth width transition

---

## 6. Acceptance Criteria

1. ✅ App loads with animated gradient background
2. ✅ Featured playlists display correctly
3. ✅ Trending artists show with proper images
4. ✅ Top tracks render with play functionality
5. ✅ Search returns relevant results (debounced)
6. ✅ Clicking play starts audio preview
7. ✅ Mini player shows current track info
8. ✅ Progress bar updates during playback
9. ✅ All hover effects work smoothly
10. ✅ Responsive on mobile/tablet/desktop
11. ✅ No console errors on load
12. ✅ Branding "Nexyra" prominent throughout
