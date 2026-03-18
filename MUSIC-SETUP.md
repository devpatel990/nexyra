# 🎵 Nexyra Music Player - Setup Guide

## Quick Start: Use Your Own Music

### Step 1: Download Music Files
Download MP3 files from any source you prefer (YouTube converters, etc.)

### Step 2: Create Your Music Library

1. Create a folder called `audio` in your Nexyra directory
2. Put your MP3 files there (e.g., `heat-waves.mp3`, `blinding-lights.mp3`)

3. Edit the `songs.json` file with your music info:

```json
[
  {
    "id": "1",
    "name": "Heat Waves",
    "artist": "Glass Animals",
    "album": "Dreamland",
    "image": "https://i.imgur.com/your-cover.jpg",
    "duration": 239000,
    "audio": "audio/heat-waves.mp3"
  },
  {
    "id": "2", 
    "name": "Blinding Lights",
    "artist": "The Weeknd",
    "album": "After Hours",
    "image": "https://i.imgur.com/your-cover2.jpg",
    "duration": 200000,
    "audio": "audio/blinding-lights.mp3"
  }
]
```

### Step 3: Upload to GitHub

1. Push your files to GitHub
2. Wait for GitHub Pages to rebuild
3. Your music will play automatically!

## How It Works

The app loads songs in this order:
1. ✅ **Local songs.json** (YOUR music - plays first!)
2. ❓ **Deezer API** (if no local songs)
3. 🔄 **Demo music** (only if all else fails)

## Getting Album Covers

1. Search Google for album art: `Glass Animals Dreamland album cover`
2. Right-click → "Copy Image Address"
3. Paste in the `image` field

## Audio File Hosting Options

### Option 1: GitHub Pages (Free)
- Put MP3s in `audio/` folder
- Push to GitHub
- Wait 2-3 minutes for deployment

### Option 2: Cloud Storage (Free)
- Upload to Google Drive
- Get shareable link
- Convert to direct download URL

### Option 3: Your Own Server
- Upload anywhere that allows direct file access
- Use the full URL in `audio` field

## Example songs.json

```json
[
  {
    "id": "1",
    "name": "Your Song Title",
    "artist": "Artist Name",
    "album": "Album Name",
    "image": "https://example.com/cover.jpg",
    "duration": 180000,
    "audio": "audio/your-song.mp3"
  }
]
```

## Troubleshooting

**Q: Songs not playing?**
- Make sure MP3 files are uploaded to GitHub
- Check the file path matches exactly
- Check browser console for errors

**Q: Images not showing?**
- Use direct image URLs (ending in .jpg/.png)
- Make sure URLs are publicly accessible

**Q: How to get album art?**
- Search on Google Images
- Use Spotify album covers
- Use i.scdn.co links (Spotify CDN)

## Support
Email: devpatel43@gmail.com
