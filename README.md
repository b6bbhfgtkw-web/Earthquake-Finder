# Earthquake Triangulation Simulator (P–S Delay)

A lightweight, browser-based lab activity that simulates locating an earthquake epicenter using **three seismograph stations** and **P–S arrival time differences**.

Students:
1. Place three seismic stations on a map
2. Generate a hidden earthquake
3. Pick **P** and **S** arrivals on each seismogram
4. Convert **Δt = tS − tP** to distance and draw circles
5. Triangulate the epicenter where circles intersect

---

## How it works (the key idea)

Because **Vs < Vp**, the S-wave arrives later than the P-wave, and the time separation grows with distance.

Distance is computed from the picked time difference:

\[
d = \frac{\Delta t}{(1/V_s - 1/V_p)} = \Delta t \cdot \frac{V_p V_s}{V_p - V_s}
\]

---

## What’s in this repository

- `index.html` — the full simulator (HTML/CSS/JS in one file)
- `README.md` — this file

---

## Student workflow (quick instructions)

1. Click **Place Stations** and click **three locations** on the map (S1–S3).
2. Click **Generate Earthquake** (the epicenter is hidden).
3. For each station seismogram:
   - Click once to pick the **P** arrival
   - Click again to pick the **S** arrival
   - (A third click resets the picks for that station)
4. Click **Draw Circles** to plot distance circles from each station.
5. The circle intersection region is the estimated epicenter.
6. Optional:
   - **Compute Best-Fit Epicenter** (numerical best-fit location)
   - **Reveal True Epicenter** (check error)

---

## Run locally

Just open `index.html` in a modern browser (Chrome, Edge, Firefox, Safari).

No installation required.

---

## Upload to GitHub (two simple methods)

### Option A: Upload using the GitHub website (easy)
GitHub supports uploading files via your browser:
- In your repo, click **Add file → Upload files**
- Drag and drop your files (including `index.html` and `README.md`)
- Add a commit message and **Commit changes** [1](https://stackoverflow.com/questions/77726552/how-to-deploy-a-website-with-github-pages-from-a-folder-other-than-docs)

### Option B: Push from your computer using Git (best for ongoing edits)
GitHub documents the general flow for adding locally hosted code:
- Initialize repo → stage files → commit → add remote → push [3](https://outlook.office365.com/owa/?ItemID=AAMkAGFkYjhmN2MxLWE1ZGItNDZmMi1iMmE4LWUxNjUyOTkwM2M0MwBGAAAAAABdJgymlNpCSo9qf0SELAKZBwBW7e1OlG%2f8S7%2bGsmXAk6%2fMAAAAHOzLAACVeSLvNjE5Sp6T9uybbQ1VAAXVkMlaAAA%3d&exvsurl=1&viewmodel=ReadMessageItem)

Example commands (run inside the folder with `index.html`):
```bash
git init -b main
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR-USER/YOUR-REPO.git
git push -u origin main
