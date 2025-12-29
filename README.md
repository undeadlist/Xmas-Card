# Holiday Cards

Festive web-based greeting cards with YouTube video players, karaoke-style lyrics, and holiday animations.

**Live Demo:** https://undeadlist.github.io/Xmas-Card/

## Available Templates

| Holiday | File | Theme |
|---------|------|-------|
| Christmas | `christmas.html` | Snowflakes, ASCII trees, green/red glow |
| Halloween | `halloween.html` | Floating bats/ghosts, pumpkins, orange/purple |

## Quick Start

1. Open `index.html` in your browser
2. Click on a holiday card to view it
3. Click Play to start the video and lyrics

## Customization

### Change the YouTube Video

1. Find your YouTube video and copy the video ID from the URL
   - Example: `https://www.youtube.com/watch?v=E8gmARGvPlI` → ID is `E8gmARGvPlI`

2. Open the HTML file and find the iframe:
   ```html
   <iframe id="ytplayer"
       src="https://www.youtube.com/embed/YOUR_VIDEO_ID?enablejsapi=1&origin=https://yourdomain.com"
   ```

3. Replace `YOUR_VIDEO_ID` with your video ID

4. Update the `origin` parameter to match your domain (or remove it for local testing)

### Add/Edit Lyrics

Find the `lyrics` array in the JavaScript section:

```javascript
const lyrics = [
    { time: 0, text: "First line appears at 0 seconds", type: "" },
    { time: 5.5, text: "This appears at 5.5 seconds", type: "" },
    { time: 10, text: "Chorus line!", type: "chorus" },
    { time: 15, text: "Highlighted text!", type: "highlight" },
];
```

- `time`: Seconds into the video when the lyric appears
- `text`: The lyric text to display
- `type`: Style options:
  - `""` (empty) - Normal orange/green text
  - `"chorus"` - Purple glow effect
  - `"highlight"` - Green glow effect

**Tip:** Play your video and note the timestamps for each lyric line.

### Create a New Holiday Template

1. Copy an existing template (e.g., `halloween.html`)
2. Rename it (e.g., `valentines.html`)
3. Update colors in the CSS:
   - Background gradient in `body`
   - Border colors on `.video-container`
   - Text colors/shadows on `h1`, `.lyric-current`
4. Replace the ASCII art (trees/pumpkins) with your own
5. Change the floating elements in JavaScript:
   ```javascript
   const floatChars = ['❤️', '💕', '💘'];  // Valentine's example
   ```
6. Update the YouTube video ID
7. Add the new card to `index.html`

## Holiday Template Ideas

Easy templates you can create:

| Holiday | Colors | Floaters | ASCII Art |
|---------|--------|----------|-----------|
| Valentine's | Pink/Red | Hearts | Heart shapes |
| St. Patrick's | Green/Gold | Shamrocks | Pot of gold |
| Easter | Pastel | Eggs, bunnies | Easter bunny |
| 4th of July | Red/White/Blue | Stars, fireworks | Flag |
| Thanksgiving | Orange/Brown | Leaves | Turkey |
| New Year | Gold/Silver | Stars, confetti | Champagne |

## Hosting on GitHub Pages

1. Push your repo to GitHub
2. Go to Settings → Pages
3. Set Source to "Deploy from a branch"
4. Select `main` branch and `/ (root)` folder
5. Your site will be at `https://username.github.io/repo-name/`

**Note:** Use YouTube embeds for video since GitHub Pages doesn't support large files.

## Local Development

Just open the HTML files directly in your browser, or run a local server:

```bash
python -m http.server 8080
```

Then visit `http://localhost:8080`

## License

MIT - Do whatever you want with it!
