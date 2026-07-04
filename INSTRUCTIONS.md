# Instructions

## Logging applications

| Action | How |
|---|---|
| Log for today | Set the count, click **+ add** |
| See a past day's rings | Click any cell in the history grid → a modal shows that day's daily/weekly/monthly rings, judged against the goals that were in effect *that day* |
| Log for a past day | Click a grid cell → **log / edit this day** → set count → **+ add** |
| Correct a day's count | Select the date, enter the correct total, click **set exact** |
| Keyboard shortcut | Type count in the number field, press **Enter** |
| Export data | Click **export csv** — downloads `job-applications.csv` |
| Connect a sync file | Click **sync file**, pick your CSV — app auto-saves to it every session |

## Setting goals

In the **Log** tab, type a number next to Daily, Weekly, or Monthly and click **set**. Goals persist across sessions.

## Reading the rings

Rings fill clockwise as you progress. Inner = daily (red), middle = weekly (yellow), outer = monthly (green). Hover a ring to see current count, goal, and time remaining.

## Weekly goal history

Use the range pills to change the view:
- **1w** — current week broken into individual days, each vs your daily goal
- **6w / 3m / 6m / all** — weekly bars with hit/miss badges

## File sync (recommended)

Click **sync file** and pick a CSV on your disk (create a new one if starting fresh). From that point on the app reads from and writes to that file automatically. Requires Chrome, Edge, or Opera — browsers that support the File System Access API. Firefox doesn't support it yet.

If you're on a browser without File System Access, use **export csv** periodically as a manual backup.

---

## Deploy to GitHub Pages

1. Create a new **public** repo at github.com/new
2. Upload `index.html` via **Add file → Upload files**
3. Go to **Settings → Pages → Source: Deploy from branch → main / root → Save**
4. Your app is live at `https://<your-username>.github.io/<repo-name>/` in ~60 seconds

No build step. The file is completely self-contained.

---

## Tech stack

- **HTML / CSS / Vanilla JS** — no frameworks, no install
- **Chart.js** — bar charts (CDN)
- **Google Fonts** — DM Mono + DM Sans (CDN)
- **localStorage** — primary data store
- **File System Access API** — optional direct read/write to a CSV on disk
- **GitHub Pages** — free static hosting
