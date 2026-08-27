# Her Raksha Bandhan surprise

Everything lives in one file: **index.html**. There's no install, no build step — you just edit some text and open it.

## 1. Write your messages (do this first)

Open `index.html` in any text editor (Notepad, TextEdit, VS Code, whatever you've got) and find the block near the bottom that starts with:

```
const CONFIG = {
```

Change these:

- `sisterName` — her name, used in a few places automatically
- `brotherName` — your name, used in the sign-off
- `letter.body` — replace `[WRITE YOUR PERSONAL MESSAGE HERE]` with your note
- `heart.lines` — replace `[WRITE YOUR MOST PERSONAL MESSAGE HERE]` with the most personal part. You can also split it into a few short lines like:
  ```
  lines: [
    "We've fought about everything.",
    "And somehow none of it mattered.",
    "I don't say this enough, but I'm proud of you."
  ]
  ```
  Each line fades in one after another.

You don't need to touch anything else in the file for the words to work.

## 2. Add real photos

Create a folder called `photos` next to `index.html`, and drop your pictures in it. Then in the same CONFIG block, update the `memories.items` list to point at them:

```
items: [
  { src: "photos/beach-2019.jpg", date: "Summer 2019", caption: "Remember this one?" },
  { src: "photos/birthday.jpg",   date: "",             caption: "How did we even survive this day?" },
]
```

Add as many objects as you want, or remove some. `date` is optional — leave it as `""` to hide it. If a photo file is missing or misspelled, the page just shows a nice placeholder instead of breaking, so it's safe to experiment.

## 3. (Optional) Add background music

Create a folder called `music` next to `index.html`, drop an mp3 in it, and update:

```
music: {
  src: "music/your-song-here.mp3"
}
```

If you skip this, the music button simply does nothing when tapped — nothing else breaks.

## 4. Send it to her

The whole thing is one self-contained page, so the easiest options are:

- **Zip the folder** (index.html + your photos/music folders) and send it to her directly — she opens `index.html` and it just works.
- **Host it for free** so she gets a real link — drag the folder into [netlify.com/drop](https://app.netlify.com/drop), or push it to a free [GitHub Pages](https://pages.github.com/) site. Either takes a couple of minutes and gives you a shareable URL.

## A couple of notes

- Everything personal to edit lives in the `CONFIG` object — you shouldn't need to touch any HTML, CSS, or the rest of the JavaScript.
- The page works fine even with zero photos and no music — it just falls back gracefully.
- Test it once yourself on your own phone before sending it, just to see the full flow start to finish.

Happy Raksha Bandhan. 🪢
