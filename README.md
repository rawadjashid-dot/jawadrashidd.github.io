# Academic website

A static site with four sections on one page: About, Projects, Publications and Opinions. It needs no build step. Fonts (Inter, JetBrains Mono) load from Google Fonts.

Like wongmjane.com, the site is white for visitors in light mode and dark for visitors whose system is in dark mode. To make it always white, delete the `@media (prefers-color-scheme: dark)` block near the top of `style.css`, and change `content="light dark"` to `content="light"` in the `color-scheme` meta tag of each HTML file.

```
index.html              the whole site
style.css               all styling
opinions/template.html  copy this for each opinion piece
images/photo.jpg        your photo (add it, square)
images/projects/*.jpg   one image per project (add them)
cv.pdf                  your CV (add it)
```

## Images to add

Until an image exists, the page shows a light grey box in its place.

| File | Used for |
|---|---|
| `images/photo.jpg` | photo next to your name (square, at least 400×400) |
| `images/projects/pcbkit.jpg` | PCBKIT |
| `images/projects/traffic.jpg` | Traffic Vehicle Detection and Counting |
| `images/projects/ball-balance.jpg` | Ball Balancing Platform Control |
| `images/projects/sap1.jpg` | SAP-1 8-bit Computer |
| `images/projects/bt8051.jpg` | Bluetooth Interfacing with 8051 |
| `images/projects/snake-ladder.jpg` | Digital Snake and Ladder Game |

Project images are cropped to a 16:10 shape. A screenshot, photo of the hardware, or a result figure from each repo works well.

## Writing an opinion

1. Copy `opinions/template.html` to a new file, e.g. `opinions/why-real-datasets-matter.html`.
2. Fill in the title, date, reading time and text.
3. In `index.html`, find the Opinions section and replace one of the three placeholder entries: set its `href` to your new file, and fill in the title, date and first sentence or two.
4. Delete any placeholder entries you don't use before publishing.

## Publish on GitHub Pages

1. Create a public repository named **`jawadrashidd.github.io`**.
2. Upload everything in this folder, keeping the `images/` and `opinions/` folders.
3. Go to **Settings → Pages**, choose **Deploy from a branch**, then select `main` and `/ (root)`.
4. After a minute or two the site is live at `https://jawadrashidd.github.io`.
