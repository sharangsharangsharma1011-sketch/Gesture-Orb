# Gesture Data Orb

Webcam hand-tracking demo (Iron Man / Tony Stark style UI). Pinch to zoom,
spread fingers to expand a data-node network, move your hand to rotate.

- **Hand tracking:** MediaPipe Hands (loaded from CDN, runs client-side)
- **3D rendering:** Three.js
- **No build step** — it's a single static `index.html`

## Run locally
Just open `index.html` in a browser. Camera access requires either
`localhost` or HTTPS — opening the file directly (`file://`) will work in
most browsers for camera permission, but if it doesn't, run a quick local
server:

```
npx serve .
```

## Deploy (Vercel)
This is a zero-config static site, so Vercel needs no build settings.

```
git init
git add .
git commit -m "Initial commit - gesture orb demo"
git branch -M main
git remote add origin https://github.com/<your-username>/gesture-orb.git
git push -u origin main
```

Then on vercel.com:
1. **Add New → Project**
2. Import the `gesture-orb` GitHub repo
3. Framework preset: **Other** (no build command, no output dir needed)
4. Deploy

Camera access needs HTTPS, which Vercel provides by default — no extra
config required.
