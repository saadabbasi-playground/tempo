# Tempo — Focus Timer

A simple productivity app that combines three methods in one place:

- **Time-blocking (anchors)** — fixed daily blocks like gym or deep work
- **Pomodoro** — timed focus sessions with short breaks
- **Eisenhower matrix** — sort tasks by what actually matters

It runs entirely in your browser. No account, no server — your data stays on your device.

---

## Getting started (deploy to GitHub Pages)

1. Create a new GitHub repository (e.g. `tempo`).
2. Upload all the files in this folder to the repository:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
3. In the repository, go to **Settings → Pages**.
4. Under **Source**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
5. After a minute, your app is live at `https://<your-username>.github.io/tempo/`.

**Install it like an app:** open the link on your phone or desktop, then choose **Add to Home Screen** (mobile) or click the install icon in the address bar (desktop). It works offline after the first load.

---

## How to use it

The app has three tabs: **Focus**, **Plan**, and **Stats**.

### 1. Plan your day (Plan tab)

**Set your anchors.** Anchors are the fixed blocks that structure your day — gym, deep work, weekly review. Give each one a name, a start time, and an end time, then press **Add anchor**. They appear as orange arcs on the 24-hour dial in the Focus tab.

**Add your tasks.** Type a task, pick a quadrant, press **Add task**:

| Quadrant | Meaning | What to do |
|---|---|---|
| Do first | Urgent + important | Focus on these today |
| Schedule | Important, not urgent | Plan time for these — this is where real progress happens |
| Delegate / batch | Urgent, not important | Hand off or batch into one block |
| Drop | Neither | Question why it's on the list at all |

Tick ✓ to mark a task done, or × to delete it.

### 2. Run focus sessions (Focus tab)

1. Your top-priority open tasks appear under **Next up**. Tap one to attach it to your session (optional).
2. Adjust focus/break lengths if you like (default 25/5 minutes).
3. Press **Start focus**. The inner blue ring counts down; a chime plays when time is up.
4. A break starts queuing automatically when a focus session ends — press **Start break**, then repeat.

**Reading the dial:**
- **Outer ring** = your whole day (24 hours). Orange arcs are your anchors, the thin hand shows the time right now.
- **Inner ring** = the current Pomodoro counting down.

The line under the timer shows today's total focus minutes and session count.

### 3. Review your progress (Stats tab)

- **Focus minutes and sessions** over the last 14 days
- **Day streak** — any day with at least one completed focus session counts
- A bar chart of daily focus minutes (today is highlighted in orange)

---

## Tips for getting the most out of it

- **Anchor first, task second.** Set 2–3 anchors and protect them — the tasks fill the space around them.
- **Live in "Schedule".** If most of your work sits in Urgent + Important, you're firefighting. Aim to do the important work before it becomes urgent.
- **Don't break the chain.** One completed session a day keeps the streak alive — a low bar on bad days beats a broken habit.

## Notes

- Data is stored in your browser (localStorage). Clearing site data resets the app.
- Works in any modern browser; no build step or dependencies.