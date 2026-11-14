# Experimental Aerodynamics Research Laboratory

Website for the Wind Tunnel Laboratory, Department of Mechanical Engineering, University of Idaho.
Director: Dr. Vibhav Durgesh.

It is a static site. It needs no build step and no server code, so it runs anywhere that serves plain files, including GitHub Pages.

## Contents

```
index.html                 the whole page (layout, styles and scripts)
assets/img/                photos, figures and thumbnails (WebP/JPEG)
assets/video/              research movies (H.264 MP4, web-optimized)
assets/data/plif-frames.js 23 pLIF frames (Run 209, 40–62 s) for the interactive explorer
assets/data/ofi-image.js   oil-film image for the fringe-spacing tool
.nojekyll                  tells GitHub Pages to serve files as they are
```

## Publish on GitHub Pages

1. Create a new public repository on GitHub (for example `wind-tunnel-lab`).
2. Upload everything in this folder to the repository root, keeping the `assets` folder structure.
   - Web upload: **Add file → Upload files**, then drag in `index.html`, `README.md`, `.nojekyll` and the `assets` folder.
   - Or from a terminal:
     ```
     git init
     git add .
     git commit -m "Wind tunnel laboratory website"
     git branch -M main
     git remote add origin https://github.com/<your-username>/wind-tunnel-lab.git
     git push -u origin main
     ```
3. In the repository, open **Settings → Pages**, set **Source** to *Deploy from a branch*, choose `main` and `/ (root)`, then save.
4. After a minute the site is live at `https://<your-username>.github.io/wind-tunnel-lab/`.

## Preview locally

Open `index.html` in a browser. Everything works when opened from disk, including the interactive pLIF and oil-film tools.

## Editing

- Text, links and captions are in `index.html`. Search for the section ids: `capabilities`, `research`, `gust`, `plif`, `ofi`, `owl`, `flag`, `people`, `facility`, `instruments`, `contact`.
- To replace an image, keep the same file name in `assets/img/`, or update the `src` in `index.html`.
- Research figures sit in fixed 16:10 frames and keep their own proportions, so any figure size works.

All files are well under GitHub's 100 MB per-file limit. The largest is the airfoil–gust movie at about 4.5 MB.
