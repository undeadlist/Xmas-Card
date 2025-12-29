# TuneCards

**Digital music greeting cards for every occasion.**

Send festive, animated greeting cards with embedded YouTube videos and karaoke-style lyrics. Free, customizable, and hosted on GitHub Pages.

![Built by UndeadList](badge.png)

**Live Demo:** [undeadlist.github.io/TuneCards](https://undeadlist.github.io/TuneCards/)

---

## Available Cards

| Holiday | File | Description |
|---------|------|-------------|
| New Year | `newyear.html` | Champagne, fireworks, gold theme |
| Valentine's Day | `valentines.html` | Floating hearts, pink/red |
| St. Patrick's Day | `stpatricks.html` | Shamrocks, pot of gold |
| Birthday | `birthday.html` | Cake, balloons, confetti |
| 4th of July | `july4th.html` | Flags, stars, fireworks |
| Halloween | `halloween.html` | Pumpkins, bats, ghosts |
| Thanksgiving | `thanksgiving.html` | Turkey, falling leaves |
| Christmas | `christmas.html` | Snowflakes, trees, carols |

---

## Quick Start

1. Fork this repo
2. Enable GitHub Pages (Settings → Pages → Deploy from `main`)
3. Share your link: `https://yourusername.github.io/TuneCards/christmas.html`

---

## Customization

### Change the YouTube Video

1. Get your YouTube video ID from the URL:
   ```
   https://www.youtube.com/watch?v=E8gmARGvPlI
                                   ^^^^^^^^^^^
                                   This is the ID
   ```

2. Open any card HTML file and find the iframe:
   ```html
   <iframe id="ytplayer"
       src="https://www.youtube.com/embed/YOUR_VIDEO_ID?enablejsapi=1&origin=https://yourdomain.com"
   ```

3. Replace the video ID and update the `origin` to your domain

### Add Synced Lyrics

Find the `lyrics` array in the JavaScript:

```javascript
const lyrics = [
    { time: 0, text: "Opening line...", type: "" },
    { time: 5.5, text: "Next line at 5.5 seconds", type: "" },
    { time: 10, text: "Chorus!", type: "chorus" },
    { time: 15, text: "Highlight this!", type: "highlight" },
];
```

- `time` — Seconds into the video
- `text` — The lyric to display
- `type` — Style: `""` (normal), `"chorus"` (purple glow), `"highlight"` (green glow)

**Tip:** Play your video and note timestamps for each line.

### Create a New Holiday Card

1. Copy any existing template
2. Update the CSS colors (background, borders, text shadows)
3. Change the floating elements in JavaScript:
   ```javascript
   const floatChars = ['❤️', '💕', '💘'];  // Your emoji set
   ```
4. Replace the ASCII art decorations
5. Update the YouTube video ID
6. Add to `index.html`

---

## Tech Stack

- Pure HTML/CSS/JavaScript
- YouTube IFrame API for video playback
- No build tools, no dependencies
- Hosted free on GitHub Pages

---

## Local Development

Open any HTML file directly in your browser, or run a local server:

```bash
python -m http.server 8080
```

Visit `http://localhost:8080`

---

## License

MIT — Do whatever you want with it.

---

<p align="center">
  <a href="https://undeadlist.com">
    <img src="badge.png" alt="Built by UndeadList" height="40">
  </a>
  <br>
  <sub>Built by <a href="https://undeadlist.com">undeadlist.com</a></sub>
</p>
