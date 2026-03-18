# 🎵 How to Add Your Own Music to Nexyra

## THE PROBLEM WITH APIS
APIs like Spotify & Deezer don't give us full songs - they give 30-second previews. That's why you hear weird sounds!

## THE SOLUTION: YOUR OWN MUSIC FILES

### Step 1: Download Your Songs
Download MP3 files of songs you want (from any app/website)

### Step 2: Edit songs.json
Open `songs.json` and replace with your music:

```json
[
  {
    "id": "1",
    "name": "Heat Waves",
    "artist": "Glass Animals",
    "album": "Dreamland",
    "image": "https://i.scdn.co/image/ab67616d0000b273a4a6c8390a374b951a10f656",
    "duration": 239000,
    "audio": "audio/heat-waves.mp3"
  },
  {
    "id": "2",
    "name": "Blinding Lights", 
    "artist": "The Weeknd",
    "album": "After Hours",
    "image": "https://i.scdn.co/image/ab67616d0000b2730c2f6e2a3b3c5d4e5f6a7b8c",
    "duration": 200000,
    "audio": "audio/blinding-lights.mp3"
  }
]
```

### Step 3: Upload MP3 Files
Create a folder called `audio` and put your MP3 files:
```
nexyra/
├── index.html
├── songs.json
├── audio/
│   ├── heat-waves.mp3
│   ├── blinding-lights.mp3
│   └── your-song.mp3
```

### Step 4: Push to GitHub
1. Add all files to git
2. Push to GitHub
3. Wait 2-3 minutes
4. Done! Your music plays!

## HOW TO GET ALBUM COVERS
1. Search: "Glass Animals Dreamland album cover"
2. Find image → Right click → Copy image address
3. Paste in `image` field

## HOW TO GET SONG DURATION
1. Search on Google: "Heat Waves Glass Animals duration"
2. Get seconds (e.g., 3:59 = 239 seconds)
3. Multiply by 1000: 239000 (this is in milliseconds)

## EXAMPLE songs.json WITH YOUR DOWNLOADED MUSIC

```json
[
  {
    "name": "Name of YOUR downloaded song",
    "artist": "Artist Name",
    "image": "https://link-to-album-cover.jpg",
    "duration": 180000,
    "audio": "audio/your-song-file.mp3"
  }
]
```

## IMPORTANT NOTES
- Audio file path: `audio/filename.mp3` (relative path)
- Image must be a direct URL (ends in .jpg or .png)
- Duration is in MILLISECONDS (3:00 = 180000)
- JSON format must be valid (check for commas)

## DEPLOYMENT
After editing:
1. `git add .`
2. `git commit -m "Added my music"`
3. `git push`
4. Wait for GitHub Pages to update
5. Visit https://devpatel990.github.io/nexyra/

That's it! Your downloaded songs will play perfectly!
