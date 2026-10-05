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

Cross a goal and you get confetti — red for daily, yellow for weekly, green for monthly. It fires once, on the log that crosses the line, and only for today, this week, and this month. Backfilling an old week stays quiet. If your device has reduced motion turned on, you get the message without the confetti.

## Reading the rings

Rings fill clockwise as you progress. Inner = daily (red), middle = weekly (yellow), outer = monthly (green). Hover a ring to see current count, goal, and time remaining.

## Weekly goal history

Use the range pills to change the view:
- **1w** — current week broken into individual days, each vs your daily goal
- **6w / 3m / 6m / all** — weekly bars with hit/miss badges

Below it, the **Weekly totals** and **Monthly totals** charts. The weekly chart shows 12 weeks at a time — use **‹** and **›** to page back to older weeks and forward again.

## Reading the stats tab

| Section | What it tells you |
|---|---|
| This week | Apps so far vs the same point last week, last week's total, where this week will land, and your last 7 days vs the 7 before |
| This month | Same idea, by month — so far vs the same date last month, last month's total, and a projection |
| Your rate | Average apps per week, per month, and per day, plus active days per week. Switch between **4w**, **12w**, and **all**. Only completed weeks count, so a half-finished week doesn't drag you down |
| Trends | Last 4 weeks vs the 12 before. ↑ means you're ahead of your usual pace. ↓ comes with a target for this week that would turn it around |
| Last 8 weeks | One row per week — total, change from the week before, active days, and goal ✓/✗ |
| Weekday pattern | Average apps per weekday since you started. Strongest day in green, weakest in amber |
| Breaks & comebacks | A break is 3+ days in a row with no applications. Shows how long you've been back, your last break, and your longest |
| Personal records | Best day, best week, best month, and longest streak — each with the dates and what it takes to beat it |

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
- **Canvas API** — goal confetti, no library
- **Google Fonts** — DM Mono + DM Sans (CDN)
- **localStorage** — primary data store
- **File System Access API** — optional direct read/write to a CSV on disk
- **GitHub Pages** — free static hosting
